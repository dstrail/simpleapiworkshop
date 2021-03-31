+++
title = "Access to Cloud9"
chapter = false
weight = 79
+++

#### What is AWS Cloud9?

AWS Cloud9 is an integrated development environment, or IDE.

The AWS Cloud9 IDE offers a rich code-editing experience with support for several programming languages and runtime debuggers, and a built-in terminal. It contains a collection of tools that you use to code, build, run, test, and debug software, and helps you release software to the cloud.

You access the AWS Cloud9 IDE through a web browser. You can configure the IDE to your preferences. You can switch color themes, bind shortcut keys, enable programming language-specific syntax coloring and code formatting, and more.

The following diagram shows a high-level overview of how AWS Cloud9 works.

![** use the AWS Cloud9 IDE, running in a web browser on your local computer, to interact with your AWS Cloud9 environment **](/images/Cloud9-arch.png)

**Using the AWS Cloud9 IDE, you can:**

-   Store your project's files locally on the instance or server.
-   Clone a remote code repository—such as a repo in AWS CodeCommit—into your environment.
-   Work with a combination of local and cloned files in the environment.

...and today you will use it to deploy and test your API!

Connect to Cloud9 brwosing to [** Cloud9 **](https://console.aws.amazon.com/cloud9) 

In the console anter making sure you are in the right Region (top right) search for the button **Create environment** 

![**Click on the button create environment **](/images/cloud-9-create-environment.png)

Next: 

1. give a name to your instance

```bash 
    api-workshop
```
2. configure the options of your Cloud9 instance

![** choose your options **](/images/cloud-9-configure-settings.png)

3. review the options and Create!

After a few minutes...

![** cloud9 logo will show up **](/images/creating-cloud-9.png)

...your Cloud 9 environment!


Few more configuration steps then we can start:

1. close the Welcome Screen
![** close the welcome screen **](/images/cloud-9-close-welcome-screen.png)

2. prepare a terminal in full screen

![** click the x **](/images/cloud-9-open-new-terminal.png)

Your **teminal** in Cloud9 is **ready**! 

You will test your API from here:
![** Cloud9 terminal **](/images/cloud-9-terminal.png)


