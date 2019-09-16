---
title: "[TIL] Prevent Privillege Escallation with IAM Boundary"
tags: [AWS, IAM]
layout: post
excerpt_separator: <!--more-->
published: false
---

In a shared AWS Account you will not want to give all users an administrator access.  
<!--more-->
Even after following Principle of Least Privillege, sometimes you must grant several people more permissions for them to manage their infrastructure. For instance, giving IAM Resource permission.

