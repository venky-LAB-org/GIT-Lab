## GIT-Installation

### Ubuntu
```
apt-get update -y
apt-get install git -y
```
### Red-Hat
```
yum update -y
yum install git -y
```

### Install the particular GIT Version

Yum or apt-get will install git version that is present in then Package manager Repo
But if we want to install particular git version we need to follow these steps
```
yum groupinstall "Development Tools" -y 
yum install gettext-devel openssl-devel perl-CPAN perl-devel zlib-devel curl-devel -y 
yum install wget tar -y 
```
```
Open these URL ====>   https://github.com/git/git/releases 

Select your GIT version => Right-Click => copy Link Address 
```
```
wget  <Your Copied-URL>

tar -zxvf <Git-Package-Name> 
cd  <git-Directory> 
make  configure 
make  install 
git  --version 
```

