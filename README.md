# GigShield AI

AI-powered parametric insurance platform protecting gig delivery workers from income loss caused by environmental disruptions.

GigShield AI is designed for gig economy workers such as delivery partners from platforms like Blinkit, Zepto, and Swiggy Instamart who depend on daily deliveries for income. The platform automatically detects environmental disruptions and compensates workers through automated parametric insurance claims.


# Problem Statement

Gig economy delivery workers rely on daily orders to earn their income. However, environmental disruptions such as:

* Heavy rain
* Flooding
* Extreme heat
* High pollution levels

can significantly reduce delivery demand and limit workers' ability to complete orders.

Even when workers remain active on the platform, they may receive fewer delivery requests due to these disruptions, resulting in sudden income loss.

Currently, gig workers do not have a financial safety net to protect them from these short-term environmental disruptions.


# Why This Problem Matters

Millions of gig workers depend on daily earnings for their livelihood.

Even a few hours of disruption can cause:

* Reduced order volume
* Idle working hours
* Significant income reduction

Traditional insurance models are not designed to cover micro-income losses caused by short-term environmental conditions.

GigShield AI addresses this gap by introducing an automated parametric insurance system tailored specifically for gig workers.


# Our Solution

GigShield AI provides automated income protection through parametric micro-insurance.

The platform continuously monitors:

* Environmental conditions
* Worker activity
* Delivery performance

When disruption events occur and income loss is detected, the system automatically triggers an insurance claim and compensates the worker.

Key capabilities include:

* Real-time environmental monitoring
* AI-based income loss prediction
* Automated claim triggering
* Fraud detection
* Instant compensation payout

This eliminates manual claim processes and ensures faster support for gig workers.


# Target Users

Primary Users

* Quick commerce delivery workers
* Gig economy drivers
* Hyperlocal logistics partners

Examples

* Blinkit delivery partners
* Zepto delivery workers
* Swiggy Instamart riders


# Parametric Insurance Model

GigShield AI uses a parametric insurance approach.

Unlike traditional insurance that requires manual claim verification, parametric insurance automatically triggers payouts when predefined conditions are met.

Example triggers:

| Event          | Condition          |
| -------------- | ------------------ |
| Heavy Rain     | Rainfall > 70mm    |
| Extreme Heat   | Temperature > 42°C |
| High Pollution | AQI > 350          |

When these thresholds are crossed and worker activity is confirmed, the system evaluates delivery performance and triggers a payout if income loss is detected.


# Claim Trigger Logic

GigShield AI evaluates three key factors before triggering a claim.

IF
rainfall > threshold
AND worker was active
AND delivery rate dropped

THEN
auto insurance claim is triggered.

Example Scenario

Rainfall: 45mm
Worker active: Yes
Expected deliveries: 12
Completed deliveries: 4

Delivery drop = 66%

Result: Automatic insurance compensation for the worker.


# System Architecture

![System Architecture](architecture/system-architecture.png)

The platform consists of multiple layers.

External Data Sources
Weather API and Air Quality API provide environmental data such as rainfall, temperature, and pollution levels.

Frontend Layer
Worker Web App and Dashboard built using React and Vite allow workers to manage policies, monitor claims, and view payouts.

Backend Microservices
Spring Boot services handle business logic including:

* Worker Service
* Policy Service
* Claim Service
* Notification Service

Core Processing Layer
Includes the Parametric Trigger Engine and AI Prediction Engine responsible for detecting disruptions and evaluating income loss.

Data Layer
PostgreSQL database stores worker data, policies, delivery statistics, weather events, claims, and payout records.

Payment System
Handles automated compensation payouts to workers once claims are approved.


# AI / ML Design

GigShield AI uses machine learning models to estimate income loss risk and detect fraud.

Input Data Sources

* Weather conditions
* Worker activity data
* Delivery performance data
* Worker location data

AI Processing Pipeline

Weather Data + Delivery Data
↓
Feature Engineering
↓
Machine Learning Model
↓
Income Loss Risk Score
↓
Parametric Claim Trigger

AI Functions

Risk Scoring
Predicts disruption risk for each delivery zone.

Income Loss Prediction
Estimates expected delivery reduction during disruption events.

Fraud Detection
Identifies suspicious claim patterns and abnormal worker activity.


## System Workflow

The GigShield AI platform automatically detects disruption events and processes claims using the following workflow.

| Step | Process |
|-----|--------|
| 1 | Worker registers and selects an insurance plan |
| 2 | System continuously monitors environmental conditions |
| 3 | Environmental disruption detected |
| 4 | Worker activity is verified |
| 5 | Delivery performance drop is calculated |
| 6 | AI model evaluates income loss risk |
| 7 | Automatic insurance claim generated |
| 8 | Fraud detection verification |
| 9 | Compensation payout to the worker |


# Technology Stack

Frontend
React.js + Vite

Backend
Spring Boot

Database
PostgreSQL

AI / ML
Python + Scikit-learn

External APIs
Weather API
Air Quality API


# Project Structure

gigshield-ai
│
├── frontend/ # React + Vite worker dashboard
│
├── backend/ # Spring Boot microservices
│
├── ai-service/ # Machine learning models and prediction APIs
│
├── architecture/ # System architecture diagrams
│
└── README.md # Project documentation


# Innovation

GigShield AI introduces several innovations for the gig economy:

* Automated parametric insurance for gig workers
* AI-driven income loss estimation
* Real-time environmental disruption monitoring
* Intelligent fraud detection
* Instant claim triggering and payouts


# Future Scope

* Integration with real delivery platforms
* Hyperlocal risk prediction models
* Dynamic insurance pricing
* Mobile application for gig workers
* Predictive disruption alerts
* Blockchain-based claim transparency


# Team

Guidewire DevTrails Hackathon Team
KLU DEV 2327