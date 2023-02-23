---
title:  Design conversations for voice bots  
sidebar_label : Design conversations for voice bots  
---



**Design** module on the [yellow.ai](https://cloud.yellow.ai) platform allows you to design a bot without needing to learn all the platform aspects prior. You can input text as required to create a conversation between the bot and the user. Flows are built automatically on the Studio module.

You can design multiple flows on the conversation design module, Once they are converted into flows, you can train, test, preview, and publish the bot.

In this article, you will learn how to use the conversation design to build **voice bots**. 

-----------


To build a voice bot using designer, follow the steps below: 

## 1. Create a new bot 

> If you are a new user, refer to [this](https://docs.yellow.ai/docs/platform_concepts/Getting%20Started/account-setup) article. 


1. [Log in](https://cloud.yellow.ai) to your account and click **+Create new bot**.

    ![](https://i.imgur.com/wAbVsH9.png)

2. Select **Create from scratch**. 

    ![](https://i.imgur.com/0LG3d7y.png)

3. Enter these details: 
    - **Subscription**: Select the **subscription** under which you want to create this bot.
    - **Bot type**: Choose **Voice bot**. 
    - **Avatar**: Choose/upload an avatar (your bots display photo).
    - **Industry**: Select from the dropdown. 
    - **Region**: Select from the dropdown.
    - Select **Add live chat support to your bot** if you want to add a customer support flow.

4. Click **Create bot**. 

    ![](https://i.imgur.com/u2UEI56.png)

5. From the Overview switcher, select **Design**. 

    <img src="https://i.imgur.com/AcKCNyw.png" alt="drawing" width="70%"/>

-------

## 2. Design chat conversations 

> - **Home** flow is the main flow from where the conversation starts(you can rename/delete/add it as fallback). This can be followed by other flows. 
> - All the messages are trained as text. You cannot add buttons or other chat-design options. 

**Demo**:

![](https://i.imgur.com/rqP9Cp7.gif)

- **Dialog box**: You can add a bot and user conversation here. The name of the dialogue box can be changed by clicking the pencil icon on top.
- **Bot says**: Add the questions you want the bot to ask. Ex: Hey! What is your name? 
- **Use variables**: Add [variables](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#31-create-a-variable-via-nodes) to the conversation to display the stored user data.
- **User says**: Add the questions you are expecting from the bot user. Example: My name is Karan. I want to enquire about my bank balance. 
- **Store response in**: Add [variables](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#31-create-a-variable-via-nodes) to store the responses in a variable. Choose an existing variable or click **+Add new variable**. Example: Store customers name in First name variable. 
- **Fallback**: Message from the bot's side when the bot is unable to provide the solution/ understand the user's query. Example: I did not get your name, can you please repeat? 
- **Create flow**: Click **+ Create flow** to create a new flow. 

    <img src="https://i.imgur.com/GplCpZt.png" alt="drawing" width="100%"/>

- **Add components**: Click **+** and connect this dialogue to a new **flow/dialogue/condition**.

    ![](https://i.imgur.com/lORvCQ3.png)



:::note
For guidelines to build a good conversation, click [here](https://docs.yellow.ai/docs/cookbooks/getting_started). 
:::

--------

## 3. Configure global/node-level settings and preview

While creating flows manually, for each of these nodes, you had to enter the text in Speech synthesis markup language(SSML) format and configure further using [Tools](https://docs.yellow.ai/docs/platform_concepts/studio/tools#25-voice) or [Node settings](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes#32-configure-node-for-a-voice-bot). 

With the conversation designer, you can design natural voice conversations by auto-generating SSML tags from voice effects such as emphasis, pronunciation, pause, etc.

### 3.1 Bot persona settings(Global settings)

- Click the **Settings** button on the top-right of the screen. Changes made in Bot persona settings will apply to all the nodes. 
    - **Language**: Select the language you want the bot to speak. 
    - **Voice**: Voices available are listed in the dropdown, select your preferred voice.  
    - **Pitch/Speed/Volume**: Place the cursor on the number you want to select. 

- Click **Save**. 

    ![](https://i.imgur.com/QCSgznC.png)

--------

### 3.2 Node level settings

- Double-click on the entered text (bot says).
    - **Emphasis**: Select a text from the entered sentence and emphasize that word (**low, medium, high**). If you select **Off**, emphasis applied by default will detain. 
    <img src="https://i.imgur.com/pp9id0a.png" alt="drawing" width="70%"/>     
    
    - **Pause**: You can add pauses (delays) between words/sentences. 
     <img src="https://i.imgur.com/RwtNLlj.png" alt="drawing" width="70%"/>    

    - **Music**: You can add .mp3 or .wav music files, that can get played during the conversation.
    <img src="https://i.imgur.com/AqLhpza.png" alt="drawing" width="70%"/>    
    
    - **Interpret**: It can be used to interpret a word in a particular format. 
     <img src="https://i.imgur.com/IBRZqiG.png" alt="drawing" width="70%"/>    
     
<!--
     
| Value | Meaning |
| -------- | -------- |
| Off     | TBA     |
|Spell out||
|Cardinal ||
|Ordinal||
|Number_di||
|Date||
|Time||
|Duration||
|Telephone||
|Currency ||
|Address||
|Name||

-->

- Click **Preview** in the dialogue box and understand how the bot sounds after configuring it. 

    <img src="https://i.imgur.com/LlclIW4.png" alt="drawing" width="80%"/>      


--------

### 3.3 Voice bot demo(Receive a live call)

> This demo is accessible if your bot is connected with Interactive Voice Response (IVR). Click [here](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/Ivr) for more details. 


1. Click **Preview** at the top-right of your screen. 

     <img src="https://i.imgur.com/r1b7Mqb.png" alt="drawing" width="70%"/>    

2. Enter your phone number. Verify your OTP. 

    <img src="https://i.imgur.com/n0440Ru.png" alt="drawing" width="40%"/>
    
3. Click **Call**. You will receive a phone call to the entered number. You can have a conversation with the bot and experience its behavior. 




-----

## 4. Share designs 

Share designs with others within the platform to quickly close the feedback loop

<img src="https://i.imgur.com/rdyRDoh.png" alt="drawing" width="80%"/>




-------


## 5. Sync conversation flows to studio and deploy

With bi-directional auto-sync between **Conversation design** and **Studio > Flows**, the information on the design module will be available as flows(and vice versa).

1. From the overview switcher, select **Studio>Flows**. 
2. If you want to add a welcome message or change the flow from which the bot conversation starts, click **Welcome message** on the conversation settings section and edit it. 

    ![](https://i.imgur.com/zv58neq.png)

2. You can click on the created flows to edit and test them. 

    ![](https://i.imgur.com/v0dgTFm.png)

4. Click **Publish changes** to [publish](https://docs.yellow.ai/docs/platform_concepts/studio/test-and-publish-bot/modes) the bot. Once approved, your voice bot will be live and ready to handle calls. 


