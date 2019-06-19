# Descours & Cabaud

Multi-week project with a multidisciplinary team of developers and testers.
Providing CI/CD pipelines for the microservices developed by the developers and CI/CD for the testers. Deploying the microservices on an internal D&C server with Docker using Docker Compose. These microservices were backed with a Postgres database and RabbitMQ on a different server.
Configuring the exchanges and queues in RabbitMQ, creating schemas in Postgres. Give the schemas the proper authentication (user). Making sure that all the authentication for the RabbitMQ was separate from our project, this was needed for an external company subscribing to our queues.
Created a private registry for the docker images on Nexus and provided jacoco reports on SonarQube.
Also created some extra bash scripts to make the life of the developers easy, get the logs of the Docker containers to debug bugs or misconfigurations.


[Back](../projects.md)
[Home](../../index.md)
