# DigitalOcean Server User Setup

## Task: Create a new user on a freshly launched Ubuntu Droplet

### Environment:
- Host: DigitalOcean Droplet
- OS : Ubuntu 24.10 x64
- Access: Root via SSH

### Steps Performed:

1. **Created a new user named "new_admin" on the droplet server and adding to sudo group:**

```bash
adduser new_admin
usermod -aG sudo new_admin
```
![pwd](https://github.com/user-attachments/assets/02df1c8e-f085-46f5-b207-56522f961fb0)


2. **Set up SSH access for the new user to login directly to DigitalOcean droplet server - need to provide SSH key for root user to new_admin user otherwise server won't recognize the new_admin user:**

*Copy your public SSH key from local machine and paste in the droplet server's new_admin user's .ssh folder you will create (in authorized_keys file)
```bash
su - new_admin
mkdir .ssh
sudo vim .ssh/authorized_keys
```

*Copy output of --> cat /home/new_admin/.ssh/id_rsa.pub --> add as a new ssh key to DigitalOcean to allow SSH login directly to new_admin user without having to login first as root user


3. Test SSH login directly to DigitalOcean droplet server

```bash
exit
exit
ssh new_admin@mydroplet-ipaddress
```



