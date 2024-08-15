Modified from Carpenox scripts to install a more vanilla vicidial (no dyn portal, no custom webphone, no certbot)

# VICIDIAL INSTALLATION SCRIPTS (Default is Eastern Time Zone US)
# Centos, Rocky and AlmaLinux Vicidial Install pre_requisites 

```

hostnamectl set-hostname xxxxxx.xxxxx.xxx
### Use YOUR SubDomain

vi /etc/hosts
##Change domain name for actual server ip (xxx.xxx.xxx.xxx   complete domain name    subdomain only)

timedatectl set-timezone America/New_York

yum check-update
yum update -y
yum -y install epel-release
yum update -y
yum install git -y
yum install -y kernel*

#Disable SELINUX
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config    

cd /usr/src/
git clone https://github.com/NJRmaxsip/vicidial-install-scripts.git

reboot

````
  Reboot Before running this script

# Install VICIDIAL scripts

```
cd /usr/src/vicidial-install-scripts
git clone https://github.com/NJRmaxsip/vicidial-install-scripts.git
cd vicidial-install-scripts
```



# Alma/Rocky 9 Installer with Asterisk 16

```
cd /usr/src/vicidial-install-scripts
chmod +x alma-rocky9-ast16.sh
./alma-rocky9-ast16.sh
```

Make sure you update your SSL cert location in /etc/httpd/conf.d/viciportal-ssl.conf


# Install a default database with everything setup ready to go

```
cd /usr/src/vicidial-install-scripts
chmod +x standard-db.sh
./standard-db.sh
```



