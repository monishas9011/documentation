---
title: Bot logs
sidebar_label: Bot logs
tags: [bot logs, debug logs]
---

Logs in bot conversations are step-by-step records, detailing events and flows at the backend, important for identifying errors, understanding user interactions, and optimizing performance. They assist in diagnostics, illustrate user flows, and are crucial for testing and continuous development improvements.

The logs are accessible in real-time for **Sandbox** and **Staging** directly from the ongoing conversation. For **Production**, it will be available 15 minutes after the conversation ends.

## Check logs in Sandbox/Staging

To check the debug logs in Sandbox and Staging environments,

1. Go to **Studio** > **Build** and click the respective flow.

   ![](https://i.imgur.com/olJfQZF.png)

2. Click **Preview** and click the **bug icon** on the right corner.

   ![](https://i.imgur.com/rgyNgsQ.png)
   
3. Under **Console**, you can see the time at which the particluar action occured. Click **Refresh** to reload the logs.

    
    <img src="https://i.imgur.com/Hwpr3rP.png" alt="drawing" width="110%"/>
 
### View logs
 
If you hover over each timestamp, you can see the option to view the logs. 

  <img src="https://i.imgur.com/259rVvm.png" alt="drawing" width="110%"/>

----  
 
Click the logs icon to view the logs.

  <img src="https://i.imgur.com/79AiOTr.png" alt="drawing" width="60%"/>

### View node

If you hover over each timestamp, you can see the option to go to the respective node where the specific action occured. 

 ![](https://i.imgur.com/ay93P3J.png)
 
## Check logs in Production

To check the debug logs in Production:

1. Go to **Studio** > **Analysis** > **Conversation logs** > click the preferred conversation.

   ![](https://i.imgur.com/zxl0njk.png)

2. If you hover over each timestamp, you can see the options to [view the logs](#view-logs) and [the node which was involved in that action](#view-node).

   ![](https://i.imgur.com/4mzoe11.png)