# DigitalOcean Server User Setup

## Task: Create a new user on a freshly launched Ubuntu Droplet

### Environment:
- Host: DigitalOcean Droplet
- OS : Ubuntu 24.10 x64
- Access: Root via SSH

### Steps Performed:

1. **Created a new user named "new_admin" on the droplet server:**

```bash
adduser new_admin
```

2. **Set up SSH access for the new user to login directl to DigitalOcean droplet server:**

```bash
su - new_admin
ssh-keygen -t rsa -b 4096 -C "new_admin@mydroplet"
cat /home/new_admin/.ssh/id_rsa.pub >> /home/new_admin/.ssh/authorized_keys

*Copy output of --> cat /home/new_admin/.ssh/id_rsa.pub --> add as a new ssh key to DigitalOcean to allow SSH login directly to new_admin user without having to login first as root user
```

3. Test SSH login directly to DigitalOcean droplet server

```bash
exit
exit
ssh new_admin@mydroplet-ipaddress
```



