---
title: "Random post of December"
pubDate: "Dec 5, 2016"
heroImage: "https://images.unsplash.com/photo-1605745341112-85968b19335b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1471&q=80"
---

Hi,
Well this last two days were very intriguing 'cause I deploy on a server with docker my blog (this one) and my curiosity didn't end there.

Then I proposed to myself to deploy a private docker registry and did!. But I needed a web view to display all available images and maybe their tags. So I develop a small webapp with nodejs and express.

Finally decided I needed a git repo hub so I look for it and found [GOGS](https://gogs.io) a pretty great and lightweight self-hosted git service.

One more thing! I needed to test my repos and build my images so here is where jenkins takes place. I integrated jenkins with gogs to be trigger by push events and when your branch is master it builds a docker image within jenkins _\*note a DiD takes place_ and then deploy with ansible to main server'!

- [registry.jorgeadolfo.com](https://registry.jorgeadolfo.com)
- [git.jorgeadolfo.com](https://git.jorgeadolfo.com)
- [ci.jorgeadolfo.com](https://ci.jorgeadolfo.com)

-all of them running docker containers :)
