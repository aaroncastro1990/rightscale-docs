---
title: Key Principles
layout: cm_layout
description: Below are some general best practice principles that you should follow in the Cloud while working with the RightScale Cloud Management Platform.
---


1. **Always roll-forward, never fail backwards or fix in place** When problems occur with a server, the natural tendency for most system administrators is to immediately shell into the machine to diagnose and fix the problem. In the Cloud, you no longer need to waste valuable time trying to fix a problematic server. Simply clone and launch a fresh new server. Concentrate on getting a replacement server back online. Later, you can troubleshoot the bad server and diagnose the problem at your convenience.  
2. **Use Deployments to create Sandboxes** For large scale changes where you might inadvertently introduce incompatibility issues, you should always use deployments to create an isolated sandbox for development and testing purposes. Simply clone the production deployment to create an identical "staging" deployment.  
3. **Start Migrations with Cloned Servers** Once you have a stable production environment, it's better to start with a cloned server instead of trying to launch a fresh new server (perhaps from a new ServerTemplate revision) and then trying to configure it so that it matches your production servers. Always try to remove as much human error out of the equation as possible. If you start with a cloned server, you're guaranteed that it will work the same way. Later, as you make changes to the cloned server such as changing the machine image, ServerTemplate revision, or application and a problem occurs, you'll know exactly what change caused the problem.  
4. **Document your upgrade procedures** Be sure to have a detailed upgrade strategy before making any major changes to your production deployment. For most system administrators, performing upgrades in the Cloud is new and uncharted territory. Remember, in the Cloud, hardware resources are no longer a limitation. You can always practice an upgrade procedure on an internal sandbox before you attempt to make those changes to your live, production environment.  