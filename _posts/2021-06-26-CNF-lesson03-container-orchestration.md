---
toc: false
layout: post
hide: true
search_exclude: false
comments: true
description: Preparing and publishing application with Docker and Kubernetes
categories: [SCNF]
title: Container Orchestration with Kubernetes 
---

After developing an application it is time to package it and deploy it. One of the most common ways of doing so is utilizing docker and kubernetes. 

## Transitions from VMs to Containers


<figure align = "center">
 <img src="{{ site.baseurl }}/images/scnf/muli-apps-vm.png" alt="VM" />
 <figcaption>
 Figure 1: Application in virtual machines <small>source: Udacity SCNF course</small>
 </figcaption>
</figure>

Then we move into containerized applications 

<figure align = "center">
 <img src="{{ site.baseurl }}/images/scnf/containerized-apps.png" alt="containers" />
 <figcaption>
 Figure 2: Application running in containers <small>source: Udacity SCNF course</small>
 </figcaption>
</figure>