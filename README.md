# 🍕 AWS Lex Pizza Ordering Chatbot
A simple chatbot built on AWS Lex that allows users to order pizza and drinks. This demonstrates step-by-step how to create a conversational AI bot using AWS Lex, with natural language understanding powered by machine learning.

This project is perfect for beginners who want to get started with AWS chatbots, slot types, and intents.

# 🚀 Features
* Greeting Intent: Welcomes users and guides them on how to interact with the bot.
* Pizza Ordering Intent: Allows users to select pizza size and toppings.
* Drink Ordering Intent: Lets users select drinks and quantity.
* Slot Validation: Only allows predefined options for pizza sizes, toppings, and drinks.
* Confirmation & Fulfillment: Reads back the order to the user and confirms placement.
* Voice Support: Users can interact with the bot via text or speech (Alexa/voice-enabled devices).

# 🛠️ Prerequisites
* AWS Account
* Access to AWS Lex
* Basic understanding of chatbots and AWS console

# 📝 Step-by-Step Guide
A. Create a New Bot
1. Open AWS Console → Lex → Create Bot.
2. Give your bot a name: PizzaOrderingBot.
3. Select Create a basic bot and leave default settings.
4. Configure:
* Language: English (US)
* Voice: Joanna (or any preferred voice)
* Intent classification confidence threshold: 0.4
5. Click Done.

B. Create Intents

1. Greeting Intent

i. Go to Intents → Add Intent → Name: Greeting
ii. Sample Utterances:

      hi
      hello
      hey
iii. Closing Responses:

      Hi, welcome to the Amazing Pizza Store! My name is Joanna. I can help you with your pizza or drink orders. Which would you like to order?
iv. Add response variations if needed:

      Yo! Welcome to the shop, Joanna here. I'll help you place your order.
v. Save and Build Bot.
vi. Test: Type hi or hello → bot should respond correctly.


