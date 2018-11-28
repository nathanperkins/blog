---
title: Google Cloud computing solutions
date: 2018/11/10
categories:
- Software Engineering
- Backend
tags:
- Datastore
---
# Introduction

This short blog post will serve as an introduction to a series of posts I'll be doing on Google App Engine, Datastore and the G-Cloud suite. 

The G-Cloud suite is a product that Google offers which includes a number of APIs, NoSQL solutions, and cloud computing hosting options. I've been using it with personal projects and in my Cloud development class, and overall, I've enjoyed it. The main competetor here is Amazon Web Services and while I think AWS generally is the better product, there are some cool things G-Cloud is doing. Lets dive in.  

# Setup

First, here's a basic guide on how to set up G-Cloud on your local machine

1. [Sign up for G-Cloud](https://cloud.google.com/) - You can try G-Cloud for free. Usually you can also find some free credits online as well. Since you are using google's hardware in the "cloud", you have to pay for it. Most of my personal projects don't accrued more than a few dollars, but, depending on how many people use your app or visit your site, your milage will vary. 

2. [Install local dev tools](https://cloud.google.com/sdk/) - Once you have your account, go ahead and install the local SDK (software development kit). These local tools will be used to interface with Google Cloud and deploy your application.

3. [Go to the Console and create a project]() - This will take your through a few billing steps and configuration options (like where in the world should your app be hosted). 

Now that you have the basic set up ready to go for Google Cloud and a project set up from the Console, lets take a look at a few of their products and deployment options.

# App Engine

The Google App Engine is a cloud computing / web framework product that google offers. It enables you to deploy web applications or do scheduled cloud computing operations. Basically, any deployment needs that you might have, app engine is a good solution. Let's say you have this super simple Python Flask web app:

```python
from flask import Flask
app = Flask(__name__)
 
@app.route("/")
def test():
    return "Hello World!"
 
if __name__ == "__main__":
    app.run()
```

and you want to run it in the cloud with app engine. You'll need this basic app.yml file:

```yml
runtime: python3
threadsafe: true
```
and flask should handle the rest. These `.yml` files can get pretty complicated, but basically, they tell the environment (in this case, the app engine) what runtime environment and configurations this python app should be running in. Check out [this article](https://cloud.google.com/appengine/docs/flexible/nodejs/configuring-your-app-with-app-yaml) for some more logistics!

Once you have this working locally, you can deploy it using the google cloud SDK:

```bash
gcloud app deploy
```

The SDK will take you through some steps to get it deployed and running! 

# Google Datastore

# To Be Continued ...

If this has you curious, here's [a link]() to the Google Cloud documentation. Again, this is a huge platform, so you won't be able to digest all of it, but this will get you started if you have specific questions. 