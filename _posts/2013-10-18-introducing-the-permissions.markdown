---
layout: post
title:  "Introducing dockify permissions"
date:   2013-10-18 19:51:49
categories: dockify docker docker-registry permissions
---

![Dockify permissions]({{ site.baseurl }}/assets/images/permissions.png)

From the moment we started building dockify we knew that this will be a must for our customers. The ability to share a repository with other members is crucial for teams working together on the same projects so we added the functionality to the core.

The permissions work very simple and the whole experience is very easy and elegant. When you click on a repository that you own (not one where you just have access) you will notice on the right side a small widget **Access permissions for repository name**. The widget has two distinct parts where you can add users: the first one is for adding users with read access while the second is for write access. To add a new user you simply have to click on the plus sign, write the username and press enter. If the user is found in our database it will be added to the appropriate list and your project will abbear on their read or write list of repositories.

To delete a user you simply have to click on the username and it will be removed from the access list. Read access means pulling is allowed while write stands for push. We have in mind to allow users with write access to also read but it's something that we must get feedback on as we're not sure what makes more sense for our clients so make yourself heard. Leave us a comment and we promise to reply ASAP.