---
layout: post
title:  "What's behind dockify.it"
date:   2013-10-21 19:51:49
categories: dockify docker docker-registry infrastructure
---

We have been asked recently what sits behind dockify.it and how our whole service is put together so without going into much detail I will say that for our web application we picked [sailsjs](http://www.sailjs.org) which is a nodejs/express based web application framework. We picked sails because it has a decent "default" which allowed us to rapidly bootstrap our project and worry more about the storage and the actual docker-registry blanket rather than spend too much on our web app. We're hosting it on heroku which also allows us to scale and allocate different services fast and easy.

Our private docker-registry boxes are sitting on Amazon EC2 and they're used to process your requests via docker pull/push and also process user permissions based on what you defined for each registry in part. They run nginx in front with SSL on port 443 and communicates with a private local gunicorn webserver (docker-registry). All nicely boxed inside a docker instance of course.

As a storage we are using Amazon S3 to host your repositories, it needs no introduction since S3 is quite standard when it comes to hosting stuff on the internet. We all use it somewhere.