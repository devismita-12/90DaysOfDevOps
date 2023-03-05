---
title: "Day-13 task"
datePublished: Sun Mar 05 2023 10:43:23 GMT+0000 (Coordinated Universal Time)
cuid: clev9m7x6000609moflap2b51
slug: day-13-task

---

**What is Python?**

* It was created by **Guido van Rossum**
    
* Python consists of vast libraries and various frameworks like Django,Tensorflow, Flask, Pandas, Keras etc.
    
* **Python** is a general-purpose, dynamic, high-level, and interpreted programming language. It supports Object Oriented programming approach to develop applications. It is simple and easy to learn and provides lots of high-level data structures. Python is an *easy-to-learn* yet powerful and versatile scripting language, which makes it attractive for Application Development.
    
    Python's syntax and *dynamic typing* with its interpreted nature make it an ideal language for scripting and rapid application development.
    
    Python supports *multiple programming patterns*, including object-oriented, imperative, and functional or procedural programming styles.
    

### How to Install Python?

# Prerequisites

You’ll need a computer running Windows 10 with administrative privileges and an internet connection.

# Step 1 — Downloading the Python Installer

1. Go to the official [Python download page for Windows](https://www.python.org/downloads/windows/).
    
2. Find a stable Python 3 release. This tutorial was tested with Python version 3.10.10.
    
3. Click the appropriate link for your system to download the executable file: **Windows installer (64-bit)** or **Windows installer (32-bit)**.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677950786472/c8b1358d-d9a5-4991-92ef-36e2c681bbbe.png align="center")

# Step 2 — Running the Executable Installer

1. After the installer is downloaded, double-click the `.exe` file, for example `python-3.10.10-amd64.exe`, to run the Python installer.
    
2. Select the **Install launcher for all users** checkbox, which enables all users of the computer to access the Python launcher application.
    
3. Select the **Add python.exe to PATH** checkbox, which enables users to launch Python from the command line.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677951033287/e788d2f9-3f3c-4fa9-aa91-b8d76847ca42.png align="center")
    
4. If you’re just getting started with Python and you want to install it with default features as described in the dialog, then click **Install Now** and go to [Step 4 - Verify the Python Installation](https://www.digitalocean.com/community/tutorials/install-python-windows-10#step-4-verify-the-python-installation). To install other optional and advanced features, click **Customize installation** and continue.
    
5. The **Optional Features** include common tools and resources for Python and you can install all of them, even if you don’t plan to use them.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678011080205/1042ad67-9858-4a8a-9cbc-3a77748724aa.png align="center")

1. Select some or all of the following options:
    
    * **Documentation**: recommended
        
    * **pip**: recommended if you want to install other Python packages, such as NumPy or pandas
        
    * **tcl/tk and IDLE**: recommended if you plan to use IDLE or follow tutorials that use it
        
    * **Python test suite**: recommended for testing and learning
        
    * **py launcher** and **for all users**: recommended to enable users to launch Python from the command line
        
    * Click **Next**.
        
    * The **Advanced Options** dialog displays.
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678011239600/952a8f8b-8e15-42cb-9f72-bafdb7e3698d.png align="center")

1. Select the options that suit your requirements:
    
    * **Install for all users**: recommended if you’re not the only user on this computer
        
    * **Associate files with Python**: recommended, because this option associates all the Python file types with the launcher or editor
        
    * **Create shortcuts for installed applications**: recommended to enable shortcuts for Python applications
        
    * **Add Python to environment variables**: recommended to enable launching Python
        
    * **Precompile standard library**: not required, it might down the installation
        
    * **Download debugging symbols** and **Download debug binaries**: recommended only if you plan to create C or C++ extensions
        
    
    Make note of the Python installation directory in case you need to reference it later.
    
2. Click **Install** to start the installation.
    
3. After the installation is complete, a **Setup was successful** message displays.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678011352057/a5a4095e-dbd2-4e11-bd34-978824d04417.png align="center")

# Step 3 — Adding Python to the Environment Variables (optional)

Skip this step if you selected **Add Python to environment variables** during installation.

If you want to access Python through the command line but you didn’t add Python to your environment variables during installation, then you can still do it manually.

Before you start, locate the Python installation directory on your system. The following directories are examples of the default directory paths:

* `C:\Program Files\Python310`: if you selected **Install for all users** during installation, then the directory will be system wide
    
* `C:\Users\Devismita Sahoo\Python310`: if you didn’t select **Install for all users** during installation, then the directory will be in the Windows user path
    

Note that the folder name will be different if you installed a different version, but will still start with `Python`.

1. Go to **Start** and enter `advanced system settings` in the search bar.
    
2. Click **View advanced system settings**.
    
3. In the **System Properties** dialog, click the **Advanced** tab and then click **Environment Variables**.
    
4. Depending on your installation:
    
    * If you selected **Install for all users** during installation, select **Path** from the list of **System Variables** and click **Edit**.
        
    * If you didn’t select **Install for all users** during installation, select **Path** from the list of **User Variables** and click **Edit**.
        
5. Click **New** and enter the Python directory path, then click **OK** until all the dialogs are closed.
    

## Step 4 — Verify the Python Installation

You can verify whether the Python installation is successful either through the command line or through the Integrated Development Environment (IDLE) application, if you chose to install it.

Go to **Start** and enter `cmd` in the search bar. Click **Command Prompt**.

Enter the following command in the command prompt:

python --version

You can also check the version of Python by opening the IDLE application. Go to **Start** and enter `python` in the search bar and then click the IDLE app, for example **IDLE (Python 3.10 64-bit)**.

