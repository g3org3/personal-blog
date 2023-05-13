---
title: "How to create an Alexa Skill with AWS"
pubDate: "Jun 25, 2017"
heroImage: "https://images.unsplash.com/photo-1512446733611-9099a758e5e5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
---

How to create your first Alexa skill?
We are going to make an Alexa Skill, Serverless with node, that tells you how many github followers you have.
Alexa Skill - get gh followers
create your account @ https://developer.amazon.com remember that this account must be the same as the one you enter on your Alexa app in order to test our own Alexa Skills without publish them.
Once you login and see the dashboard click the ALEXA option to begin
Click on Get Started on Alexa Skills Kit!
Here you will see all the skills you have created, go to the right and click add a new skill
Let's fill out the app's info… the name and the invocation name doesn't need to be the same, the Name is how it is displayed in the "skills store" and the invocation name is how to actually call to app.
Defining Schema
This is where you defines all the intents the skill will have, for now we'll keep it simple and only add 1 intent. It is important that your intent name is PascalCase.
We'll leave the custom slot types empty for now.
We'll add some sample utterances that Alexa needs to now how the user will ask for the intent so the convention is NameOfIntent space and what the users might say to active the intent. All the utterances for all intents should be here. Then click NEXT!
Under the Configuration select AWS Lambda ARN, for this tutorial we'll do a serverless solution. Click on the "More info about AWS Lambda"
It will redirect you to the AWS site and there you can create your account or sign in if you already have one.
After you login you will see the dashboard, there are a ton of services so let's search for lambda
Now create your first lambda function
For our demo we'll choose the blank function to keep things simple and get the basics of a lambda function
Next you need to specify that it will be triggered by an Alexa Skill, click the first box and search by alexa and choose the Alexa Skills Kit
Remember to be able to see this you need to be in the US East (N. Virginia) or EU (Ireland) region.
Screenshot from Amazon support click the link/box below for more infoCreating an AWS Lambda Function for a Custom Skill - Amazon Apps & Services Developer Portal
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

Post on Medium!
https://medium.com/@g3org3dev/how-to-create-your-first-alexa-skill-ed471270f872
