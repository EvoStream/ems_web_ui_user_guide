---
layout: post
title: Authentication
date:   2016-01-01 00:00:00 +0000
categories: jekyll update
permalink: authentication
---

Users may opt to add security to the Web UI and this could be done by enabling the authentication for the page. The authentication settings is enabled by default using EMS in an Amazon Instance.

To enable the authentication, uncomment the `auth` section in the webconfig.lua and set the `enable` parameter to `true`.

``` 
auth=
{
	{
	domain="EMS_Web_UI", 
    digestFile="../evo-webroot/EMS_Web_UI/settings/passwords/.htdigest",
    enable=true,
	},
},
```

**Note:** This is only applicable when using EWS as the web server. User should modify the account-settings.php located at ../evo-webroot/EMS_Web_UI/settings when using different web server.

*In ../evo-webroot/EMS_Web_UI/settings/account-settings.php, set the ENABLE_LOGIN to TRUE.*

``` 
@define('ENABLE_LOGIN', TRUE);
```

*See User Guide http://docs.evostream.com/ems_user_guide/webconfigfile#authentication for other details.*





## Opening Web UI with Authentication Enabled

Simply go to the URL of the EMS Web UI and enter the username and password to be used.

![]({{site.url}}{{site.baseurl}}/assets/WebUI_auth.JPG)



### Users

By default, there are two users defined in the ./htdigest file of the Web UI settings.

**A. Administrator**

Default username: evostream

Default password: password

It is recommended to change the password of the Administrator immediately after login. 

The administrator handles the **Account Settings** where the following actions can be made:

- Add account - this will add a user account in the configuration
  
- Delete account - this will delete a user account in the configuration
  
- Reset user's account password - this will reset the user's password to the default user password
  
- Change user's account password - this will change the user's password according to the new set password
  
  ![]({{site.url}}{{site.baseurl}}/assets/account_settings.JPG)

**B. User**

Default username: user1000

Default password: password

The logged in user will not be able to see the Account Settings. The user may only access the EMS Web UI normally.