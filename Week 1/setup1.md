# 📋 Week 1 Notes: Intro & Environment Setup


## ⚙ Environment Setup 


### 1. Create EC2 Instances

https://www.youtube.com/watch?v=IXSiYkP23zo&list=PL3MmuxUbc_hIUISrluw_A7wDSmfOhErJK 

### 2. Connect Local Machine(MAC) to EC2 Instances

#### Given that we Created the Key Pair and downloaded into our machine, following are the steps to connect to EC2 Instance from Local Machine

**To Connect to Ec2 Instances:**

```sh
 $ ssh -i /Users/user_name/.ssh/key.pem ubuntu@13.127.221.83
```
key.pem       --> Your Key name

ubuntu        --> user name

13.127.221.83 --> Public IPv4 address



**If you get error like below:**

Warning: Identity file /Users/user_name/.ssh/key.pem not accessible: No such file or directory.
ubuntu@13.127.221.83: Permission denied (publickey).

Follow the below steps:

2.1 Ensure Correct Permissions on the Private Key File:

```sh
$ chmod 400 /Users/user_name/.ssh/key.pem
```

Now we will be able to run 

```sh
 $ ssh -i /Users/user_name/.ssh/key.pem ubuntu@13.127.221.83
```

### [Optional] Give alias to host

```sh
$ nano .ssh/config
```

Add the following lines inside the config

```sh
$ nano .ssh/config
```

```sh
Host mlops-zoomcamp
    HostName 43.204.110.29
    User ubuntu
    IdentityFile /Users/user_name/Documents/key.pem
    StrictHostKeyChecking no
```

Now , we can connect to Connect to Ec2 Instances by just running:

```sh
ssh mlops-zoomcamp
```

Note:

For very new instance we need to update the Public IPv4 address inside the .ssh/config


