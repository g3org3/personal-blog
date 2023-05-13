---
title: "Hunting wild node_modules, I found 12GB! 😳"
description: "Here is a sample of some basic Markdown syntax that can be used when writing Markdown content in Astro."
pubDate: "Feb 14 2018"
heroImage: "https://images.unsplash.com/photo-1598755257130-c2aaca1f061c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
---

Many of us don’t realize how much space does the node_modules take in our machine. Have you think about all the projects or examples you have ever developed in the past that you have forgotten and now is potentially taking GBs of storage.

That’s why I decided to create nm-hunter . “But wait you created another node project to see how much storage are taking the other node projects” With this simple cli you can now have an overview of all your node_modules in a given path and see how much space is taken by them. I did the test my self and found that the sum of all node_modules is around 12GB

So how can I get this ?

```sh
# to install
➜ ~ npm install -g nm-hunter
# to run
➜ ~ nm-hunter
⠏ Hunting wild node_modules: 102 MB
# after a couple of minutes...
⚠️   276 MB  /Users/george/project1/node_modules
✅   565 kB  /Users/george/project2/node_modules
✅  12.8 MB  /Users/george/project4/node_modules
✅   565 kB  /Users/george/project-beta/node_modules
⚠️   902 MB  /Users/george/awesome/node_modules
✅   565 kB  /Users/george/dashboard/node_modules
# and the rest of the node_modules found
total used: 12.3 GB
it took: 2 minutes 59.1 seconds
```

Here is the repo for further reading and [click here to read the post in Medium](https://medium.com/@g3org3dev/hunting-wild-node-modules-i-found-12gb-9e6e9f4039d3)

https://github.com/g3org3/nm-hunter
