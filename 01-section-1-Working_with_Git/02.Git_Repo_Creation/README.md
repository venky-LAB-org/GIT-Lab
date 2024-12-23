# GIT-Repo-Creation

There are 2 ways we create GIT Repos
```
using "git init ==> Initialize your Existing Directory as GIT Repo "
using "git clone ==> Clone Repo from Remote Server "
```

# git init
```
Step:1 ==> Init your Local Directory as GIT Local Repo 
Step:2 ==> Add your Local git Repo to Remote git Repo 
```
#### Step:1 ==> Init your Local Directory as GIT Local Repo 
```
cd /home/user/OLA-India-DEV  
git init
```
Now in "OLA-India-DEV" Directory you have .git Directory. So "OLA-India-DEV" Directory act as Git Repo now 

#### Step:2 ==> Add your Local git Repo to Remote git Repo 

To Link your Local repository to Your Remote Repository 
```
git  remote add  <Alias-Name>  <Remote-Repo-URL> 
```
Using these Command Link established Now we can Push, Pull the Code from Local to Remote 
```
git remote -v ===> this command will show your remote repo URL
```
```
Open Flipkart project, 

    git  remote add  flipkart  <Flipkart-Remote-Repo-URL> 

Open Amazon project, 

    git  remote add  amazon <Flipkart-Remote-Repo-URL> 
```
# git clone
Project has been Already setup in Centra Repository. 

git clone ==> Command is used to clone Remote Repo into your Local Machine 
```
git clone <Your-Remote-Repo-URL> 
```
There are 2 ways we can clone the Remote repos
```
Http [We hit Username & Password] ====> If we clone using HTTP, we hit username and Password for Every time when you push and/pull 

SSH [We configure ssh keys in GitHub] [passwordless]  ===>  If we clone using SSH, we don’t hit username and Password for Every time when you push and/pull 
```
 
## clone Public Repository 

To clone the Public Repository in 2 ways
```
Using HTTP  ====>  For Cloning Public Repo Using HTTPS we don’t need user name and Password to Clone the Repo 

Using SSH   ===> For Cloning Public Repo Using SSH we  need to Save our Public Key in GitHub 
```


## clone Private Repository 

To clone the private Repository in 2 ways

### using HTTP 
For Cloning Private Repo Using HTTPS we  need user name and Password to Clone the Repo.
Instead of Password we use "PAT Token"

PAT Token ====>  PAT [personal Access token] we use instead of Password. In real-Time we use PAT token only 

Here we create "PAT Token"  for HTTP Clone 
```
Got to GitHub ====> Settings  =====> Developer settings ===> Personal Access Token 

Enter 
        Note ==> Your PAT-Name HERE
        Expiration => Here you mention Expiry Time
        select Scope ==> Here we select the Permission to assign for the Token
```
```
These Token is not Shown again ===> you have to save that Token in safe place
```

### using SSH

Cloning the Private Repo using SSH we need to follow these steps
```
Step:1 =====> Create Public key of your System 
Step:2 =====> Copy your Laptop Public Key in your GitHub 
```
#### Step:1 =====> Create Public key of your System 

Copy your public SSH key

```
ssh-keygen 
cat id_rsa.pub 
```

#### Step:2 =====> Copy your Laptop Public Key in your GitHub 

config SSH Authentication in your Remote GITHUB

```
Got to GitHub ====> Settings  ====> SSH and GPG Keys  

Enter 
        Title ==> Your SSH-Name HERE
        key => Paste your KEY HERE
```
To Test your SSH-Key added to GitHub or Not ? 
```
ssh  -T git@github.com 
```
After you add your Public Key in your GitHub ==> Later you can Clone/Pull/Push any Repository without asking any Password  