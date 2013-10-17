---
layout: post
title:  "Welcome to dockify"
date:   2013-10-17 19:51:49
categories: dockify docker docker-registry
---

This is our first post, we just launched and we're excited to share it with you. Making [dockify](http://www.dockify.it) has been a challenge and a pleasure. We love picking on new technologies and a docker private registry, at this early stage, really puts a pressure because everything is so new and evolving/changing so very few things stay consistent.

We watched docker come to life and grow so fast that we just couldn't ignore it any more and decided to make it part of our development stack right away given the huge benefits it brings to the table at a very small size as well.

Since our projects are private we needed a secure environment to host our repositories and eventually share some with our customers. We only found [docker-registry](https://github.com/dotcloud/docker-registry) which is also in BETA to do what we wanted (almost) but there were problems. Since we wanted a SSL secure connection to our registry we had to put our registry behind a webserver such as nginx and also password protect it with a basic authentication which is supported and recognized by docker when pushing or pulling.

The biggest problem was that, once a user is authenticated, he gets access to all other repositories because there isn't any checking implemented to verify who has permission to do what so we decided to create our own registry, based on the one we just linked, but much more sophisticated to allow security checks, permission checks, repository sharing both on reading or writing.

We really don't know how is this going to evolve because docker is very young and devs are constantly changing things but we're really happy to be here right now and take part of it. Should you have any requests or questions please contact us, we're most of the day online via live support.