You can start coding in Python using IDLE or your preferred code editor.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678011600096/eacc0e46-ead1-40f9-a280-994e9165448d.png align="center")

### python install on Ubuntu:-

To complete this tutorial, you should have a non-root user with `sudo` privileges on an Ubuntu 20.04 server. To learn how to achieve this setup, follow our [initial server setup guide](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04).

If you’re not already familiar with a terminal environment, you may find the article [An Introduction to the Linux Terminal](https://www.digitalocean.com/community/tutorials/an-introduction-to-the-linux-terminal) useful for becoming better oriented with the terminal.

## Step 1 — Setting Up Python 3

1. sudo apt update
    
2. sudo apt -y upgrade
    
    The `-y` flag will confirm that we are agreeing for all items to be installed, but depending on your version of Linux, you may need to confirm additional prompts as your system updates and upgrades.
    
    Once the process is complete, we can check the version of Python 3 that is installed in the system by typing:
    
3. python3 -V
    

You’ll receive output in the terminal window that will let you know the version number. While this number may vary, the output will be similar to this:

output:

Python 3.8.10

1. To manage software packages for Python, let’s install **pip**, a tool that will install and manage programming packages we may want to use in our development projects. You can learn more about modules or packages that you can install with pip by reading [How To Import Modules in Python 3](https://www.digitalocean.com/community/tutorials/how-to-import-modules-in-python-3).
    
    sudo apt install -y python3-pip
    
2. Python packages can be installed by typing:
    
    pip3 install | package name
    
3. Here, `package_name` can refer to any Python package or library, such as Django for web development or NumPy for scientific computing. So if you would like to install NumPy, you can do so with the command `pip3 install numpy`.
    
    There are a few more packages and development tools to install to ensure that we have a robust setup for our programming environment:
    
    sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
    

### Read about different Data Types in Python.

Data types are the classification or categorization of data items. It represents the kind of value that tells what operations can be performed on a particular data. Since everything is an object in Python programming, data types are classes and variables are instances (object) of these classes.

Following are the standard or built-in data types of Python:

* [**Numeric**](https://www.geeksforgeeks.org/python-data-types/#numeric)
    
* [**Sequence Type**](https://www.geeksforgeeks.org/python-data-types/#Sequence)
    
* [**Boolean**](https://www.geeksforgeeks.org/python-data-types/#boolean)
    
* [**Set**](https://www.geeksforgeeks.org/python-data-types/#set)
    
* [**Dictionary**](https://www.geeksforgeeks.org/python-data-types/#dictionary)
    

# Numeric

In Python, numeric data type represents the data that has a numeric value. Numeric values can be integers, floating numbers or even complex numbers. These values are defined as `int`, `float` and `complex` class in Python.

* **Integers** – This value is represented by int class. It contains positive or negative whole numbers (without fraction or decimals). In Python, there is no limit to how long an integer value can be.
    
* **Float** – This value is represented by the float class. It is a real number with a floating-point representation. It is specified by a decimal point. Optionally, the character e or E followed by a positive or negative integer may be appended to specify scientific notation.
    
* **Complex Numbers** – Complex number is represented by a complex class. It is specified as *(real part) + (imaginary part)j*. For example – 2+3j
    

# Sequence Type

In Python, the sequence is the ordered collection of similar or different data types. Sequences allow storing of multiple values in an organized and efficient fashion. There are several sequence types in

* [**String**](https://www.geeksforgeeks.org/python-data-types/#string)
    
* [**List**](https://www.geeksforgeeks.org/python-data-types/#list)
    
* [**Tuple**](https://www.geeksforgeeks.org/python-data-types/#tuple)
    

## String

In Python, [**Strings**](https://www.geeksforgeeks.org/python-strings/) are arrays of bytes representing Unicode characters. A string is a collection of one or more characters put in a single quote, double-quote or triple-quote. In python there is no character data type, a character is a string of length one. It is represented by an `str` class.

## List

[**Lists**](https://www.geeksforgeeks.org/python-list/) are just like arrays, declared in other languages which is an ordered collection of data. It is very flexible as the items in a list do not need to be of the same type.

## Tuple

Just like a list, a [**tuple**](https://www.geeksforgeeks.org/python-tuples/) is also an ordered collection of Python objects. The only difference between a tuple and a list is that tuples are immutable i.e. tuples cannot be modified after it is created. It is represented by `tuple` class.

Data type with one of the two built-in values, `True` or `False`. Boolean objects that are equal to True are truthy (true), and those equal to False are falsy (false). But non-Boolean objects can be evaluated in a Boolean context as well and determined to be true or false. It is denoted by the class `bool`.

# Dictionary

[**A dictionary**](https://www.geeksforgeeks.org/python-dictionary/) in Python is an unordered collection of data values, used to store data values like a map, unlike other Data Types that hold only a single value as an element, a Dictionary holds a `key: value` pair. Key-value is provided in the dictionary to make it more optimized. Each key-value pair in a Dictionary is separated by a colon: whereas each key is separated by a ‘comma’.

#### Creating Dictionary

In Python, a Dictionary can be created by placing a sequence of elements within curly `{}` braces, separated by ‘comma’. Values in a dictionary can be of any datatype and can be duplicated, whereas keys can’t be repeated and must be immutable. The dictionary can also be created by the built-in function `dict()`. An empty dictionary can be created by just placing it in curly braces{}.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678012912346/436a3b44-d291-48e3-adb6-e3ada38cdec1.png align="center")

These are some basic installation guides and datatypes in python.