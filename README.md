# Ansible Role: emqttd

The Massively Scalable MQTT Broker for IoT and Mobile Applications.

[http://emqtt.io/](http://emqtt.io/)

# Role Variables

```
emqtt_release: 2318
```

Reference to [offical changelog](http://emqtt.io/changelogs/3001)

* 3001 - Version 3.0-beta.2
* 3000 - Version 3.0-beta.1
* 2318 - Version 2.3.11
* 2317 - Version 2.3.10
* 2316 - Version 2.3.9
* 2315 - Version 2.3.8
* 2314 - Version 2.3.7
* 2313 - Version 2.3.6
* 2312 - Version 2.3.5
* 2311 - Version 2.3.4
* 2310 - Version 2.3.3
* 2309 - Version 2.3.2
* 2308 - Version 2.3.1
* 2307 - Version 2.3.0
* 2306 - Version 2.3-rc.2
* 2305 - Version 2.3-rc.1
* 2304 - Version 2.3-beta.4
* 2303 - Version 2.3-beta.3
* 2302 - Version 2.3-beta.2
* 2301 - Version 2.3-beta.1
* 2206 - Version 2.2.0

```
linux_release: ubuntu16_04
```

Posible values:
 * centos6
 * centos7
 * debian7
 * debian8
 * debian9
 * ubuntu12_04
 * ubuntu14_04
 * ubuntu16_04

```
emqttd_user: root
```

What user to execute emqttd

```
emqttd_root: /usr/share/local/emqttd
```

What path emqttd should placed

```
tmp_dst: /tmp/emqtt.zip
```

temporary directory

```
limit_nofile: 1024
```

number of opened files

# Example Playbook

```
- hosts: server
  vars:
    emqtt_release: 2318
    linux_release: ubuntu16_04
    emqttd_user: emqtt
    emqttd_root: /usr/share/local/emqttd
    limit_nofile: 1048576
  roles:
    - { role: honomoa.emqttd }
```

# License
CC BY-SA 3.0
