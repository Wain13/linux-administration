# Users

## w

- lists users current logged in and their current system use
- displays syste uptime

## last

- user logins, reboots, system crashes, loguts

## passwd

- changes password
  - run as root can be set for user instead of them needing to type it
  - passwd will still change a password even if it gives you a BAD PASSSWORD warning

passwords are stored in **/etc/shadow**
passwords are encrypted with a salt, specified in shadow file

## user commands

- useradd
  - -c comment is usually users name
  - -g primary group
  - -G secondary groups
- userdel
  - -r remove user directory
    - user files are tied to user ID, if you want to save files you need to change the ID of the files so they don't end up tied to a new user with same ID of removed user

## Locking a user out

- usermod -L \<username>
  - modifies the salt result in /etc/shadow
- usermod -U \<username>
  - unlocks
