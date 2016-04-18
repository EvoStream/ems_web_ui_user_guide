---
layout: post
title: Installation and Startup
date:   2016-01-01 00:00:00 +0000
categories: jekyll update
permalink: installation_and_startup
---

## Install and Configure the EMS

Following the instructions that can be found in the EMS User Guide, install the EMS and verify that it is functioning on your platform. You must be sure that the EMS is functional on your system prior to working with the UI. This will greatly simplify any problem solving that may need to be done with the installation of the Web UI!

------

## Environment Installation

The Web-based UI requires the evo-webserver which is the EMS’s local web server and installed along the installation of the EMS package.

The evo-webserver listens to port 8888 as default.

User’s may still use other web-servers such as:

- NGINX
- LIGHTTPD
- Apache: WAMP/LAMP, XAMPP, etc.
- IIS



Required Modules to Install:

- PHP5 – PHP language translation modules


- PHP\_CURL\* – Handles external HTTP Post/Get requests. Required to interact with the EMS.

> Some recent distributions of WAMP/LAMP have been released with corrupt PHP\_CURL modules! If the Web UI does not cause any logging events on the EMS (see below), then your CURL module may be inactive or corrupt.

Please refer to the documents of your chosen web server for installation and configuration directions.

------

## Web UI Installation

The Web UI is located in the evo-webroot folder which is the evo-webservices’ web root. If user will use other web server, simply copy the contents of the EMS Web UI into the Web Server’s web root.

Test the installation by navigating to:

``` 
http://localhost:8888/EMS_Web_UI/index.php
```

**Notes:**

- EMS should be running to open Web UI
- localhost – IP address of the EMS
- 8888 - Web server’s assigned port.

This will open the EMS Web UI’s home screen.

![homepage]({{site.url}}{{site.baseurl}}/assets/homepage.jpg)

