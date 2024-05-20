# 📋 Week 1 Notes: Intro & Environment Setup


## ⚙ Environment Setup 

### 1. Create EC2 Instances

https://www.youtube.com/watch?v=IXSiYkP23zo&list=PL3MmuxUbc_hIUISrluw_A7wDSmfOhErJK 

### 2. Connect Local Machine(MAC) to EC2 Instances
#### Given that we Created the Key Pair and downlaoded into our machine, following are the steps to connect to EC2 Instance from Local Machine
 When we try connecting to Instance 
 **Lets say my PEM file is downloaded in the below path 

Execute the Below:
```sh
 $ ssh -i /Users/user_name/.ssh/key.pem ubuntu@13.127.221.83
```
key.pem       --> Your Key name
ubuntu        --> user name
13.127.221.83 -->

2.1 Change Access of PEM File

```sh
$ mkdir soft
$ cd soft
```
