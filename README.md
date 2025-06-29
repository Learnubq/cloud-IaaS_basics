# cloud & IaaS Basics Module
This is a repository to showcase my cloud and IaaS project for the TWN DevOps Bootcamp. For this project I created a server using DigitalOcean and deployed a Java application on it using Gradle as a build tool.

## Project Description

1. I setup and configured a droplet server on DigitalOcean.
2. I then created and configured a new Linux user on the droplet before deploying an application on it. This is a security best practice as it prevents giving the application root permissions to configure the system, which would have occurred if I deployed the Java application using the root user. The new user I created is called "new_admin".
3. After creating the new user on the droplet I installed Java, built the Java JAR file using Gradle on my local machine and securely copied the JAR artifact to the droplet server.
4. Then I deployed and run the Gradle application on the droplet under the "new_admin" user I created.

## Acknowlegement

I would like to thank Nana and TWN for the opportunity to delve into the world of DevOps engineering through the TWN DevOps Bootcamp. Nana's approach to teaching is very effective and I feel concepts are introduced with the right amount of depth, whilst ensuring you are not overwhelmed with technical jargon, techniques, or tools. She has made a task that initially felt like a mountain to climb without directions, straightforward. I no longer had to worry about whether I was learning the correct concepts or missing out on any important information or skills. Thanks TWN!



