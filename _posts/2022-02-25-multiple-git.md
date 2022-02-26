---
layout: post
title: 🖥️ Multiple Git accounts on a single machine
subtitle: A quick setup to manage several git accounts
illustration: https://git-scm.com/images/logos/logomark-orange@2x.png
categories: [blog]
tags: [linux, tutorial, git]
comments: false
youtubeId:
---

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/L3L17MUSO)

---

Hello there, long time no see since the last article in December. A late happy new year is due I guess. 
Today's article is to solve a problem that drove me crazy and tested my googlefu to the limit. The problem is simple, I now have to managed two git accounts on the same machine and I want to be able to push on those two accounts easily. I also want to keep using an IDE for easier markdown and code editing. Up until last year I was using atom but I recently switched to Vscodium a few days ago. 

Let's get this straight, there is only one simple solution that will work without driving you crazy. Forget about plugins in VSCode or any IDEs, the solution is ssh keys.

I want to thank Bibil M Jacob who gave me the solution I needed in his 2018 article on [freecodecamp](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/). But I'm going to modify some of his terminal lines to better fit our purpose.

So first thing first you need to setup several things: 
- be sure that you have git installed (ofc)
- install keychain ([debian](https://manpages.debian.org/testing/keychain/keychain.1.en.html), [arch](https://wiki.archlinux.org/title/SSH_keys#Keychain))

We are going to setup your ssh keys for the different accounts your are managing. for simplicity let's imagine this situation: 

>| Accounts |     Email              |  Repo |
>|----------|:-------------          |------ |
>| work     |  work@email.com        | work_repo_name.git |
>| personal |    personal@email.com  | personal_repo_name.git |

### <ins>1. Creating and storing the ssh keys</ins>

If it doesn't exist already, create the .ssh folder:

```$ 
mkdir ~/.ssh
cd ~/.ssh/
```

Then we will create the keys

```$ 
ssh-keygen -t rsa -C "work@email.com" -f "id_rsa_work
ssh-keygen -t rsa -C "personal@email.com" -f "id_rsa_personal
```

You will see 4 files in your .ssh folder: 
- id_rsa_work
- id_rsa_work.pub
- id_rsa_personal
- id_rsa_personal.pub

Open the .pub key in your text editor and copy the key you generated. Next we are going to add the pub key to your github account. 

Log in github, go to your settings, SSH and GPG keys and click on "New SSH key". Give it a name, past the key and you're good. Do that for both accounts, you should have something like this: 

[![ssh key](/images/gitacc/01.png)](/images/gitacc/01.png)

### <ins>2. Adding the keys to ssh-agent</ins>

Now comes the fun part, you want to register the key with the ssh-agent. The problem that I had was that ssh-agent was not running on start-up and it gave me nightmares. I found an easy solution using keychain. Keychain is designed to help you manage your ssh keys with minimal interaction from your part, perfect for us. We are going to add a few lines to your shell configuration in (so .bashrc or zshrc for example), don't forget to source your shell after that:

```$ 
eval $(keychain --eval --quiet ~/.ssh/id_rsa_work)
eval $(keychain --eval --quiet ~/.ssh/id_rsa_personal)
source .bashrc
```

### <ins>3. ssh configuration</ins>

We are going to create a config file and then make the entries for our setup, user any editor you like, I used nano here: 

```$
cd ~./ssh/
touch config
nano config
```
Here is the content: 
```
# Work account
Host github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_work
   
# Personal account
Host github.com-personal   
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa_personal
```
The **_github.com-personal_** is really important here as it's what will make the difference on which account is used.

### <ins>4. Clonging and final git config</ins>

This is the last part, we are getting there. What you will need to do now is cloning your repo locally. If you already have a clone, delete the folder, we will do it from scratch.

Go to your repo page and click on "Code" and select the SSH method and copy the command: 

[![ssh key](/images/gitacc/02.png)](/images/gitacc/02.png)

You will do that for both repos you need to clone of course. 
Now time to clone them but we are going to do a little modification, **add -personal to github.com on the second repo** so it matches our config file: 

```$
git clone git@github.com:work/work_repo_name.git
git clone git@github.com-personal:personal/personal_repo_name.git
```

The final touch, we are going to configure git for each repo: 

```$
cd work_repo_name/
git config --local user.name "work"
git config --local user.email "work@email.com"

cd ..
cd personal_repo_name/
git config --local user.name "personal"
git config --local user.email "personal@email.com"
```
You don't have to specify the _--local_ but it doesn't hurt!

That's it, now you can edit, commit and push on two different accounts depending on what repo you are working on. Now if you are using VScode, no need to tinker with extra extension, it will work! That's what I'm doing right now.

I hope someone will find it usefull, I sure did and this article is the result of a frustrating google search and mix of several articles into a single one with everything you should need. 

Get to work now!