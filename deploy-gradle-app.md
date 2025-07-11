# Gradle App Deployment on DigitalOcean Droplet (as Non-root User)

## Environment:
- Host: DigitalOcean Droplet (Ubuntu 24.10 x64)
- User: "new_admin" (created manually)
- App: Gradle-built Java application
- Location: /home/new_admin/cloud-IaaS_basics/

## Deployment Steps

1. **Switched to "new_admin" user:**

```bash
su - new_admin
```
2. **Cloned the git@gitlab.com:twn-devops-bootcamp/latest/05-cloud/java-react-example.git repository on my local machine:**

```bash
git clone git@gitlab.com:twn-devops-bootcamp/latest/05-cloud/java-react-example.git
```

3. **Built the app with Gradle on local machine:**

```bash
cd java-react-example
gradle build
```
**This generated: build/libs/java-react-example.jar

![image](https://github.com/user-attachments/assets/84e48d48-c709-44db-8827-a030b78c5d20)

4. **Securely copied the JAR file to server's new_admin user's home directory from local machine:**

```bash
scp java-react-example.jar new_admin@dropletserver_ip:/home/new_admin/cloud-IaaS_basics
```

5. **Installed Java openjdk-8 then Ran the Java app in the directory /home/new_admin/cloud-IaaS_basics:**

```bash
sudo apt update
sudo apt install openjdk-8-jre-headless
java -version
java -jar java-react-example.jar
```

**Application started

![Java-app-run](https://github.com/user-attachments/assets/16e75871-0d2c-4e73-bf3c-14d67b246eb4)


