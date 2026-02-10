# 🍕 AWS Lex Chatbot — Pizza Ordering (Console-Only Guide)

This repository documents how to build a pizza ordering chatbot using AWS Lex (V2) entirely through the AWS Management Console — no JSON imports, no code, and no CLI required.

It’s designed for beginners learning conversational AI concepts like intents, utterances, and slots.

# 📌 Overview

This chatbot can:

* Greet users
* Take pizza orders (size + topping)
* Take drink orders (type + quantity)
* Confirm user choices
* Simulate order fulfillment

It demonstrates the core building blocks of AWS Lex:

| Component	| Purpose |
| ---- | ---- |
| Bot | Container for conversational logic |
| Intent | User goal (ordering pizza, greeting) |
| Utterance |	Example phrases triggering an intent |
| Slot | Required information to fulfill an intent |
| Slot Type | Allowed values for slots |

# ✅ Prerequisites

* AWS account
* Console access permissions for:
  * Amazon Lex
  * IAM auto-role creation (default wizard behavior)
  
# ⚠️ Note: AWS services may incur charges depending on usage. Review pricing before deployment.

# 🚀 Step 1 — Create the Bot
1. Log into AWS Console
2. Navigate to Amazon Lex
3. Click Create bot
4. Choose:

| Setting |	Value |
| --- | --- | 
| Creation | Method	Create a blank bot |
| Bot name |	PizzaBot |
| Runtime role	| Create new role |
| Language |	English (US) |
| Voice |	Joanna |
| Confidence threshold |	0.4 |

5. Click Create

# 🧠 Step 2 — Create Slot Types

Go to Slot types → Create

SizeType

Values:

    small
    medium
    large
    
ToppingType

Values:

    pepperoni
    sausage
    chicken
    
DrinkType

Values:

    Coke
    Pepsi
    Sprite
    Vodka

Save each slot type.

# 👋 Step 3 — Greeting Intent

Go to Intents → Create intent

Name

    Greeting

Sample Utterances

    hi
    hello
    hey
    
Closing Response

    Hi! Welcome to the Amazing Pizza Store.
    I can help you order pizza or drinks.
    What would you like?

Save → Build

# 🍕 Step 4 — Pizza Ordering Intent

Create intent:

Name

    PizzaOrdering
    
Utterances

    I want pizza
    Order pizza
    I'd like pizza
