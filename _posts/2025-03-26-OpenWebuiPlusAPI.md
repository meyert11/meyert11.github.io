---
layout: post
title: Add Experimental Models to your Open Webui
description: Make your local Open Webui even better by connecting it to free experimental models by Google/Facebook/OpenAI
date: 2025-03-29
tags: AI Gemini machine-learning local-models
categories: data-science AI
---

Kind of working backwards, as I setup the site, but I currently have an Open Webui hosted in my basement rig, where 2 rtx 3080s can run a bunch of modern models in a secure, private network. Google's new model, Gemini 2.5 experimental is getting a lot of hype so I thought - wouldn't it be nice if I could connect Open WebUI to the Google API, so on my phone, tablet or computers I can utilize the latest models... well it turns out it's super easy!

First - get your free API from google's AI Studio https://aistudio.google.com/apikey

## AI's suggestion

The first thing I did was search perplexity for a solution. It had me creating a litellm container, but the ports started to conflict with open-webui's ports. There were some work arounds, but I thought let's just give it a try manually. So I asked it if I already had an API key, can i connect to Google's api in open webui, and it gave 'almost' the right answer.

## Configuring Direct Connections

Open WebUI version: 0.5.20
There's a major disconnect between AI models and some of the github software, and open webui is a prime example. It will tell me how to traverse the admin panel and settings and sections just won't exist. For example it told me to go to Admin panel, connections and add a direct connection, however this area just had a toggle switch, nothing else.

So after exploring on my own, I found the solution:

1. After logging into to your user account, click on your icon in the upper right, then settings (not admin panel)

2. Click Connections, then the plus botton to add a new connection

3. For Google models, put this for the URL: https://generativelanguage.googleapis.com/v1beta

4. Then add your API key in the 'Key' section

The next step is critical, you HAVE to add the Model ID, and only 1 model will show up for each connection, so don't add more, only the top one works.

5. Click the Add a model ID plus sign, and type in exactly the model ID: eg gemini-2.5-pro-exp-03-25

Dont' worry about errors if you click 'verify connection' mine had errors too, but it still works.

6. Click Save, Save, then go back to New Chat and under models you'll see your model. if you don't see the model, try searching for it. Enjoy!!

Eventually I'll create a blog about creating the local Open WebUI in a proxmox environment, and give the updates for the new WebUI.