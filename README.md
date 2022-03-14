# My api server dockerized
## What service I have dockerized?
I dockerized my API server that you can find [here](https://github.com/ludotosk/json-corsi-fastify),obviously I used the node docker to do the job.
## Docker I used:
* Nginx
* Node
* Certbot
* Watchtower
## How do I manage performance?
I set docker to run the network in host mode, so will provide the best performance possible. I tested this set up with [wrk](https://github.com/wg/wrk), the overhead due to docker is minimal.
## Why I use watchtower?
Related to docker the only thing I can do is keep updated all the docker, this is possible with [Watchtower](https://github.com/containrrr/watchtower).
## Why I use Certbot?
With [Certbot](https://certbot.eff.org/) I can obtain an SSL certificate from let's encrypt.
## Why I use Nginx?
Because following the node.js official documentation using node.js with root privileges is a bad thing in terms of security, so I have installed Nginx to act as a proxy manager and to server certificates provided by  Certbot. 