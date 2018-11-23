# kafka-node

producer &amp; consumer node for kafka

## Link

- [rurumimic/kafka-docker](https://github.com/rurumimic/kafka-docker)  
- [SOHU-Co/kafka-node](https://github.com/SOHU-Co/kafka-node)
  - [npm kafka-node](https://www.npmjs.com/package/kafka-node)

## Ubuntu

[vagrant를 이용한 설치 방법](Vagrant)

우분투 머신 2개를 준비한다. 도커도 같이 설치한다.

## Docker Swarm Mode

**node 1**

```bash
# 아이피는 vagrantfile에서 설정한 100+1이다.
$ docker swarm init --advertise-addr 172.28.128.3

Swarm initialized: current node (hfnp52yy4dr4wwsk29uaanoex) is now a manager.

토큰 생성됨.
```

**node 2**

```bash
$ docker swarm join --token SWMTKN-1-08sas8iky2mrd0xxm0gjwytvcrwh74bs83xne00ynmpp2vmwhk-dl5cp8sudsi5bosmppqbvfbrh 172.28.128.3:2377

This node joined a swarm as a worker.
```

**node 1**

```bash
$ docker node ls
ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
ihicuxdspiawl00t8aelh6uo4 *   ubuntu-xenial       Ready               Active              Leader              18.09.0
p2fca9qr6e8wx13zps1w0uskn     ubuntu-xenial       Ready               Active                                  18.09.0
```
