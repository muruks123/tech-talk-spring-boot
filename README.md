Switching To MongoDB
===
All we need to do is add the `@EnableMongoRepositories` annotation to our configuration, update the `Robot` domain, and use `org.springframework.data.mongodb.repository.MongoRepository`.

> **Note**: The project doesn't come with an embedded MongoDB datastore similar to H2 so you will need MongoDB running on your machine.

###Building and running
Build the project:
`./gradlew build`

Run the application:
`java -jar build/libs/registration-0.0.2-SNAPSHOT.jar`

Hit the application:
`curl localhost:8080`

Hit the robots resource that we set up:
`curl localhost:8080/robots`

![Slag Brothers](http://www.dan-dare.org/Dan%20FRD/BoulderMobileAni.gif)   
[credit to dan-dare.org for the picture]

Add a robot:
`curl -i -X POST -H "Content-Type:application/json" -d '{  "name" : "Slag Brothers" }' localhost:8080/robots`

Check out the robot we just created:
`curl localhost:8080/robots`
