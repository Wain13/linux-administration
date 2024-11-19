# Daemons and Services

Closely related concepts.  

## Daemon

A background program, usually starts at machine boot, doesn't interact directly with user.

- httpd
- sshd

## Service

A Background program with a configration and management tool

- Usually started throuogh **init** or **systemd** or similar service managers
- Service tends to refer to both the Daemon and it's launching utility/managing controller program

## Security

The more external access points and abilities a service has, the higher the risk

- listening ports, for example
