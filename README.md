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

# Slots
* Slot 1
  
| Field |	Value |
| --- | --- |
| Name |	PizzaSize |
| Slot Type |	SizeType |
| Prompt |	What size pizza would you like? |

* Slot 2

| Field |	Value |
| --- | --- |
| Name |	PizzaTopping |
| Slot Type |	ToppingType |
| Prompt |	What topping would you like? |

# Confirmation Prompt

You want a {PizzaSize} pizza with {PizzaTopping}.
Should I place the order?

# Decline Message

Okay — order cancelled.

# Success Response

Your pizza order has been placed!
Anything else?

Save → Build

# 🥤 Step 5 — Drink Ordering Intent

Create intent:
# Name
    DrinkOrdering
# Utterances
    drinks
    I want drinks
    Order a drink

# Slots
* Slot 1

| Field |	Value |
| --- | --- |
| Name |	DrinkType |
| Slot Type |	DrinkType |
| Prompt |	What drink would you like? |

* Slot 2

| Field |	Value |
| --- | --- |
| Name |	DrinkQuantity |
| Slot Type |	AMAZON.Number |
| Prompt |	How many {DrinkType}? |

# Confirmation Prompt

You want {DrinkQuantity} {DrinkType}.
Is that correct?

# Decline Message

No problem — cancelled.

# Success Response

Your drink order has been placed!

Save → Build

# 🧪 Step 6 — Test the Bot

Use the Test Panel in the console.

## Try:
    hi
    I want pizza
    medium
    pepperoni
    yes
    I want drinks
    Coke
    2
    yes

You should observe:
* Slot prompting
* Confirmation
* Fulfillment responses
* Natural language matching

# 📈 Optional Extensions

You can enhance this bot by adding:
* Lambda backend fulfillment
* Payment processing
* Delivery address slots
* Multi-language support
* Channel integrations (Slack, Twilio, Alexa)

# 🏁 Conclusion

This project demonstrates the fastest way to understand AWS conversational AI using only the browser console.
No infrastructure automation or scripting is required — making it ideal for workshops, classrooms, or onboarding.
