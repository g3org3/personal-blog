---
title: "Boilerplate? Scaffolding? scripts? #nodejs"
pubDate: "Feb 24, 2018"
heroImage: "https://images.unsplash.com/photo-1507126694149-a8685f99aa4f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80"
---

Let’s be honest and answer the following question, the las project you created were you a) copying files from another project, b) copy from a boilerplate c) scaffolding. These are common answers to the pitiful process of starting a new project 😔. I have tried all options and I found them hard to maintain and increase my productivity. I started to build a scaffolding tool yagg but it is still in the works, I will give you an update on that soon.

So having partially failed with that tool I took another approach of having all my build, configs, tools and all the setup in a single module. That way you can easily install the build-tools to a new project and will be easy to maintain and more importantly update! That was another pain, once you updated the boilerplate the old apps could not be updated in a nice, smooth and simple way. This approach will certainly increase my productivity and many of you already recognize the origin of this approach. I was inspired bycreate-react-app and react-scripts , many of you already know but if you don’t please check that out!

https://github.com/facebook/create-react-app

So after 8 hours of non stop coding and some time to write this post, I created 2 repos, george-create-app and gg-scripts. So both are node cli apps but gg-scritpts has the configuration files for eslint, testing and any other that I might need in the future. george-create-app is a cli to install gg-scripts to an existing project but also create a new project from scratch. Having some ideas from my previous project yagg (scaffolding-tool) I added some templates to that cli that I know I must need in any node module I will create, the main skeleton. Feel free to check them out and I invite you to make your own I guarantee that will easily create new projects or use any existing one that you like, cheers!

https://github.com/g3org3/george-create-app
https://github.com/g3org3/gg-scripts

Follow me on medium
https://medium.com/@g3org3dev/boilerplate-scaffolding-scripts-nodejs-931b231ab948

Image taken from unsplash: https://unsplash.com/photos/OIfFRthAASc
