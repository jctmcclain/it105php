# IT 105 PHP Code 

## Build a LAMP Installation 
### LAMP 
* Linux
* Apache2
* MySQL
* PHP

## Linux
* Provided Ubuntu Server
  Install Cockpit management which runs on port :9090
  
```bash
sudo apt-get install cockpit
sudo systemctl start cockpit
```

## Apache2, MySQL, and PHP 

* Install the AMP components

```bash
sudo apt-get install apache2 mariadb-server php
```

* Chack the location for HTML documents

```bash
sudo cat /etc/apache2/sites-available/000-default.conf |grep DocumentRoot
```

By default the DocumentRoot is /var/www/html

```code
# Returns 
# DocumentRoot /var/www/html
```

Navigate to the the default DocumentRoot 
Clone is repository into the DocumentRoot location

```bash
cd /var/www/html/
sudo git clone https://github.com/jctmcclain/it105php.git
```

List (show) the directory /var/www/html/it106php contents

```bash
ls it105php
```

Pull down any changes from the GIT repository

```bash
cd it105php
sudo git pull 
```


## PHP Example Code
* [See index.php](index.php)

## MySQL Primer



  

