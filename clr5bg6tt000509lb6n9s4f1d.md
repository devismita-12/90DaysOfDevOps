---
title: "Project-3:ansible  Playbooks In Actions For Devops"
datePublished: Mon Jan 08 2024 19:28:51 GMT+0000 (Coordinated Universal Time)
cuid: clr5bg6tt000509lb6n9s4f1d
slug: project-3ansible-playbooks-in-actions-for-devops

---

Hello folks hope you people are doing good. it’s been long since I posted a blog. today I will try to explain Ansible in easy way. I believe it’s going to very helpful. I hope you people would definitely love this Article. so, let’s start the today’s topic.

## What is Ansible?

**Ansible** is an open-source automation and orchestration tool for software configuration management and software deployment.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704725403017/96564249-83ea-4860-89a1-8d819502e13e.png align="center")

## Why use Ansible?

> *courtesy- Ansible official documentation*

W***hat is the need of Ansible? why companies use Ansible?***

Here I won’t go deep in very technical way. I will explain a scenario where the use of ansible will fit.

> *Scenario — Suppose we have 200 servers, and we want to install nginx in all the servers at the same time. so how would we perform this task? I don’t think it’s convenient way to manually go to each server and install nginx one by one. so here Ansible comes in the picture. so now with the help of this amazing tool we can install nginx in all the 200 servers just by a single click. yes, you read it right, this is the magic of Ansible.*

I hope from the above simple scenario, things are bit clear in your mind.

In big MNCs, there are thousands of servers that need to be configured daily. Now imagine if you had to go and configure that each server manually, how tiresome and time-consuming it would have been. And that’s why ansible was created. Ansible allows you to configure multiple nodes at one time from one single controller using **Infrastructure as code.**

The server which has ansible installed is known as the Control node while the remote hosts/servers which are configured are known as Managed nodes.

In ansible, you have two approaches to configure things: -

1. Ad-hoc commands (Command-line)
    
2. Playbooks
    

3)Tasks. The format used for writing playbooks is **YAML.**

The remote servers or hosts which need to be configured are mentioned in the **Inventory**. There are two types of inventories: -

1. Static Inventory
    

2)Dynamic Inventory. We use dynamic inventory if our hosts are running on top of the cloud or in a container engine where the hosts are up and down frequently.

Now I won’t let you deep down in theoretical part. here we will do some Hands-On practice.

# **Things to be covered in Hands-On.**

1. Creating Host server.
    
2. Install Ansible to Host server.
    
3. Creating 2 more EC2 instances (servers)
    
4. Add these EC2s to inventory file.
    
5. Configure the servers using command method.
    
6. Uses of playbooks.
    
7. Deployment of a simple webpage using Ansible.
    

Firstly log into your AWS account.

# **Step\_1**

First of all we will create 3 EC2 instances . make sure all three are created with same key pair. our one server would be host server where we perform all the tasks and rest are other servers.And name the host server as Ansible Master and other server as Ansible Servers.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704729723359/8978aed5-047d-4e36-b0f4-e372ea667839.png align="center")

Servers

# **STEP2**

— Now we will install Ansible in host server (Ansible\_host). you can follow the followings commands to install Ansible.

1. sudo apt-add-repository ppa:ansible/ansible
    
2. sudo apt update
    
3. sudo apt install ansible
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704730270808/8063c91c-a13a-453a-8ccd-88f89a65b21a.png align="center")

# **STEP3**

—Connect the ansible master with ansible servers through ssh. you can follow the following command to copy the key from local to Ansible\_host.

*scp -i “&lt;&lt;key pair name&gt;&gt;” &lt;&lt;key pair name&gt;&gt; &lt;&lt;public DNS of EC2&gt;&gt;:/home/ubuntu/.ssh*

# **STEP4**

— <mark>Now we will access the inventory file using </mark> *<mark>sudo nano /etc/ansible/hosts</mark>*

[https://hashnode.com/post/clopsip58000508lj3l1v95u0](https://hashnode.com/post/clopsip58000508lj3l1v95u0) you can referthis link to figure out inventory, connection , module,play and play book

Ansible ad hoc commands- using ad hoc commands is a quick way to run a single task on one or more managed nodes.

some examples of valid use cases are rebooting servers, copying files, checking connection status, managing packages, gathering facts etc.

The pattern for ad hoc commands looks like this :

*$ansible \[host-pattern\] -m \[module\] -a “\[module options\]”*

now we will define some servers in our inventory file and ping them using *ansible all -m ping (you can refer the Screenshot)*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704735304845/bdd8f431-bfbd-48dd-a4d7-4e28a620c045.png align="center")

Now we will ping the servers and do some server configurations ( refer the screenshot for better understanding)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704737824153/28e84a88-3849-4a79-91d5-b23376c3e189.png align="center")

  
We have successfully established connection with the servers. Now we will check some other commands to check disk space

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704738076174/1be7d3ed-4f07-4d46-afdc-9f244af78693.png align="center")

# **STEP5**

Here we will learn about playbooks. In previous blog I have mentioned about playbooks

**Ansible Playbooks** are a way of sending commands to remote systems through scripts. Ansible playbooks are used to configure complex system environments to increase flexibility by executing a script to one or more systems. Ansible playbooks tend to be more of a configuration language than a programming language.

Ansible playbook commands use YAML format, so there is not much syntax needed, but indentation must be respected. As the name says, a playbook is a collection of plays. Through a playbook, you can designate specific roles to some hosts and other roles to other hosts.

To have all the details precise before continuing with Ansible playbook examples, we must first define a task. These are the interfaces to Ansible modules for roles and playbooks.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704738688282/99ccc0b9-ee7b-487d-b0a8-8338272af57b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704738705088/14de4854-cd97-4425-bcd1-070216617aa3.png align="center")

So now we will deploy a sample webpage using the ansible playbook. this sounds interesting, is it?

so first we will create an index.html file in which source code is present. at the end of the blog i will provide Github repository link where all the codes and playbooks are present.

[https://github.com/devismita-12/Live-nginx-project](https://github.com/devismita-12/Live-nginx-project)

now we will create a playbook to perform this particular task.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704741815535/157370f7-eca9-4e74-8719-79b3154821ff.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704741844889/02253da2-947b-4e9b-b83d-83f69e52408a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704741869015/cb5ce900-8ee6-4fcf-b664-d8330677da80.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1704741897064/0004c905-75dc-45fe-b89e-0eddedc5c195.png align="center")

So, we successfully deployed a sample webpage to all the dedicated servers. and we can access this web application using theirs Public IP address.

So, as you can see I have performed all the tasks successfully. I recommend you to first read this article and understand the entire concepts and then move forward to Hands-ON. I believe this was the easiest way to explain about Ansible.

> *If you folks find any difficulties to perform the labs. kindly mail me at* [devismita1998@gmail.com](https://mail.google.com/mail) *I would be Happy to help.*

o folks, I hope you liked this article. if you find this article helpful then kindly give feedback and also follow me for more, and also do let me know about the topic of next Blog.

— — — — — — THANK YOU\_\_\_\_\_\_\_\_\_

— — — — Devismita Sahoo\_\_\_\_\_\_-