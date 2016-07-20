PrintFlow
======================

A PHP system for collecting and managing alerts and supplyrequest from MPS systems

## Supported MPS systems
* 3Manager
* @Remote

## Requirements
* Web server with PHP support (such as Apache, IIS)
* MySQL 5.0 or newer
* PHP 5.5 or newer, with session support and CLI
* A web browser with cookies and javascript enabled

## Download
You can download the newest release at http://github.com/dotdeas/printflow/releases/

If you prefer to follow the git repository, the following branch and tag names may be of interest
* ``master`` is the current stable release
* ``trunk`` is the development branch

## Installation
1. Upload all the files to your web server
2. Import printflow.sql in the sql dir to your MySQL server
3. Make reportslog and log dir writeable
4. Open and edit config.php

Sample config.php
```
<?php
// database
$dbhost="localhost";
$dbuser="pf-user";
$dbpass="pf-pass";
$dbname="printflow";

// imap
$imap_string="{mail.dotdeas.se:995/pop3/ssl/novalidate-cert}";
$imap_user="reports@printflow.dotdeas.se";
$imap_pass="EmailPassword";

// smtp
$smtp_host"smtp.dotdeas.se";
$smtp_port="587";
$smtp_encryption="tls";
$smtp_auth=true;
$smtp_username="app@printflow.dotdeas.se";
$smtp_password="TrustNo1";
$smtp_fromaddr="app@printflow.dotdeas.se";

// timezone
date_default_timezone_set("Europe/Stockholm");

// password
$password="ff574334c2814795b84a2112dfad89acdff14c7b8b250c9ef19df7d8667ba7a579f1dede842bcf1b523c94bfee4524cd3e57609d4677d2b2a59a55d28c1552bd";
```

## FAQ - Frequently Asked Questions
**Nothing happens when i start the installation?**
> Check you mysql information and if your user has the correct rights to access the database

**How do I get randomized usernames and password?**
> Double click on the username and/or password field and you will get a random generated username and/or password

**CSP stops fetching users when using start-date?**
> Some versions of csp dont work with start-date. If you need them in cmum, then use genxml options to exclude it from the output to csp.

**Expire-date dosnt work in CSP?**
> Make sure you are using the ```com.bowman.cardserv.AdvXmlUserManager``` user-manager class.

**The installer cant connect to MySQL server?**
> Try using ```localhost``` instead of ```127.0.0.1``` if your MySQL server is installed locally

## Contact me
If you found a bug, got a great idea or just want to say hello. Send me a email on andreas@dotdeas.se

## License
Released under the [MIT license](http://makesites.org/licenses/MIT)

PrintFlow includes several third party libraries which come under their respective licenses.