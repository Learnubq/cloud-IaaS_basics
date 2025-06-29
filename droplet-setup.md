# DigitalOcean Server User Setup

## Task: Create a new user on a freshly launched Ubuntu Droplet

### Environment:
- Host: DigitalOcean Droplet
- OS : Ubuntu 24.10 x64
- Access: Root via SSH

### Steps Performed:

1. **Created a new user named "new_admin" on the droplet server and added to sudo group:**

```bash
adduser new_admin
usermod -aG sudo new_admin
```
![pwd](https://github.com/user-attachments/assets/02df1c8e-f085-46f5-b207-56522f961fb0)


2. **Set up SSH access for the new user to login directly to DigitalOcean droplet server - needed to provide SSH key for local machine user to new_admin user otherwise server wouldn't recognize the new_admin user:**

*Copied public SSH key from local machine and pasted into the droplet server's new_admin user's .ssh folder I created (in authorized_keys file)
```bash
su - new_admin
mkdir .ssh
sudo vim .ssh/authorized_keys
```

3. **Tested SSH login directly to DigitalOcean droplet server with new_admin user:**

```bash
exit
exit
ssh new_admin@mydroplet-ipaddress
```
![new_admin_login](https://github.com/user-attachments/assets/45a43ec7-266e-41b9-b1ad-fd988986a8f9)




