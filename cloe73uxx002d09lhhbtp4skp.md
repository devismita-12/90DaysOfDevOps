---
title: "Day 1: Introduction to Python, Installation, and Configuration"
datePublished: Tue Oct 31 2023 10:38:05 GMT+0000 (Coordinated Universal Time)
cuid: cloe73uxx002d09lhhbtp4skp
slug: day-1-introduction-to-python-installation-and-configuration

---

* ## Introduction to Python and its role in DevOps.
    
    ## **<mark>What is DevOps?</mark>**
    
    DevOps is the combination of software development and operations. This practice allows a single team to handle the entire application lifecycle—from development to testing, to deployment, and operations. DevOps helps reduce the disconnect between software developers, quality assurance engineers (QA), and system administrators.
    
* ## **<mark>Python for DevOps</mark>**
    
    What’s Python’s role in DevOps? Python is one of the primary technologies used by teams practicing DevOps. Its flexibility and accessibility make Python a great fit for this job, enabling the whole team to build web applications, and data visualizations, and to improve their workflow with custom utilities. On top of that, Ansible and other popular DevOps tools are written in Python or can be controlled via Python.
    
* ## **<mark>How To Install Python 3 and Set Up a Programming Environment</mark>**
    
* <mark>For Ubuntu</mark>
    
* ## [Step 1 — Setting Up Python 3](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-an-ubuntu-20-04-server#step-1-setting-up-python-3)
    
    Ubuntu 20.04 and other versions of Debian Linux ship with Python 3 pre-installed. To make sure that our versions are up-to-date, update your local package index:
    
    ```plaintext
    sudo apt update
    ```
    
    ### **Step 2: Install Supporting Software**
    
    The software-properties-common package gives you better control over your package manager by letting you add PPA (Personal Package Archive) repositories. Install the supporting software with the command:
    
    ```plaintext
    sudo apt install software-properties-common
    ```
    
    ### **Step 3: Add Deadsnakes PPA**
    
    Deadsnakes is a PPA with newer releases than the default Ubuntu repositories. Add the PPA by entering the following:
    
    ```plaintext
    sudo add-apt-repository ppa:deadsnakes/ppa
    ```
    
    The system will prompt you to press enter to continue. Do so, and allow it to finish. Refresh the package lists again:
    
    ```plaintext
    sudo apt update
    ```
    
    ### **Step 4: Install Python 3**
    
    Now you can start the installation of Python 3.8 with the command:
    
    ```plaintext
    sudo apt install python3.8
    ```
    
    Allow the process to complete and verify the Python version was installed successfully::
    
    ```plaintext
    python --version
    ```
    
    # **How to Install Python on Windows 10**
    
    # [Step 1 — Downloading the Python Installer](https://www.digitalocean.com/community/tutorials/install-python-windows-10#step-1-downloading-the-python-installer)
    
    1. Go to the official [Python download page for Windows](https://www.python.org/downloads/windows/).
        
    2. Find a stable Python 3 release. This tutorial was tested with Python version 3.10.10.
        
    3. Click the appropriate link for your system to download the executable file: **Windows installer (64-bit)** or **Windows installer (32-bit)**.
        
    
    ![Download Python Installer](https://deved-images.nyc3.digitaloceanspaces.com/CONTINT-1526%2Fpy_download.png align="left")
    
    # [Step 2 — Running the Executable Installer](https://www.digitalocean.com/community/tutorials/install-python-windows-10#step-2-running-the-executable-installer)
    
    1. After the installer is downloaded, double-click the `.exe` file, for example `python-3.10.10-amd64.exe`, to run the Python installer.
        
    2. Select the **Install launcher for all users** checkbox, which enables all users of the computer to access the Python launcher application.
        
    3. Select the **Add python.exe to PATH** checkbox, which enables users to launch Python from the command line.
        
    
    ![Customize Installation](https://deved-images.nyc3.digitaloceanspaces.com/CONTINT-1526%2Fpy-installer-customize.png align="left")
    
    1. If you’re just getting started with Python and you want to install it with default features as described in the dialog, then click **Install Now** and go to [Step 4 - Verify the Python Installation](https://www.digitalocean.com/community/tutorials/install-python-windows-10#step-4-verify-the-python-installation). To install other optional and advanced features, click **Customize installation** and continue.
        
    2. The **Optional Features** include common tools and resources for Python and you can install all of them, even if you don’t plan to use them.
        
    
    ![Python Optional Features](https://deved-images.nyc3.digitaloceanspaces.com/CONTINT-1526%2Fpy-installer-optional.png align="left")
    
    1. Click **Next**.
        
    2. The **Advanced Options** dialog displays.
        
    
    ![Python Advanced Options](https://deved-images.nyc3.digitaloceanspaces.com/CONTINT-1526%2Fpy-installer-advanced.png align="left")
    
* 1. Click **Install** to start the installation.
        
    2. After the installation is complete, a **Setup was successful** message displays.
        
    
    ![Python setup was successful](https://deved-images.nyc3.digitaloceanspaces.com/CONTINT-1526%2Fpy-installer-success.png align="left")
    
      
      
    
    ## How to Use Python Online Compiler
    
    Follow the simple steps below to compile and execute Python online using your favourite browser, without having any setup on your local machine. This online Python editor will help you run Python online programs. You can use this Python online editor to execute your Python programs.
    
    **Step-1** Type your source using available text editor in this Online Python Compiler
    
    **Step-2** Click Run to get the Output from this Python Interpreter Online
    
    **Note:** Before Compilation and using this Python IDE online, you must know about [Python](https://www.guru99.com/python-tutorials.html).
    
    ## Online Python Compiler (Editor / Interpreter / IDE)
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698748648072/8cd5fc2c-6092-4ade-ae6f-29ae4f53153c.png align="center")