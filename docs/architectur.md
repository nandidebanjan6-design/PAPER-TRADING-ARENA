# System Architecture — Paper Trading Arena

## 1. Architecture Goal

Paper Trading Arena is designed as a **learning-first trading simulation system**, not simply a virtual buy/sell application.

The architecture is built around the core learning loop:

**Learn → Predict → Explain → Trade → Review → Reflect → Improve**

The system separates learning, simulation, decision tracking, review, and user progress so that each simulated trade becomes a learning experience.

---

## 2. Core Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | React + JavaScript | Interactive user interface |
| Styling | HTML + CSS | Structure and visual design |
| Backend | Node.js + Express.js | APIs and application logic |
| Database | MongoDB | User, trade, learning and progress data |
| Version Control | Git + GitHub | Source control and collaboration |
| Market Data | Historical data / suitable API | Simulation scenarios |

---

## 3. High-Level Architecture

```text
                         USER
                           |
                           v
                  +----------------+
                  |    FRONTEND    |
                  | React + JS     |
                  +----------------+
                           |
                           | REST API
                           v
                  +----------------+
                  |   BACKEND API  |
                  | Node + Express |
                  +----------------+
                           |
          +----------------+----------------+
          |                |                |
          v                v                v
   +-------------+  +-------------+  +-------------+
   |   LEARNING  |  |   TRADING   |  |   REVIEW &  |
   |   MODULE    |  |   ENGINE    |  | REFLECTION  |
   +-------------+  +-------------+  +-------------+
          |                |                |
          +----------------+----------------+
                           |
                           v
                  +----------------+
                  |    DATABASE    |
                  |    MongoDB     |
                  +----------------+
                           |
                           v
                  +----------------+

                  |  MARKET DATA   |
                  | Source / Feed  |
                  +----------------+
2)**Core Design Principle**

A trade should not end when the user sees profit or loss. It should end when the user understands the decision and identifies what to improve.

The complete learning loop is:
Learn
  ↓
Predict
  ↓
Explain
  ↓
Trade
  ↓
Observe
  ↓
Review
  ↓
Reflect
  ↓
Improve
  ↓
Next Challenge

5)** Frontend Layer**

The frontend is the main interface through which users interact with Paper Trading Arena.

Technology
React
JavaScript
HTML
CSS
Responsibilities

The frontend provides:

User onboarding
Learning modules
Market scenarios
Prediction input
Decision journal
Simulated trading interface
Virtual wallet
Portfolio
Trade history
Trade review
Reflection
Progress tracking
Learning challenges

The frontend focuses on user interaction and presentation.

Important business rules should also be validated by the backend rather than relying only on frontend logic.

7.** Learning Module**

The Learning Module handles the educational part of the product.

It can contain:

Beginner lessons
Short explanations
Examples
Learning checkpoints
Practice challenges
Topic completion status

Example:

Lesson
  ↓
Explanation
  ↓
Example
  ↓
Prediction Challenge
  ↓
Simulation
8. Decision Journal

The Decision Journal is one of the main differentiating components of Paper Trading Arena.

Before placing a simulated trade, the user records:

Prediction
Reasoning
Confidence level
Optional assumptions

Example:
Prediction:
Price will increase.

Reason:
The recent trend appears upward.

Confidence:
Medium

9.** Trading Simulation Engine**

The Trading Engine manages simulated transactions using virtual money.

It is responsible for:

Buy operations
Sell operations
Virtual wallet balance
Holdings
Trade quantity
Simulated execution
Trade timestamps
Trade history
Important Boundary

The Trading Engine does not connect to real brokerage accounts.

There is:

No real-money deposit
No real-money withdrawal
No real order execution
No brokerage integration

The system remains an educational simulation.

10. Market Data Layer

The Market Data Layer provides the information required for simulated scenarios.

Depending on the implementation stage, the system may use:

Historical market data
A suitable market-data API
Predefined educational scenarios

For the initial MVP, complex real-time trading infrastructure is unnecessary.

The market-data source should be replaceable without rewriting the learning, review, or user-interface systems.

11. **Review & Reflection System
**
The Review System connects trading activity back to learning.

After a simulated trade:

Original Prediction
        ↓
Original Reasoning
        ↓
Actual Market Outcome
        ↓
Difference
        ↓
Reflection
        ↓
Learning Point

The review helps the user answer:

What did I expect?
Why did I expect it?
What actually happened?
Where was my assumption different from the outcome?
What can I learn from this?

The purpose is not simply to tell the user whether the trade was right or wrong.

The purpose is to help the user understand the decision.

12. **Progress Tracking**

The system tracks learning progress rather than only simulated financial performance.

Possible progress signals include:

Lessons completed
Predictions recorded
Decisions explained
Trades completed
Reviews completed
Reflections completed
Challenges completed
Topics practiced

Example:
Learning Progress

Lessons:        4 / 5
Predictions:    8
Reviews:        7
Reflections:    6
Challenges:     3
13. Database Design
Technology

MongoDB

Possible collections:
Users
Lessons
LearningProgress
MarketScenarios
Trades
Portfolios
DecisionJournals
TradeReviews
Reflections
Challenges
**EXAMPLE RELATIONSHIP:**
User
 |
 +-- Learning Progress
 |
 +-- Trade
       |
       +-- Prediction
       +-- Reasoning
       +-- Confidence
       +-- Entry Data
       +-- Outcome
       +-- Review
       +-- Reflection
