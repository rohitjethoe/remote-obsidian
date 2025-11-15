## Software Prerequisites
---
- Git 2.51+
- Maven 3.9+
- Java 25


## Setup Open JFX
---
1. [https://openjfx.io](https://openjfx.io)
	- Download SDK (Match your JDK version)
	- Scene Builder >> Download
2. Unzip the downloaded SDK `.zip` somewhere
3. Add VM Arguments to your **Run Configs** for the Client
	- `--module-path="/path/to/javafx-sdk/lib" --add-modules=javafx.controls,javafx.fxml,javafx.web`

(The client project contains a README.md with the VM args)

![[Screenshot 2025-11-14 at 14.31.41.png]]

![[Screenshot 2025-11-14 at 14.32.00.png]]