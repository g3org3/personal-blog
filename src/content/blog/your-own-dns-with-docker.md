---
title: 'Your own DNS with docker!'
description: 'Lorem ipsum dolor sit amet'
pubDate: 'Jan 31 2017'
heroImage: "https://plus.unsplash.com/premium_photo-1677448831822-4251f31b9fd5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1632&q=80"
---
### Have you ever wonder how to setup your own dns?

This is my first kind of tutorial for the year and I'll show you how to run your own dns with docker :)

Before you proceed

- have docker installed
  [get.docker.com](http://get.docker.com)
- have docker-compose installed (optional)

#### Step 1

download a dockerized webmin application with bind dns

```
docker pull sameersbn/bind:9.9.5-20161106
```

credit: thanks to [sameersbn](https://github.com/sameersbn/docker-bind)

#### Step 2

run the docker compose, below is the yml file

```
version: '2'
services:
  bind:
    image: sameersbn/bind:9.9.5-20161106
    ports:
      - "53:53/udp"
      - "53:53/tcp"
      - "10000:10000/tcp"
    volumes:
      - ./data:/data
```
