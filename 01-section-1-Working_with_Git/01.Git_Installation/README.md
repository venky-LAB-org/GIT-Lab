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

Select your GIT version
```
```
wget  <Your Copied-URL>

tar -zxvf <Git-Package-Name> 
cd  <git-Directory> 
make  configure 
make  install 
git  --version 
```


## GIT-Configuration

### System

If any GIT Configuration apply to all the USERS in these System ====> then we Go for these "System" 
```
git config --system 
```

These setting usually stored in "git config" file in 
```
Linux ====>  /usr/etc/git/config  [or]  /usr/local/etc/git/config 

Windows ===> c/program Data/git/config 
```
### Global
If any Configuration applicable  to All the repositories for Particular User ====> Then we go for "Global" 

Generally in Organizations we use these Option Only 
```
git config --global --list ===> to ceck the global configuration 

git  config --global user.name "<Username>" 
git  config --global user.email"<Email-ID>" 
```

```
These setting usually stored in ".git/config" file in User Home Directory 
```

### Local
If any Configuration applicable  to any one Particular  repositories only ====> Then we go for "Local" 
```
Step:1 ====> Go to that Particular Repository where .git is located that Directory 
Step:2 ====> Hit Below Commands to Apply  

            git  config --local user.name "<Username>" 

            git  config --local user.email"<Email-ID>" 
```
```
These setting usually stored  in that Repository ".git" Folder ===> ".git/config" file 
```