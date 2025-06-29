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
cd ./gradle
build
```
**This generated: build/libs/java-react-example.jar

![image](https://github.com/user-attachments/assets/84e48d48-c709-44db-8827-a030b78c5d20)

