
# **Basic Conversation**
IBM Watson® Conversation is a question-and-answer system that provides a dialog interaction between the conversation system and users. This style of interaction is commonly called a chatbot.

![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/1.png)


# **Building the Conversation**

**Requirements:**

IBM Cloud account https://ibm.biz/BdZYZx

**1-  Create an instance of Watson Conversation on IBM Cloud**
Make sure that you are logged in to your IBM Cloud account. Click **Catalog** and then click **Services > Watson > Conversation> choose a name> hit Create**

**2-Click Launch tool to open the Watson Conversation workspace**

**3-Create a Workspace.**

**4-Add intents.**

An intent is a group of examples of things that a user might say to communicate a specific goal or idea. To identify intents, start with something that a user might want and then list the ways that the user might describe it.


**5-Create a new intent.**

For each intent, add examples to train the conversation for intent recognition.
![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/2.png)

**5-Test your intent.**
As soon as you create an intent, you can test it by clicking Ask Watson icon in the top, right-hand side of the conversation editor.
![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/3.1.PNG)

**6-Create Your Entity**
entity is a portion of the user's input that you can use to provide a different response to a particular intent.
Click Entities. On the Entities page, click Create new.

Each entity definition includes a set of specific entity values that can be used to trigger different responses. Each value can have multiple synonyms that define different ways that the same value can be specified in user input.

![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/3.2.PNG)

Create entities to represent to the application what the user wants to access.     
Fuzzy logic is a feature that allows Watson Conversation to accept misspelled words. You can enable this feature at the entity level.

**7-Building the Dialog**
A dialog is made up of nodes that define steps in the conversation.

![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/3.png)

In the previous image, two dialog nodes are shown. The first node is the standard welcome message. The other node is a catch-all node named "Anything else." Dialog nodes are chained in a tree structure to create an interactive conversation with the user. The evaluation starts at the top, so the welcome node is assessed before the "Anything else" node.

If you click the welcome node, the standard Watson response is "Hello. How can I help you?" To validate how the flow works, you can click the Ask Watson icon.


**8-Define Greeting Node**

The first node addresses greetings in a response to a query such as "hello." Click the welcome node and click Add node below

![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/4.png)

A new node is added between the welcome and "Anything else" nodes.

At each node level, you can expand the conversation by adding nodes. If you add nodes at the same level, the flows are parallel. Adding a child node creates a dependent track of conversation, and the conversation branches out into a tree structure.

Name the new node Handle Greetings. In the If bot recognizes field, change the value to #Greetings. The number sign (#) represents a prefix for intent. The condition is triggered when the Watson natural language classifier classifies the query as a greeting intent.

**9-Add Response **

![](https://github.com/nailahDev/Watson-chatbot/blob/master/Basic-Conversation-master/views/Chatbot-tutorial-pictures/5.png)

The previous image also illustrates how to use the multiple responses pattern to avoid being repetitive. The bot can present different answers to the same query. You can allow the system to randomly select an answer from the list of potential responses.


**10- Test your bot by clicking Ask Watson icon **

## Web Application Template for Watson Conversation API Demonstration

**Requirements:**
1. Install Nodejs http://blog.teamtreehouse.com/install-node-js-npm-windows

**Main steps:**
1. **"Clone or Download"**  this Repository
2. Take note of Watson Conversation Service's **Credentials** and **workspace_id**
3. Edit the file **app.js** and fill the fields: *username*, *<password>* and *<workspace_id>* with the data collected in the last step.
```css
var conversation = watson.conversation({
  username:"<username>",//replace with the username from service credential
  password:"<password>",//replace with the password from service credential
  version: 'v1',
  version_date: '2016-07-11'
});
```
4. Get the workspace ID
[workspace!]();

```css
     var workspace = "<workspace_id>"; //replace with the workspace_id from service credential

```


5.Open a terminal and Change the directory where you saved your code
write the command

```css
cd C:\Users\Desktop\...;

```
