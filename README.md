# Backbase Training Exercises

## Portal Backend - Module 3: REST call

This example provides an example of REST call

### Installation & Configuration

- Clone this project into the **services** folder of your project

- Include integration-service-exercise-03 module to the build. Open `services/pom.xml` and add **integration-service-exercise-03** in the `<modules>` section:
	```xml
	    <modules>
	        ...	    
	        <module>integration-service-exercise-03</module>
	        ...
	    </modules>
	```	
	Re-compile **services** by executing `mvn clean install` in the **services** folder.

- Add the newly created module in the Portal application. In the `<dependencies>` section of `webapps/portalserver/pom.xml`, add the following dependency:

	```xml
	    <dependency>
	        <groupId>com.backbase.training</groupId>
	        <artifactId>content-service-exercise-03</artifactId>
	        <version>1.0-SNAPSHOT</version>
	    </dependency>
	```

If you are already running portal server, stop your jetty server. Otherwise, just proceed with the next step.     

### Run & Test

- If Portal Server is already running, stop it by pressing *Ctrl+C*. Start Portal Server application by executing `mvn jetty:run` command from the **webapps/portalserver** directory.
- Call the REST service.
	
```javascript
POST http://localhost:7777/portalserver/services/rest/game/session
{
   "playerId" : "3"
}	
```	
	
	
	
