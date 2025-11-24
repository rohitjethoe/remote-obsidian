---
tags:
  - CSE1105
title: "Self-Study: Getting Started with Spring"
---
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


