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
Create a New Bot
1. Open AWS Console → Lex → Create Bot.
2. Give your bot a name: PizzaOrderingBot.
3. Select Create a basic bot and leave default settings.
4. Configure:
  * Language: English (US)
  * Voice: Joanna (or any preferred voice)
  * Intent classification confidence threshold: 0.4
5. Click Done.
