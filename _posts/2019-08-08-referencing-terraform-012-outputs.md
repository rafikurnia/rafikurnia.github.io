---
title: "Referencing Terraform 0.12 stack's output from Terraform 0.11"
tags: [terraform]
layout: post
excerpt_separator: <!--more-->
published: true
---

Terraform recently announced version 0.12 which introduces lots of changes.  
<!--more-->
I was afraid that using Terraform 0.11 to access [outputs](https://learn.hashicorp.com/terraform/getting-started/outputs.html#defining-outputs) from Terraform 0.12 stack is not possible.

Fortunately, it is not the case!

[Remote state](https://www.terraform.io/docs/providers/terraform/d/remote_state.html) data provider still works just fine.