# PrePlate

## An Agentic AI-Based Campus Food Pre-Ordering and Smart Pickup System

## Overview

PrePlate is an AI-based campus food pre-ordering system designed to reduce waiting time at campus food counters. It allows students to order food in advance, receive personalized recommendations, and get a suitable pickup time based on their requirements and the current cafeteria queue.

The system uses multiple AI agents and follows a Service-Oriented Architecture (SOA) to coordinate food ordering, recommendations, queue estimation, kitchen processing, and feedback.

## Problem Statement

Campus food counters often experience long queues during lunch and break hours. Students have limited time between classes and may spend a significant amount of their break waiting for food.

Existing food-ordering systems mainly provide menu browsing, ordering, and order tracking. They generally do not consider factors such as student preferences, budget, current queue, preparation time, and available time before the next class.

PrePlate aims to provide an intelligent campus-specific solution to this problem.

## Objectives

* Reduce waiting time at campus food counters.
* Allow students to pre-order food.
* Understand natural-language food requests.
* Provide personalized food recommendations.
* Estimate food preparation and waiting time.
* Recommend suitable pickup times.
* Improve coordination between students and cafeteria staff.
* Analyze student feedback.
* Demonstrate Agentic AI with Service-Oriented Architecture.

## Key Features

### Natural-Language Ordering

Students can describe what they want in simple language.

Example:

> I want a vegetarian meal under Rs. 150 and I have class at 1 PM.

The system extracts the relevant requirements from the request.

### Food Recommendation

The system recommends suitable food based on:

* Food preference
* Budget
* Availability
* Previous orders
* Preparation time

### Smart Pickup Recommendation

The system considers the current queue and estimated preparation time to recommend a suitable pickup slot.

### Agent-Based Processing

The system uses specialized agents for different tasks:

* Order Agent
* Recommendation Agent
* Queue Agent

These agents work together to process a student's request.

### Kitchen Management

The kitchen receives confirmed orders and can update their status:

```text
Confirmed -> Preparing -> Ready
```

### Feedback Analysis

Students can provide feedback after receiving their orders. The feedback can be analyzed to identify its general sentiment.

## Novelty

### 1. Multi-Agent Cafeteria Coordination

Multiple specialized AI agents work together to handle different stages of the food-ordering process.

### 2. Context-Aware Smart Pickup

The system considers the student's available time, food preparation time, and current queue when recommending a pickup time.

### 3. Demand-Aware Food Service

Order information can be analyzed to identify busy periods and support better cafeteria preparation planning.

## System Workflow

```text
Student
   |
   v
React Web Application
   |
   v
FastAPI REST API
   |
   v
AI Agent Manager
   |
   +-------------------+-------------------+
   |                   |                   |
   v                   v                   v
Order Agent      Recommendation Agent   Queue Agent
   |                   |                   |
   +-------------------+-------------------+
                       |
                       v
                  Menu Service
                       |
                       v
                  Order Service
                       |
                       v
                 Kitchen Service
                       |
                       v
                   Order Ready
                       |
                       v
              Notification Service
                       |
                       v
                    Student
                       |
                       v
                   Feedback
                       |
                       v
              Sentiment Analysis
```

## AI Technologies

| Technology                | Purpose                                                |
| ------------------------- | ------------------------------------------------------ |
| Google Gemini             | Natural-language understanding and response generation |
| LangGraph                 | AI agent orchestration                                 |
| Whisper                   | Optional voice-to-text ordering                        |
| Scikit-learn              | Queue and basic demand prediction                      |
| Hugging Face Transformers | Feedback sentiment analysis                            |

## SOA Services

| Service                  | Responsibility                      |
| ------------------------ | ----------------------------------- |
| Student Service          | Student information and preferences |
| Menu Service             | Food items, prices and availability |
| Order Service            | Creating and tracking orders        |
| Recommendation Service   | Food recommendations                |
| Queue Prediction Service | Waiting-time estimation             |
| Kitchen Service          | Kitchen order management            |
| Feedback Service         | Feedback collection and analysis    |
| Notification Service     | Order status notifications          |

The services communicate through REST APIs and perform separate functions while working together as a complete system.

## Technology Stack

### Frontend

* React
* JavaScript
* HTML
* CSS

### Backend

* Python
* FastAPI
* REST APIs

### AI and Machine Learning

* Google Gemini
* LangGraph
* Whisper
* Scikit-learn
* Hugging Face Transformers

### Database

* MySQL

### Deployment and Development

* Docker
* Git
* GitHub
* VS Code

## Project Structure

```text
PrePlate/
|
├── frontend/
|
├── backend/
|   ├── services/
|   |   ├── student/
|   |   ├── menu/
|   |   ├── order/
|   |   ├── recommendation/
|   |   ├── queue/
|   |   ├── kitchen/
|   |   ├── feedback/
|   |   └── notification/
|   |
|   ├── agents/
|   |   ├── order_agent.py
|   |   ├── recommendation_agent.py
|   |   └── queue_agent.py
|   |
|   ├── models/
|   └── database/
|
├── ml/
|   ├── queue_prediction/
|   └── feedback_analysis/
|
├── docs/
|
├── requirements.txt
├── docker-compose.yml
└── README.md
```

## User Roles

### Student

* Browse the menu
* Search for food
* Make natural-language requests
* Receive recommendations
* Place pre-orders
* Select or accept pickup times
* Track order status
* Submit feedback

### Cafeteria Staff

* View incoming orders
* Update order status
* Manage food availability
* View busy periods
* Review feedback

## Evaluation Metrics

The system will be evaluated based on:

* Order-processing success rate
* Natural-language request understanding
* Recommendation relevance
* Queue prediction error
* API response time
* Service reliability
* Estimated reduction in waiting time
* User satisfaction

## SDG Alignment

### SDG 12: Responsible Consumption and Production

PrePlate supports better planning of campus food services using order and demand information.

### SDG 9: Industry, Innovation and Infrastructure

The project demonstrates the use of AI and Service-Oriented Architecture to develop an intelligent digital service for a real-world campus problem.

## Expected Outcome

The final outcome is a functional prototype that demonstrates an intelligent campus food pre-ordering workflow:

```text
Natural-Language Request
        |
        v
AI Understanding
        |
        v
Food Recommendation
        |
        v
Queue Estimation
        |
        v
Smart Pickup Time
        |
        v
Order Confirmation
        |
        v
Kitchen Processing
        |
        v
Order Ready
```

The project demonstrates how Agentic AI and Service-Oriented Architecture can be combined to provide a practical and efficient campus food pre-ordering and smart pickup solution.

## Development Plan

### Phase 1: Basic Application

* React frontend
* FastAPI backend
* MySQL database
* Student module
* Menu module
* Basic ordering

### Phase 2: SOA Integration

* Menu Service
* Order Service
* Kitchen Service
* Notification Service
* REST API integration

### Phase 3: Agentic AI

* Order Agent
* Recommendation Agent
* Queue Agent
* LangGraph workflow
* Gemini integration

### Phase 4: AI Features

* Queue prediction
* Basic demand analysis
* Feedback sentiment analysis
* Optional voice ordering

### Phase 5: Finalization

* Integration testing
* Docker setup
* UI improvements
* Performance evaluation
* Documentation
* Final demonstration

## Project Status

In Development




