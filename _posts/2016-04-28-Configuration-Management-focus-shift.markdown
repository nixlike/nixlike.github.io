---
layout: archive
title:  "Configuration Management frameworks focus shift."
author_profile: true
categories: jekyll update
---

### So, what's wrong with traditional tools like Chef, Puppet, Ansible, Salt?   
All's fine!!   
They are widely used and everyone seems happy with them.  
So what is these all about?   
It's about effectiveness and focus.  

### First, lets figure out how we use CM tools now:  
- Bootstrap servers.  
- Apply Desired State Configuration cookbooks to update, deploy, orchestrate services.  
- Engineers maintain static inventories (server lists) or use some modules to refresh dynamically. 
- Write complex cookbooks (often modules) to support all areas of application maintenance etc.  

The above way to deliver change is in place in many organizations due to many reasons, such as, historical, legacy environments, process limitations etc...

### So what has changed?

Nowadays, even skeptics classify as "cloud age", migration is inevitable trend for most of companies.   
Cloud, in turn, brings new possibilities to scale and automate.

### What's being observed:   
- Desired state configuration is not so critical, however, important, since we bake image from scratch and OS part is static. Examples: Packer, docker build etc.   
- All infrastructure orchestration is done on IaaS or PaaS layers.  
- Push approach and generating server inventories inside CM framework work bad with auto scaling and disposable servers. The simplest flow is to bake static artifacts into OS image, pull dynamic ones and trigger service discover mechanism.   
- Micro services, which is increasing trend, deploy is trivial and CM tool is often overkill.   
- Service discovery using CM tools became anti pattern. There special tools like consul, etc, zookeper available ..   

