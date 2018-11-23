# Vagrantfile

- vagrant: [ubuntu 16.04](https://app.vagrantup.com/ubuntu/boxes/xenial64)
- docker

```bash
$ vagrant up

...

$ vagrant status

Current machine states:

node-1                    running (virtualbox)
node-2                    running (virtualbox)

$ vagrant ssh node-1
# or
$ vagrant ssh node-2

Welcome to Ubuntu 16.04.5 LTS (GNU/Linux 4.4.0-139-generic x86_64)

# check docker version
vagrant@ubuntu-xenial:~$ docker

Docker version 18.09.0, build 4d60db4
```
