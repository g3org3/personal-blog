---
title: "How to create an Alexa Skill with AWS"
pubDate: "Jun 25, 2017"
heroImage: "https://images.unsplash.com/photo-1512446733611-9099a758e5e5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
---

We are going to make an Alexa Skill, Serverless with node, that tells you how many github followers you have.

## Alexa Skill - get gh followers

create your account @ https://developer.amazon.com remember that this account must be the same as the one you enter on your Alexa app in order to test our own Alexa Skills without publish them.

Once you login and see the dashboard click the ALEXA option to begin

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*i8Ug0mNjpDUHusx6d3YoHA.png)

Click on Get Started on Alexa Skills Kit!

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*WK7l-YyIKNK5XMyCfr_R6g.png)

Here you will see all the skills you have created, go to the right and click add a new skill

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*1wRpDiaI-TR7htipPGZ_NA.png)

Let's fill out the app's info… the name and the invocation name doesn't need to be the same, the Name is how it is displayed in the "skills store" and the invocation name is how to actually call to app.

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*piFcFn_X_-JcetNxkbYJcw.png)

## Defining Schema

This is where you defines all the intents the skill will have, for now we'll keep it simple and only add 1 intent. It is important that your intent name is PascalCase.

![image](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*zWwpIdV1IsLHXHW3-W3mxg.png)

We'll leave the custom slot types empty for now.

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*h4C9syxCliwObdP5FJF5Tg.png)

We'll add some sample utterances that Alexa needs to now how the user will ask for the intent so the convention is NameOfIntent space and what the users might say to active the intent. All the utterances for all intents should be here. Then click NEXT!

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*UUbbqRxcnOe6uVC7swfp9w.png)

Under the Configuration select AWS Lambda ARN, for this tutorial we'll do a serverless solution. Click on the "More info about AWS Lambda"

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*DxQ39iwv4z8NCEMG3Az1PQ.png)

It will redirect you to the AWS site and there you can create your account or sign in if you already have one.

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*6-WEzQGjOe6-7nWXOW10gQ.png)

After you login you will see the dashboard, there are a ton of services so let's search for lambda

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*cfDnzgMKdmH-quIlqhCmkA.png)

Now create your first lambda function

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*5fTsFZzM_flzhULb-LtXqQ.png)

For our demo we'll choose the blank function to keep things simple and get the basics of a lambda function

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*Xw_2rUlURML8XS80-g4MSw.png)

Next you need to specify that it will be triggered by an Alexa Skill, click the first box and search by alexa and choose the Alexa Skills Kit

![image](https://miro.medium.com/v2/resize:fit:720/format:webp/1*ZVXbbhEf120iXZPJSw9kqA.png)

Remember to be able to see this you need to be in the US East (N. Virginia) or EU (Ireland) region.

Screenshot from Amazon support click the link/box below for more infoCreating an AWS Lambda Function for a Custom Skill - Amazon Apps & Services Developer Portal

*reference: [host a custom skill as an aws lambda function](https://developer.amazon.com/en-US/docs/alexa/custom-skills/host-a-custom-skill-as-an-aws-lambda-function.html)

Creating an AWS Lambda Function for a Custom Skill The easiest way to build the cloud-based service for a custom Alexa…developer.amazon.com

All set now click next

Let's fill the function info and set the runtime to nodejs 6

Here's an example code to get the basics on how you can create your first lambda function.

After you paste code scroll down to configure the role of this lambda function then click next

You will see the following info and proceed to create function

Congrats! you created your first lambda function. Now you will see your ARN at the top right, copy that long id and then click on the Alexa Developer portal link. We need to get back and finish the skill configuration with this ARN.

Go back to the configuration pane for your Alexa Skill choose AWS Lambda, Noth America and paste the ARN id

Then click NEXT

Wooot we are now ready to test our Alexa Skill, try it with your alexa device.

Post on [Medium](https://medium.com/@g3org3dev/how-to-create-your-first-alexa-skill-ed471270f872)
