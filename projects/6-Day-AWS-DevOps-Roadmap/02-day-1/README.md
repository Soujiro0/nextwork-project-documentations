<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Set Up a Web App in the Cloud

**Project Link:** [View Project](http://nextwork.ai/projects/aws-devops-vscode)

**Author:** Jerry Castrudes  
**Email:** castrudesjerry11@gmail.com

---

## Set Up a Web App Using AWS and VS Code

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_7a1de541)

---

## Introducing Today's Project!

In this project, I'm learning to build a CI/CD pipeline from scratch that automates the build and deployment of a web app.

This project is part one of a series of DevOps projects where I'm building a CI/CD pipeline! I'll be working on the next project the next day or later in my free time

I did this project because I want to learn basic DevOps specifically the CI/CD setup.

### Key tools and concepts

Services I used were Amazon EC2 (Elastic Compute Cloud) and AWS IAM.

Key concepts I learnt include VS Code, Remote - SSH Connection, Apache Maven & Java, Nano, and the first step of the CI/CD pipeline

### Project reflection

This project took me approximately 2 hours and 40 minutes. The most challenging part was connecting and configuring ssh config. It was most rewarding to connect my EC2 instance to my local machine using SSH

One thing I didn't expect in this project was I can manage my projects file from a EC2 instance using SSH connection and I can edit the files locally using VS Code connected to my instance

---

## Launching an EC2 instance

### What I did in this step

In this step, I will set up a home for my web app file because we want to run the web app in the cloud, we will use a virtual server to house our development work.

I started this project by launching an EC2 instance because I want to make a virtual computer to make a home for my web app files.

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_7852fbf3)

### I also enabled SSH

SSH is Secure Shell is a protocol used to make sure only authorized users can access a remote server. I enabled SSH so that I can access my EC2 instance with a secure connection; all data transferred is encrypted. This encryption makes SSH an ideal method for working with virtual servers.

### Key pairs

A key pair in EC2 is like the keys to your virtual computer. Just like you need a key to unlock and start your car, a key pair lets you securely access your EC2 instance.

### Downloaded key pair file

Once I set up my key pair, AWS automatically downloaded a new file to my local computer

---

## Set up VS Code

### What I did in this step

In this step, I will install VS Code because I use Visual Studio Code (VS Code) to connect with my instance, so I can create and edit my web app's code.

### What is VS Code?

Visual Studio Code is one of the most popular tools for creating and managing coding projects. You'll often hear people call VS Code an IDE (Integrated Development Environment), which means software that help you write and edit code. It's similar to how Microsoft Word or Google Docs help you write documents.

I installed VS Code to manage the code of my web app from my EC2 instance to my local machine.

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_53d05e68)

---

## My first terminal commands

A terminal is where you send instructions to your computer using text instead of clicks. The first command I ran for this project was cd ~\Desktop\DevOps to navigate to the key file

### Updating file permissions

I also updated my private key's permissions with
- /reset to remove all existing permissions so you start with a clean slate.
- /grant:r "YOURUSERNAME:R" gives only my account read access to the file.
- /inheritance:r stops the file from inheriting permissions from its parent folder, keeping it locked down.

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_9328ada1)

---

## SSH connection to EC2 instance

### What I did in this step

In this step, I will make a connection from my VS Code to my EC2 instance because once I connected to the instance, I can work now inside my EC2 instance to set up my web app

### Connecting to EC2

To connect to my EC2 instance, I ran the command

ssh -i <your .pem file path> ec2-user@<your Public DNS>

### This command required an IPv4 address

A server's IPV4 DNS is a public address for your EC2 server that the internet uses to find and connect to it. The local computer you're using to do this project will find and connect to your EC2 instance through this DNS address.

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_e3069dca)

---

## Maven & Java

### What I did in this step

In this step, I will install tools to help build Java web apps

### Why I'm using Maven

Apache Maven is a tool that helps developers build and organize Java software projects. It's also a package manager, which means it automatically downloads any external pieces of code your project depends on to work.

Maven is required in this project to help us set up all the necessary web files to create a web app structure.

### Why I'm using Java

Java is a popular programming language used to build different types of applications, from mobile apps to large enterprise systems.

Java is required in this project because if we don't install Java, we won't be able to use Maven to generate/build our web app.

---

## Create the Application

### What I did in this step

In this step, I will create a web application using Java and Maven

### Creating the Java web app

I generated a Java web app using the command

mvn archetype:generate -DgroupId=com.nextwork.app -DartifactId=nextwork-web-project -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false

-DartifactId=nextwork-web-project names your project
-DarchetypeArtifactId=maven-archetype-webapp specifies that you're creating a web application.
-DinteractiveMode=false runs the command without pausing for user input, so Maven will go ahead and install everything without waiting for your confirmation.


### Installing Remote - SSH

I installed Remote - SSH, which is an extension in VS Code that lets you connect directly via SSH to another computer securely over the internet. I installed it to let me use VS Code to work on files or run programs on that server as if I were doing it on my own computer

### SSH configuration details

Configuration details required to set up a remote connection include:

- Host and HostName should both match your EC2 instance's Public DNS.
- IdentityFile should be the path to your nextwork-keypair.pem file on your local computer.
- User should say ec2-user

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_2939cf01)

---

## Create the Application

### Exploring the project structure

Using VS Code's file explorer, I could see the web app files/folders

Two of the project folders created by Maven are src and webapp, which

The src (source) folder holds all the source code files that define how your web app looks and works.

src is further divided into webapp, which are the web app's files e.g. HTML, CSS, JavaScript, and JSP files, and resources, which are the configuration files a web app might need e.g. connection settings to a database.

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_45f91fd7)

---

## Using Remote - SSH

### What I did in this step

In this step, I will connect my VS Code itself to my EC2 instance, not just the terminal, because this will make it so much easier to edit and manage my web app.

### Updating the web app

index.jsp is a file used in Java web apps. It's similar to an HTML file because it contains markup to display web pages.

I edited index.jsp by modifying the content using the VS Code editor and saved it using Ctrl+S

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_7a1de541)

---

## Using nano

### Additional improvements

In this secret mission, I will edit the file using the terminal instead of an IDE

### Terminal vs IDE

An alternative to using IDEs is. terminal. To edit index.jsp, I ran the command nano index.jsp to open a text editor in the terminal

Compared to using an IDE, editing index.jsp in the terminal felt like a hacker vibe; I'd be more likely to use an IDE if I were editing multiple files

### Verifying my work

To verify my editing work in the terminal, I open my VS Code connected via SSH and see the file. It was possible to see my changes in VS Code right away because both are connected directly to my EC2 instance, so they are looking at it in real time

![Image](http://nextwork.ai/serene_navy_peaceful_jujube/uploads/aws-devops-vscode_a3324ad41)

---

---
