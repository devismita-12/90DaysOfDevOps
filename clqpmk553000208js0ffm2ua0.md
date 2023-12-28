---
title: "Project 2:"
datePublished: Thu Dec 28 2023 19:55:32 GMT+0000 (Coordinated Universal Time)
cuid: clqpmk553000208js0ffm2ua0
slug: project-2

---

### <mark>Jenkins CI/CD pipeline with GitHub webhook integration for Deploying Docker application on EC2 instances using the declaration</mark>

**<mark>Follow the steps:</mark>**

1.     First of all, go to AWS portal, and create a new instance. As,

·       Name: jenkins-server

·       AMI: ubuntu.

·       Instance type: t2.micro (free tier).

·       Key pair login: Create &gt; docker.pem.

·       Allow HTTP.

·       Allow HTTPS.

(Download the .pem file.)

Click on Launch Instance.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703773267928/e75a2e1c-b21f-4846-bd90-bc29bd2fd337.png align="center")

2.     Now, connect to the EC2 instance that you have created. Connect to the through EC2 Instance Connect server:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703773437674/d0dffcc9-8827-4b3c-8ebf-847b57a17230.png align="center")

4.     In the machine, run the command

“ssh-keygen”

This will generate public and private keys in the machine.

Id\_rsa – Private Key.

Id\_[rsa.pub](http://rsa.pub) – Public Key.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703773656316/93422fd6-897a-4743-bb20-561115a8727b.png align="center")

5.     Now we will install Jenkins on the machine, by following this link

[https://www.jenkins.io/doc/book/installing/linux/](https://www.jenkins.io/doc/book/installing/linux/)

This will install java with Jenkins.

6.     Install Docker as well to the machine by running,

“Sudo apt-install [docker.io](http://docker.io)”

7.     Now check if it got installed by running “jenkins --version” and “docker --version”

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703774615204/4f436783-212d-44c2-b3df-767d516778ae.png align="center")

8.     Now, we will allow ports 8080 and 8001 for this machine from a security group. We can find the security group in the VM description. Now, here we need to allow “Inbound Rule” as below:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703774944688/2e419476-d7b6-4cf1-bd6e-95106deccadc.png align="center")

9.     Now, Copy the Public Ip of the machine and paste it to the browser to access the Jenkins portal. As,

"54.84.108.124:8080"

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703775322850/a40e63d0-2879-4e72-ad25-3c377056977f.png align="center")

10.  We need an Administrator Password to unlock this. For that, go to the provided highlighted path in the upper screenshot.

“cat /var/lib/Jenkins/secrets/initialAdminPassword”

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703775443122/9ca177b0-097e-4e2d-a0c8-b794c71d1aa7.png align="center")

11.  Now Click on, “Install Suggested Plugins”

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703775536808/bfc9386f-20f8-4480-9937-0c83311108d3.png align="center")

12.  This will now install the suggested plugins. As

  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703775641837/39972465-5f36-43a2-ab23-c9d7ebd581fc.png align="center")

13.  Now, Jenkins will ask us to create the First Admin User.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703775736736/751e567f-02e6-4e0e-aa71-ed724e0b7889.png align="center")

14.  Add the fields accordingly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703776132301/29759832-061f-45a5-8871-5757b895aa1f.png align="center")

15.  The Jenkins homepage will look like this,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703776217160/f9c97c1d-a16e-44c8-8626-e0f3ab9ddb2e.png align="center")

16.  Now, we will create a CI/CD pipeline, which will fetch the code from GitHub.

17.  From Jenkins Dashboard, Click on “New Item”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703776498948/cffdae2f-6093-43ab-a00b-60e86fbc3dd2.png align="center")

18.  Now, Add name as

Name: todo-app

Project: Freestyle project

Click “Ok”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703776601444/c204aff8-ba6b-4504-91d0-100af3509e5c.png align="center")

19.  Here, we need to fill up the description.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703776983418/231c2185-7223-4a92-984a-bcaef23efb99.png align="center")

20.  In Source Code Management, select Git and Add Repository URL and Credentials.

(If there is not any added credential, we need to add)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703777589427/61a53d2c-2bf7-423b-a004-ba3840399307.png align="center")

21.  In Build Step, select Execute Shell and write following command to build docker image and from Docker image we will create a container.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703778200788/6cc75c0a-606e-407c-9c9a-c8bd6696b797.png align="center")

22.  Now, Click on build Now. And the build will be started, in the build history.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703785313591/7c9ad250-4480-4970-a39a-7935def2c491.png align="center")

23.  In Output Console,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703785329354/ee7dd558-77b8-410f-9225-73bed62def00.png align="center")

24.  After getting success, In the browser, search for

**&lt;public\_ip\_of\_ec2:8000&gt;**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703791139359/b42af89a-c226-4c1b-b81f-a53128a3cd68.png align="center")

**Now, our goal is,**

**·       Whenever the developer commits their code in GitHub, after every commit, it should reflect in the live web app.**

**·       For that, we will use “GitScm polling”.**

**·       Every time, a developer made a commit, a trigger will run automatically, which will rebuild the image and run a container on your behalf as a part of automation that will run the pipeline automatically.**

25.  Now, configure the project again, and add

Build Trigger: GitHub hook trigger for GitScm polling.

Description: GitHub webhook integration

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703791339194/46c31182-ca33-48c6-9722-2c0830a924a8.png align="center")

26.  We need to install the “Git Integration” plugin from Manage Jenkins, by following the path,

(Manage Jenkins &gt; Manage Plugins &gt; Git Integration).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703791506922/55e33375-2ea8-4d66-9ca1-b9ed85e56603.png align="center")

27.  Now, Goto GitHub &gt; Settings &gt; SSH and GPG Keys &gt; New SSH Key.

Add details as

Title:github-jenkins-project

Key type: &lt;public\_key&gt;

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703791849079/497429fd-d688-4143-8d4e-29df86f80fa4.png align="center")

28.  To get the Public key, open the “id\_[rsa.pub](http://rsa.pub)” file and copy the content. (Public Key)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703792010547/dc1c17d3-0e87-494a-b0e0-31075b72ca6b.png align="center")

29.  Now, we need to go to GitHub and create a new SSH and GPG Key.

GitHub &gt; Repo “node-todo-cicd” &gt; Settings &gt; Webhooks.

30.  Add the following details,

Payload URL: http://&lt;public\_ip\_of\_ec2&gt;:8080/github-webhook/

Content Type: application/json

Which event would you like to trigger this webhook?

o  Just the push event.

Active: True

Click on “Add Webhook”.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703792417853/30c19860-5568-48ff-b10b-9f2b8fa3f6dd.png align="center")

31.  Now, Save the configured project.

32.  Do some changes in the code and push to GitHub, this will automatically run a pipeline, and the new code will be Live.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703793270191/d49b6f10-8400-48ef-b8d9-106b14e5a8f2.png align="center")