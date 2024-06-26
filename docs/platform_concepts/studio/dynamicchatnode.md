---
title: Dynamic chat node
sidebar_label: Dynamic chat node
---

:::note
This node is activated only upon request.
:::

The dynamic chat node simplifies conversation design by eliminating the need for building nodes or designing flows. You can directly type the instructions for the node, an d the bot will automatically execute them. This saves time since you don't have to create complex flows or add multiple nodes. Just type the instructions, and the bot will handle the conversation accordingly.

You can also add additional nodes to dynamic node to build the rest of the flow.

## Prompts for Dynamic chat node

There are two ways by which you can enter your prompts. They are:

### Generate prompts with AI Prompt Generator

1. [Build a flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys) for your use case and extend the node where you want to include the **Dynamic chat** node. Under **Prompts** click **Dynamic chat** node.

   <img src="https://i.imgur.com/RE9I5Jr.png" alt="drawing" width="70%"/>

2. Once you click the dynamic node, the **AI prompt generator** opens up. 

   <img src="https://i.imgur.com/QaVQe8Q.png" alt="drawing" width="70%"/>

3. Fill in the following fields and click **Generate** and the platform will automatically genrate a prompt for you.

   <img src="https://i.imgur.com/LWgYCmX.png" alt="drawing" width="70%"/>

* **Write goal**: Define the conversation's primary objective.
* **Write usecase:** Specify the topics or scenarios the conversation will cover.
* **Describe fallback:** Explain the action the bot should take if it doesn't understand the user's input.
* **Add input:** List the information the bot needs to collect from the user.

4. Once the prompt gets generated, you can click **Add prompt** to add it. If you'd like to further improvise the prompt, click **Improve prompt**.
   
   <img src="https://i.imgur.com/DwdHQVj.png" alt="drawing" width="70%"/>

5. Select the additional prompts to be added, enter the details to be collected for those prompts and click **Regenerate**.
   
    <img src="https://i.imgur.com/U0UXKVH.png" alt="drawing" width="70%"/>

### Write your own prompts

1. [Build a flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys) for your use case and extend the node where you want to include the **Dynamic chat** node. Under **Prompts** click **Dynamic chat** node.

   <img src="https://i.imgur.com/RE9I5Jr.png" alt="drawing" width="70%"/>

2. Once you click the dynamic node, the **AI prompt generator** opens up. 

   <img src="https://i.imgur.com/QaVQe8Q.png" alt="drawing" width="70%"/>

3. Click **Cancel** on the pop-up and enter your prompt.


