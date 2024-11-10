# Creating a new user from scratch

## New User

RHMS:

- **useradd -m \<name>**
  - -m will create the home directory
- **passwd \<name>**

## Groups

**useradd** will create a private primary group matching the user name for the user by default  
Advantages to having private user group include:

- isolation/security
- files shared only with the user by default, no confusion about group access
- private group model avoids group conflicts

User still needs to be added to other secondary groups to have access to most things  

### sudo access

- Debian based distros use the **sudo** group as the admin (sudo access) user group
- Redhat based distros use **wheel**

An example:

- **usermod -aG sudo,www-data,adm \<name>**
  - This is a sample of ubuntu groups for a remote server user admin account with sudo access
  - sudo is the admin group (admin is deprecated)
    - has sudo privileges
  - www-data gives access to web logs
  - adm system log access administrative file access
    - /var/log/syslog
    - /var/log/auth.log
    - /var/log/dmesg
    - /var/log/kern.log
    - /var/log/apt/history.log

## Set the default shell

- **sudo usermod -s /bin/bash \<name>**


## Setting up the home directory

- **sudo mkdir -p /home/\<name>**
- **sudo chown \<name>:\<name> /home/\<name>**
  - sets directory ownership to the user and the user primary group
- **sudo chmod 755 /home/\<name>**
  - rwx for owner, rx for everyone else

## Profile

The user at this point doens't have any profile information invoked at login  
defaults are at /etc/skel

- **sudo cp /etc/skel/.bashrc /home/\<name>/**
- **sudo cp /etc/skel/.profile /home/\<name>/**
- **sudo chown \<name>:\<name> /home/\<name>/.bashrc /home/\<name>/.profile**

### Testing

When all of the above is complete the user account should be able to be logged into and function as expected.  
This can be tested using the su command with login switch '-' or '-l'  
  
- **su -l \<name>**
  - **exit** to exit  
  
## Setting up SSH access

Create the user .ssh directory

- **sudo mkdir /home/\<name>/.ssh**
- **sudo chmod 700 /home/\<name>/.ssh**
- **sudo chown \<name>:\<name> /home/newusername/.ssh**

### SSH **in**

In order to connect to the server with the new user account over ssh  
Create the authorized_keys file and add the public key for connection into it

- **sudo nano /home/newusername/.ssh/authorized_keys**
  - copy/paste or otherwise add the public key as a separate line in the file
- **sudo chmod 600 /home/\<name>/.ssh/authorized_keys**
- **sudo chown \<name>:\<name> /home/newusername/.ssh/authorized_keys**

### SSH **out**

Create an ssh key

- **ssh-keygen**
