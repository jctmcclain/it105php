# IT 105 PHP Code 

## Ubuntu Server
* [Ubuntu Server](https://ubuntu.com/download/server)


## Build a LAMP Installation 
### LAMP 
* Linux
* Apache2
* MySQL
* PHP

## Linux
* Find the IP Address of the machine

```bash
ip a
```

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

```bash
sudo su - root
mysql
```

The MySQL (Mariadb) Command Line prompt 

**mariadb>**

* Show Databases 
```sql
show databases;
```

* Create a Database 
```sql
create database inventory;
```

* Use a Database 
```sql
use inventory;
```

* Create a table in the Database 
```sql 
create table equipment(
id int auto_increment primary key, 
p_sku varchar(30), 
p_name varchar(50),
p_description varchar(100), 
p_qty int);
```

* Select all the records from the equipment table
```sql
select * from equipment;
```

* Insert a record into the equipment table
```sql
insert into equipment(p_sku,p_name,p_description,p_qty)
values('100','carabiner','stuff',8);
```

* Select all the records from the equipment table
```sql
select * from equipment;
```

### Status: 3/4 Baked 
#### Associated with a Course

