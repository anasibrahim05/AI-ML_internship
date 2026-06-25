# AI-Powered Health Query Chatbot with Safety Filtering

## Project Overview

This project is an AI-powered Health Query Chatbot built using Python and the Grok AI API. The chatbot answers general health-related questions using a Large Language Model (LLM) while applying multiple safety layers to ensure safe and responsible responses.

Unlike basic chatbots, this system uses a hybrid architecture combining rule-based filtering and LLM-based reasoning. The chatbot first checks whether the user's query indicates a medical emergency. If an emergency is detected, the system immediately advises the user to contact emergency healthcare services instead of generating AI advice.

For non-emergency cases, the query is sent to Grok AI using carefully designed prompts. After receiving the AI response, an output validation layer checks for harmful content such as prescriptions, dosage recommendations, or unsafe medical advice before displaying the final response.

This project demonstrates practical implementation of prompt engineering, AI safety filtering, API integration, and conversational healthcare assistant design.

---

## Problem Statement

Build a healthcare chatbot capable of answering general health-related questions using an LLM while ensuring safety.

Example queries:

* What causes a sore throat?
* Is paracetamol safe for children?
* Why do I have headaches?
* What causes fever?

The chatbot must:

* Answer general health questions
* Detect medical emergencies
* Avoid harmful medical advice
* Prevent unsafe prescriptions
* Encourage professional medical consultation when needed

---

## Project Objectives

* Build an AI-powered healthcare chatbot
* Integrate Grok AI API
* Apply prompt engineering
* Detect emergency situations
* Implement safety filters
* Prevent harmful AI responses
* Provide safe, readable answers

---

## Technologies Used

* Python
* Jupyter Notebook
* Grok AI API
* Prompt Engineering
* Rule-Based Filtering
* Conversational AI
* Safety Validation System

---

## System Architecture

The chatbot uses a hybrid pipeline:

1. User Query Input
2. Input Safety Filter
3. Emergency Detection
4. Query Sent to Grok AI
5. AI Response Generation
6. Output Safety Validation
7. Final Safe Response

---

## Core Features

### 1. Emergency Detection Layer

Before sending any query to AI, the chatbot checks for emergency-related keywords.

Example emergency keywords:

* heart attack
* chest pain
* difficulty breathing
* unconscious
* severe bleeding
* stroke

If emergency symptoms are detected, the chatbot does not rely on AI-generated advice.

Example response:

"Your symptoms may indicate a medical emergency. Please contact emergency medical services or visit the nearest hospital immediately."

This reduces the risk of delayed medical intervention.

---

### 2. Prompt Engineering

Prompt engineering is used to control LLM behavior.

Example system prompt:

You are a helpful medical assistant. Provide clear, simple, and safe health-related information. Do not diagnose diseases, prescribe medicines, or provide dangerous medical advice. Always recommend consulting a doctor for serious symptoms.

Prompt engineering helps the AI:

* Stay safe
* Be friendly
* Be easy to understand
* Avoid harmful suggestions

---

### 3. Grok AI API Integration

For non-emergency queries, the chatbot sends user input to Grok AI.

Workflow:

* Create prompt
* Send API request
* Receive AI response
* Validate response

The LLM generates informative health explanations in natural language.

---

### 4. Output Validation Layer

After AI generates a response, another safety filter validates the output.

The system blocks responses containing:

* Medication prescriptions
* Exact dosage instructions
* Dangerous treatment advice
* Harmful suggestions

Examples of blocked content:

* Take 500mg every 6 hours
* Start antibiotics immediately
* Increase dosage

Blocked responses are sanitized before showing them to users.

---

## Working Methodology

### Step 1: User Input

User asks a health-related question.

Example:

What causes sore throat?

---

### Step 2: Input Validation

The chatbot checks whether the query contains emergency indicators.

If emergency detected:

* Stop AI processing
* Show emergency warning

Otherwise:

* Continue to AI model

---

### Step 3: Send Query to Grok AI

The system sends:

* System prompt
* Safety instructions
* User query

to Grok AI API.

---

### Step 4: AI Response Generation

Grok AI processes the query and generates a response.

Example:

A sore throat may be caused by viral infection, allergies, dry air, or irritation.

---

### Step 5: Output Safety Check

The generated response is analyzed for unsafe content.

Unsafe recommendations are removed or blocked.

---

### Step 6: Final Response

A safe and readable response is displayed to the user.

---

## Example Conversations

### Example 1: Normal Query

User: What causes a sore throat?

Bot: A sore throat may happen because of viral infection, allergies, dry air, or irritation.

---

### Example 2: Emergency Query

User: I have chest pain and cannot breathe.

Bot: Your symptoms may indicate a medical emergency. Please contact emergency services immediately.

---

## Skills Demonstrated

* Prompt Engineering
* LLM API Integration
* AI Safety Filtering
* Healthcare AI Design
* Conversational Agent Development
* Input Validation
* Output Validation
* Rule-Based Systems

---

## Challenges

* Detecting emergency cases accurately
* Preventing harmful AI responses
* Designing effective prompts
* Handling ambiguous health queries

---

## Limitations

* Cannot replace professional doctors
* May miss rare emergency phrasing
* Depends on LLM response quality
* Not intended for emergency diagnosis

---

## Future Improvements

Possible enhancements:

* Voice assistant integration
* Web/mobile application deployment
* Multi-language support
* Advanced symptom checker
* Fine-tuned medical LLM
* Medical knowledge base integration

---

## Conclusion

This project demonstrates a hybrid AI healthcare chatbot that combines rule-based emergency detection with Grok AI-powered response generation.

By integrating input filtering, prompt engineering, and output validation, the system provides safe, readable, and responsible health information while minimizing harmful medical advice. This makes the chatbot more reliable for healthcare-related conversational AI applications.
