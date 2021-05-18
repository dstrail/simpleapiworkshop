---
title: "AWS Workshop Portal"
chapter: false
weight: 12
---

### Running the workshop at an AWS Event

{{% notice warning %}}
Only complete this section if you are at an AWS hosted event (such as re:Invent,
Kubecon, Immersion Day, or any other event hosted by an AWS employee). If you are running the workshop on your own, go to:
[Self Hosted Event](../self_hosted/).
{{% /notice %}}

#### Login to AWS Workshop Portal:

This workshop uses an AWS account and a Cloud9 environment. You will need the **Participant Hash** provided upon entry, and your email address to track your unique session.

Connect to the portal by browsing to [https://dashboard.eventengine.run/](https://dashboard.eventengine.run/). The following screen shows up.



![Event Engine](/images/event-engine-initial-screen.png)

Enter the provided hash in the text box. The button on the bottom right corner changes to **Accept Terms & Login**. Click on that button to continue and autheniticate.

Choose to Authenticate with OTP
![Authentication](/images/sign-in-otp.png)
Enter your email address and check your email for your One Time Password.
After you have successfully authenticated you will see the **Event Dashboard**.

![Event Engine Dashboard](/images/event-dashboard.png)
Click on **Set Team Name** and enter your name.
![Enter your name](/images/set-team-name.png)


Take note of the AWS region to use.
Click on **Open AWS Console** on dashboard.


![Event Engine AWS Console](/images/open-console.png)

Take the defaults and click on **Open AWS Console**. This will open AWS Console in a new browser tab.



![AWS Console](/images/console.png)
The menu on the top right of your window will show which [AWS Region](https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints) your are using. 

{{% notice warning %}}
If you are already logged into a different AWS account you will be prompted to log out. Click the [here](https://signin.aws.amazon.com/oauth?Action=logout&redirect_uri=aws.amazon.com) link.

![Already logged in](/images/logout-before-logging-in.png)
Once logged out please close this page and go back to previous step.
{{% /notice %}}

Once you have completed the step above, you can head straight to [Create a DynamoDB table](/010_createadynamodbtable/)