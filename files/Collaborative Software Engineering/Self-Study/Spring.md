---
tags:
  - CSE1105
title: "Self-Study: Getting Started with Spring"
---
## Table of Contents
---
- [[#Table of Contents]]
- [[#Personalize the Hello World Controller]]
- [[#Add a Visit Counter to the Hello World Controller]]
- [[#Store Names in the Database]]
- [[#Create a Unit Test for an Endpoint]]

## Personalize the Hello World Controller
---
**Open Template Project**
- Open your team repository in your IDE
- Find `SomeController` in the `server` project
- You can redownload the `.zip` of the template project in Brightspace (Material » W1)

**Add Path Variable**
- Default [http://localhost:8080](http://localhost:8080) will return a basic "Hello, World!"
- Add a second endpoint to `SomeController` that uses `@PathVariable` to capture a name and personalize the greeting

```java
@GetMapping ("/name/{name}")
@Responsebody 
public String name (@PathVariable("name") String name) 
{
	var sb = new StringBuilder("Hello ");
	sb.append(name);
	sb.append('!');
	return sb.toString();
}
```

- Run `server` from your IDE and visit [https://localhost:8080/name/John](https://localhost:8080/name/John)

**Add Request Parameters**
- Extend the new endpoint and add a `@RequestParam` to it

```java
@GetMapping("/name/{name}")
@ResponseBody
public String name(@PathVariable("name") String name, @RequestParam("title") String title) 
{
	var sb = new StringBuilder("Hello ");
	if (title != null) {
		sb.append(title).append(' ');
	}
	sb.append(name);
	sb.append('!');
	return sb.toString();
}
```

- Run `server` from your IDE and visit [https://localhost:8080/name/John/Mr](https://localhost:8080/name/John/Mr)

**Debug Endpoint**
- Add a breakpoint somewhere in the new endpoint
	- Make sure to start `server` with a debugger attached
- Refreshing the page shows that the IDE stops processing at the breakpoint
- Useful to debug requests to your backend

## Add a Visit Counter to the Hello World Controller
****
**Create a Counter Service**
- Add a new service class `CounterService` in the `server` dir

```java
package server;

import org.springframework.stereotype.Service;

@Service
public class CounterService 
{
	private int count = 0;
	
	public int getAndIncrease() {
		return count++;
	}
}
```

**Use the Counter**
- Extend `SomeController` and create a constructor that requests the `CounterService` for injection

```java
private CounterService counter;

public SomeController(CounterService counter) 
{
	this.counter = counter;
}
```

- Now include the counter value in the personalised greeting endpoint

```java
var sb = new StringBuilder("Hello ");
sb.append(" You are visitor #").append(counter.getAndIncrease());
```
- Re-visit [localhost:8080/name/John?title=Mr](localhost:8080/name/John?title=Mr) to see the counter ("Hello Mr John! You are visitor #0")

**Use a Bean**
- Alternative to `@Service` = `@Bean`
- Useful for binding classes that are defined in libraries and which cannot be annotated

```java
@Bean
public CounterService getCounterService() 
{
	return new CounterService();
}
```

- When restarting `server`, functionality is unaffected by this change.

**Change Bean Scope**
- Bean is instantiated once as a singleton for the whole application
- This is not always desired
- Spring offers alternative instantiation strategies, change the instantiation scope:

```java
@Bean
@Scope(value = WebApplcationContext.SCOPE_SESSION, proxyMode = ScopedProxyMode.TARGET_CLASS)
public CounterService getCounterService()
{
	return new CounterService();
}
```

- Reload the page && open an incognito window or second browser
- The counter increases separate in both windows
- Using the `WebApplicationContext.SCOPE_REQUEST` will instantiate on every request, even in the same browser window

## Store Names in the Database
****
**Create a new Entity**
- Create a new data structure for names in the `commons` project (next to the `Quote` class)

```java
package commons;

import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;

@Entity
public class Name 
{
	@Id
	@GeneratedValue(strategy = GenerationType.AUTO)
	public long id;
	public String name;
}
```

**Create a new Repository**
- Create a name repository in the `server` project (next to `QuoteRepository` class)

```java
package server.database;

import org.springframework.data.jpa.repository.JpaRepository;
import commons.User;

public interface NameRepository extends JpaRepository<Name, Long> 
{
	// empty!
}
```

**Inject the Name Repository**
- To use the repository in `SomeController`, we need to request it for injection as well
- Extend the constructor of `SomeController` and assign the repository to a new field

```java
private NameRepository db;
public SomeController(CounterService counter, NameRepository db) 
{
	this.counter = counter;
	this.db = db;
}
```

**Store Request Names**
- Extend the endpoint for personalised greetings in `SomeController`
- Store all provided names in the database

```java
@GetMapping("/name/{name}") 
@ResponseBody
public String name(@PathVariable("name") String name, ...) 
{
	var n = new Name();
	n.name = name;
	db.save(n);
}
```

- Explore the database contents via the Web Console via [localhost:8080/h2-console](localhost:8080/h2-console)
- Ensure that the JDBC URL is `jdbc:h2:file:./h2-database`
- Use the pre-filled credentials to connect

## Create a Unit Test for an Endpoint
---
**Create Test**
- Create a new file `SomeControllerTest` (next to the `QuoteControllerTest`)

```java
package server.api;

import static.org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import server.SomeController;

public class SomeControllerTest 
{
	private SomeController sut;
	
	@BeforeEach
	public void setup() 
	{
		sut = new SomeController(null, null);
	}
	
	@Test
	public void indexReturnsHelloWorld() 
	{
		var expected = "Hello world!";
		var actual = sut.index();
		assertEquals(expected, actual);
	}
}
```