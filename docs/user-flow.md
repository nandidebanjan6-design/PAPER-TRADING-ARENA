# User Flow — Paper Trading Arena

## 1. Purpose

This document defines the primary user journey for **Paper Trading Arena**.

The product is designed around a simple learning loop:

> **Learn → Predict → Decide → Trade → Review → Improve**

The user should not simply make simulated trades. Each trade should create an opportunity to understand the decision, compare expectations with outcomes, and improve future decision-making.

---

## 2. Target User

The primary user is a beginner who:

* Has little or no previous trading experience
* Wants to understand basic market concepts
* Wants to practise without risking real money
* Wants to understand the reasoning behind trading decisions
* Needs a structured way to learn from simulated outcomes

---

## 3. Primary User Journey

```text
                    START
                      |
                      v
                Create Account
                      |
                      v
                  Onboarding
                      |
                      v
               Learn a Concept
                      |
                      v
              View Market Scenario
                      |
                      v
             Make a Prediction
                      |
                      v
             Record Reasoning
                      |
                      v
            Place Simulated Trade
                      |
                      v
               Track Position
                      |
                      v
              Trade Completed
                      |
                      v
                Review Result
                      |
                      v
              Reflect & Record
                      |
                      v
               Identify Lesson
                      |
                      v
              Continue Learning
                      |
                      v
                   REPEAT
```

---

## 4. Detailed User Flow

### Step 1 — Onboarding

The user enters the platform and is introduced to the purpose of the product.

The onboarding explains that:

* Trading is simulated
* No real money is involved
* The platform is designed for learning
* The objective is to improve decision-making rather than simply maximize virtual profit

**User outcome:**
The user understands what the platform is for before starting.

---

### Step 2 — Learn

The user selects a beginner-friendly learning module.

Example topics:

* What is a stock?
* What is an order?
* What are entry and exit points?
* What is risk and reward?
* What is a stop-loss?
* Common beginner mistakes

The content should be short and understandable rather than presenting large amounts of theory at once.

**User outcome:**
The user gains enough knowledge to attempt the next activity.

---

### Step 3 — View a Market Scenario

The user enters the simulated market environment.

The user can view relevant information about an available asset or scenario.

For the MVP, the interface should remain simple rather than attempting to reproduce a professional trading terminal.

**User outcome:**
The user has enough information to form a basic expectation.

---

### Step 4 — Predict

Before trading, the user records what they expect to happen.

Example:

> "I expect the price to increase over the next simulated period."

The user may also record an expected direction or target.

**User outcome:**
The user's expectation exists before the result is known.

---

### Step 5 — Record Reasoning

The user explains why they are considering the trade.

Example prompts:

* Why are you considering this trade?
* What information influenced your decision?
* What outcome do you expect?
* What would make you reconsider the trade?

The purpose is not to test whether the user's reasoning is professionally correct.

The purpose is to capture the user's decision-making process.

**User outcome:**
The user has a record of the reasoning behind the decision.

---

### Step 6 — Simulated Trade

The user chooses an action:

* Buy
* Sell
* Stay out

If the user chooses to trade, the system uses virtual funds.

No real-money transaction takes place.

**User outcome:**
The decision becomes a trackable simulated trade.

---

### Step 7 — Track Position

The user can monitor the simulated position through the portfolio.

The portfolio can show:

* Virtual balance
* Open positions
* Entry price
* Current simulated value
* Simulated profit/loss
* Trade history

The interface should avoid unnecessary professional-level complexity in the MVP.

**User outcome:**
The user can understand what happened to the simulated position.

---

### Step 8 — Trade Completion

When the simulated trade reaches its defined exit condition, the position is closed.

The system stores:

* Original prediction
* Decision reasoning
* Entry
* Exit
* Result
* Simulated profit/loss

**User outcome:**
The complete decision and outcome are available for review.

---

### Step 9 — Review

The user is taken through a structured review.

The platform compares:

```text
WHAT I EXPECTED
       vs.
WHAT ACTUALLY HAPPENED
```

The review can ask:

* Was the original prediction correct?
* What happened differently?
* What information did I overlook?
* What part of my reasoning was useful?
* What could I reconsider next time?

**User outcome:**
The user understands the difference between expectation and outcome.

---

### Step 10 — Reflect

The user records a short reflection.

Example:

> "I focused only on the expected price movement and did not consider the risk of the trade."

The reflection becomes part of the user's learning history.

**User outcome:**
The user converts a simulated result into a personal learning point.

---

### Step 11 — Improve

The platform can surface simple patterns from previous activity.

For example:

* Frequently entering trades without defining an exit
* Frequently skipping the review step
* Repeating a similar reasoning pattern
* Completing certain learning modules but not applying them

The system should present these as **learning observations**, not financial recommendations.

**User outcome:**
The user has a specific area to improve.

---

### Step 12 — Repeat

The user returns to another learning activity or simulated scenario.

The cycle begins again:

```text
Learn
  ↓
Predict
  ↓
Decide
  ↓
Trade
  ↓
Review
  ↓
Reflect
  ↓
Improve
  ↓
Repeat
```