![](https://i.postimg.cc/tRPy357r/Screenshot-2024-03-21-at-8-14-56-PM.png)

| Fields             | Descriptions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| User context       | User context allows you to store string values as variables, which can be retrieved anywhere within the context using {{userContext}}. <br/> For example, if you want to offer a discount of 35%, you can store it as a string variable and utilize {{userContext}} to retrieve this information within the context. <br/>Similarly, User context can be used to fetch and display data to the end user at any point in the conversation. It's important to note that only one User context can be used in a single conversation. |
| Send initial user message | Sends the user messages from the conversation with the bot to the dynamic chat node before the flow control transitions to the dynamic chat node.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Send message after chat ends | The last message sent to the user when the conversation ends with the dynamic chat node.                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Goal               | In this field, you describe the objective of the bot. To indicate the start of the context and instruct the bot to follow the given instructions, you enter **START CONTEXT**. Similarly, to indicate the end of the instructions, you enter **END CONTEXT**. <br/>You can define any desired actions for the node, such as greeting the user, collecting their information, verifying the entered details, and more. This allows you to tailor the behavior and actions of the node based on your specific needs.            |



 **Points to remember while describing a goal**

1. **Begin the prompt with clear instructions, separating the instruction and context using ### or """.**

   * **Wrong** ❌: Summarize the text below as a bullet point list of the most important points.
   * **Correct** ✅:  Summarize the text below as a bullet point list of the most important points.

     """
     {text input here}
     """

2. **Provide specific, descriptive, and detailed requirements regarding the desired context, outcome, length, format, style, etc.**

   * **Wrong** ❌: Write a poem about OpenAI. 
   * **Correct** ✅: Write a short inspiring poem about OpenAI, focusing on the recent DALL-E product launch (DALL-E is a text to image ML model) in the style of a {famous poet}

3. **Minimize the use of vague and imprecise descriptions.**

   * **Wrong** ❌: The description for this product should be fairly short, a few sentences only, and not too much more.
   * **Correct** ✅: Use a 3 to 5 sentence paragraph to describe this product.

4. **Include relevant details in your query to ensure more accurate and pertinent answers.**

   * **Wrong** ❌: How do I add numbers in Excel?
   * **Correct** ✅: How do I add up a row of dollar amounts in Excel? I want to do this automatically for a whole sheet of rows with all the totals ending up on the right in a column called "Total".

5. **Articulate the desired output format through examples**

   * **Wrong** ❌: Extract the entities mentioned in the text below. Extract the following 4 entity types: company names, people names, specific topics and themes.
   * **Correct** ✅:Extract the important entities mentioned in the text below. First extract all company names, then extract all people names, then extract specific topics which fit the content and finally extract general overarching themes

   Desired format:
   Company names: <comma_separated_list_of_company_names>
   People names: 
   Specific topics:
   General themes:

6. **Instead of just saying what not to do, say what to do instead**

   * **Wrong** ❌: The following is a conversation between an Agent and a Customer. DO NOT ASK USERNAME OR PASSWORD. DO NOT REPEAT.
   * **Correct** ✅:The following is a conversation between an Agent and a Customer. The agent will attempt to diagnose the problem and suggest a solution, whilst refraining from asking any questions related to PII. Instead of asking for PII, such as username or password, refer the user to the help article www.samplewebsite.com/help/faq

## Save and restore versions of prompt

If you're working on a prompt and think your input is stable, you can save the current version as a backup. This way, you can easily go back to a previous version if needed. The published prompt will also have a separate tag, making it easy to restore to the last stable version.

This action is possible only in Sandbox/Developement modes.

1. Click the **floppy disk icon** to save the prompt.

   <img src="https://i.imgur.com/sZnTiqu.png" alt="drawing" width="70%"/>

2. Whenever you want to restore the prompt, click the **restore** icon.

   <img src="https://i.imgur.com/AEnmwwk.png" alt="drawing" width="70%"/>

3. Choose the version of the prompt to be restored, and click **Restore**.

   <img src="https://i.imgur.com/rQ89iFe.png" alt="drawing" width="70%"/>

## Input list

The **Input list** allows you to store the specific details of the input that need to be collected from the user.

 <img src="https://i.imgur.com/02bpLM1.png" alt="drawing" width="70%"/>

1. Click **+ Add another input**.

   <img src="https://i.imgur.com/ZaWHvc1.png" alt="drawing" width="60%"/>

2. In **Input name**, enter the name of the input to be collected.
3. In **Store response in**, choose or create a variable in which the collected information should be stored.
4. Select **Mark as optional** to indicate if the collected information is optional, allowing for the possibility of it being collected or not.
5. Select **Mask input** to conceal the input collected from the user and this input will be concealed in the conversation logs as well.
6. Enable **Add input details**(optional) to enter a sample format for the input to be collected.
7. In **Regex for validation** specify the desired format for validation.
8. In **Examples of expected input**, provide a sample of the expected input to align with the defined format.
9. Click **Add**.

## Failure setting

In the **Failure setting** you can specify the messages to be shown when the bot takes too long to respond, set the desired response time and maximum limit for conversations.

 <img src="https://i.imgur.com/CxgtfNa.png" alt="drawing" width="75%"/>

Enable **Enable retries** for the bot to show a maximum of two failure messages after which it will switch to fallback flow.

In **Configure timeout time**, you can set the exact duration after which the bot should time out.

In **Max limit of conversations**, set the limit beyond which the bot will move to fallback if the conversation is still not over.

You can easily determine the reasons behind failure/timeout messages through tags. If the tags are related to APIs or the LLM vendor, please reach out to the respective third-party vendor or check their status for assistance. If the tags are bot-level, you can manage the configurations within your node. And if the tags are platform-level, please contact us. 

 ![](https://i.imgur.com/eLFqeIy.png)

You can find these tags in two places:

1. **Production bots and past conversations:** 

 Navigate to **Studio > Analysis > Conversation Logs**. 
 
 ![](https://i.imgur.com/9f4n0kp.png)
 
 You can also use the filter to search for conversations based on these tags and take appropriate actions.

 ![](https://i.imgur.com/4UcH7qy.png)

2. **Debug logs:**

 For continuous and replicable errors, you can find additional information in the debug logs within the Preview section, as well as in the conversation logs (highlighted in orange).

 <img src="https://i.imgur.com/hbmBquG.png" alt="drawing" width="35%"/>

## Skill configuration

In **Skill configuration**, you can call workflows (skills). Skill is a flow built using [Action nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes) and [Logic nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes) to perform a certain action. You can build a skill to hit APIs, update databases, execute custom logic, etc. This extends the bot's capability of handling dynamic data.

1. Go to **Build** > **Create flow** > **+ Create skill** and create a flow to execute certain actions. 

   <img src="https://i.imgur.com/rJQw0ny.png" alt="drawing" width="90%"/>


2. Once you're done, click **Skill configuration** and enable **Enable skill**.

   <img src="https://i.imgur.com/LtNyMPH.png" alt="drawing" width="90%"/>

3. Fill the following fields:

   <img src="https://i.imgur.com/AB1XU3r.png" alt="drawing" width="90%"/>

* **Skill**: Choose the skill to be utilized by the Dynamic Chat node. 
* **Input to skill**: Choose the variable that holds the input for the skill..
* **Output from skill**: Choose the variable where you want to save the outcome of the skill.

4. Click **+ Link more skill** to add more skills.

## Goal configuration setting

In **Goal configuration setting**, you can set the temperature, maximum length and top P of the bot.

 <img src="https://i.imgur.com/P9I2g2m.png" alt="drawing" width="80%"/>

* **Temperature:** Temperature controls the randomness of generated text. Higher values result in more diverse outputs, while lower values make the output more focused.
Example (high temperature, 1.0): The sky is blue, the grass is purple, and the trees dance with delight.
Example (low temperature, 0.5): The sky is clear and the grass is green.

* **Maximum length:** Maximum length sets a limit on the length of generated text, preventing excessively long or incomplete outputs.
Example (maximum length of 50 tokens): "The quick brown fox jumps over the lazy dog."
Example (maximum length of 140 characters): "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."

* **Top P:** Top P, or nucleus sampling, is a technique where a probability threshold is set, and only the most probable words surpassing this threshold are considered for text generation. It can be used in various scenarios with the following recommendations:

   **Controlling creativity:** Lower the threshold (e.g., p = 0.1) for conservative and predictable responses. For example, generating technical documentation or providing factual information.

  **Promoting diversity:** Increase the threshold (e.g., p = 0.9) to encourage more varied and imaginative responses. For example, generating creative writing prompts or brainstorming ideas for fiction.

  **Balancing creativity and coherence:** Use a moderate threshold (e.g., p = 0.5) to strike a balance between controlled output and promoting creative alternatives. Example: Generating marketing taglines or social media posts.
  
## Model configuration

Within the model configuration, you have the freedom to manually input your own custom GPT or LLM credentials into the bot. You can then use various models on different dynamic nodes within the same bot independently. This grants you the flexibility to conduct extensive experiments.

<img src="https://i.imgur.com/x3N9gOh.png" alt="drawing" width="70%"/>

To add custom LLM,

1. Click **+ Add account**.

<img src="https://i.imgur.com/ByrrXBQ.png" alt="drawing" width="70%%"/>

2. Fill in the following fields:

* **Give account name:** Provide a name to your LLM account.
* **LLM Provider:** Choose your LLM provider.

   ![](https://i.imgur.com/UXsaPcu.png)

3. Click **Connect**.
4. Then go to the node > **Model configuration** > choose **Model**.

 <img src="https://i.imgur.com/A5sQmyZ.png" alt="drawing" width="70%%"/>
-----

## Voice configuration

Voice configuration lets you create interactive voice-enabled interactions, further enhancing the conversational capabilities of your bot.

  <img src="https://i.imgur.com/m7mnIM3.png" alt="drawing" width="70%%"/>

:::note
**Acknowledgment Message** field will soon be removed from the UI.
:::

Fill in the following fields:

| Feature         | Description                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------|
| Wait Music      | Upload music to play while the bot generates a response. Music must be in MP3 or WAV format, with a max size of 15 MB. |
| Preview Audio   | Review the uploaded audio file, adjust volume and playback speed, and listen to a preview before finalizing settings.  |


 <img src="https://i.imgur.com/1gy4RKn.png" alt="drawing" width="100%%"/>




 