This repeated loop is the core product experience.

---

# 5. Main Screens

## Screen 1 — Onboarding

Purpose:

* Explain the product
* Establish that trading is simulated
* Introduce the learning-first approach

Primary action:

**Start Learning**

---

## Screen 2 — Learning Dashboard

Purpose:

* Show available lessons
* Display learning progress
* Recommend the next learning activity

Example:

```text
Learning Progress

[██████░░░░] 60%

Completed:
✓ Market Basics
✓ Risk & Reward

Next:
→ Entry & Exit Basics
```

---

## Screen 3 — Market Scenario

Purpose:

* Present a simple simulated market situation
* Allow the user to study the available information
* Provide access to the prediction step

Primary action:

**Make Prediction**

---

## Screen 4 — Decision Journal

Purpose:

Capture the user's reasoning before the trade.

Example fields:

```text
What do you expect?

[________________________]

Why?

[________________________]

What is your planned exit?

[________________________]

What could make your prediction wrong?

[________________________]
```

Primary action:

**Continue to Trade**

---

## Screen 5 — Trading Interface

Purpose:

Allow the user to execute a simulated decision.

Actions:

* Buy
* Sell
* Stay Out

The user interacts only with virtual funds.

---

## Screen 6 — Portfolio

Purpose:

Show the user's simulated activity.

Information:

* Virtual balance
* Current positions
* Trade history
* Simulated P/L

Primary action:

**Review Trade**

---

## Screen 7 — Trade Review

Purpose:

Help the user compare the original decision with the actual outcome.

Example:

```text
Your Prediction
      ↓
Actual Outcome
      ↓
What Changed?
      ↓
What Did You Learn?
```

Primary action:

**Complete Review**

---

## Screen 8 — Progress & Challenges

Purpose:

Encourage continued learning.

Possible sections:

* Learning progress
* Completed reviews
* Active challenges
* Decision patterns
* Next learning activity

---

# 6. Decision Points

The user should make meaningful decisions at several points.

### Decision Point 1

**What should I learn next?**

↓

### Decision Point 2

**What do I expect to happen?**

↓

### Decision Point 3

**Should I trade or stay out?**

↓

### Decision Point 4

**What is my reasoning?**

↓

### Decision Point 5

**What did I learn from the result?**

These decisions make the platform an educational experience rather than only a transaction simulator.

---

# 7. Empty and Edge States

The product should also account for situations where the user has no previous activity.

### New User

Display:

> "You haven't completed any trades yet. Start with a short learning module."

### No Open Positions

Display:

> "You currently have no open simulated positions."

### No Trade History

Display:

> "Your completed trades will appear here."

### Incomplete Review

If a trade is completed but the review has not been submitted:

> "Complete your trade review to record what you learned."

---

# 8. Core Learning Loop

The most important product loop is:

```text
┌───────────────┐
│     LEARN     │
└───────┬───────┘
        ↓
┌───────────────┐
│    PREDICT    │
└───────┬───────┘
        ↓
┌───────────────┐
│     DECIDE    │
└───────┬───────┘
        ↓
┌───────────────┐
│     TRADE     │
└───────┬───────┘
        ↓
┌───────────────┐
│    REVIEW     │
└───────┬───────┘
        ↓
┌───────────────┐
│    REFLECT    │
└───────┬───────┘
        ↓
┌───────────────┐
│    IMPROVE    │
└───────┬───────┘
        │
        └──────────────→ REPEAT
```

This loop is the central interaction model of Paper Trading Arena.

---

# 9. MVP User Flow

The first version will keep the journey intentionally simple:

```text
Onboarding
    ↓
Learning Module
    ↓
Market Scenario
    ↓
Prediction
    ↓
Decision Journal
    ↓
Simulated Trade
    ↓
Portfolio
    ↓
Trade Review
    ↓
Reflection
    ↓
Progress
```

Advanced features will be considered only after this basic loop has been validated with beginner users.

---

# 10. Product Success Criteria

The user flow will be considered successful if a beginner can:

1. Understand the basic concept being taught.
2. Form a prediction before trading.
3. Explain the reasoning behind a simulated decision.
4. Complete a simulated trade.
5. Compare the prediction with the actual result.
6. Complete a structured review.
7. Identify at least one learning point.
8. Apply that learning to a future simulation.

The goal is therefore not simply:

> **"Did the user make money?"**

The more important question is:

> **"Did the user understand something better after completing the trade?"**

---

# 11. Design Principle

Every major interaction should support the central product principle:

> **A simulated trade should teach you something.**

The interface should therefore guide users from **action → outcome → reflection → improvement**, rather than stopping at the profit/loss result.

---

# 12. Scope Boundary

This user flow does not include:

* Real-money transactions
* Deposits
* Withdrawals
* Brokerage accounts
* Personalized investment advice
* Guaranteed-return systems
* Professional trading terminals
* High-frequency trading

These are outside the scope of the initial educational simulation.

