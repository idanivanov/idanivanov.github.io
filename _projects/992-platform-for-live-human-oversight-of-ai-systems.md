---
layout: project
title: "Platform for Live Human Oversight of AI Systems"
image: "/assets/images/hitl.png"
project_summary: "API platform that enables human-in-the-loop (HITL) machine learning workflows. The platform is used by data scientists to connect their production AI models to a human workforce that can verify the outputs of the models in real-time. The platform provides work to refugees and people from conflict affected countries. As the CTO, I was responsible for the product management and technical implementation of the solution."
project_duration: "7 months"
team_size: "8 team members, 1 data scientist"
industry: "IT"
published: true
---

## Customer

The company is a Bulgarian startup that provides data collection and labeling services for artificial intelligence. The company is a social enterprise that provides work to refugees and people from conflict affected countries, such as, Syria, Afghanistan, Iraq, Ukraine, and others.

## Business Case

The company wanted to transition from a service based company to a product based company. The goal was to build a platform that would enable the company to scale its operations and provide a SaaS solution to its customers.

## Solution

The solution is an API platform that enables human-in-the-loop (HITL) machine learning workflows. The platform is used by data scientists to connect their production AI models to a human workforce that can verify the outputs of the models in real-time.

A typical workflow in the platform is the following:

1. A computer vision model detects objects in images on a production system.
2. The model outputs are sent in real-time to the platform via an API call.
3. The platform sends the outputs to a human worker who is currently on shift.
4. The human worker verifies the outputs and sends the results back to the platform.
5. The platform sends the results back to the production system where they can be used to override the model outputs or to train the model.

## Tools & Technologies

- Python
- PostgreSQL
- Google Cloud Platform
- Google Cloud Run
- Google Cloud Build
- Google Cloud SQL
- Google Cloud Functions
- Terraform
- Label Studio

## My Role & Responsibilities

As the Chief Technology Officer (CTO) of the company, my responsibilities included:

- Technology strategy - defining the company's strategy for transitioning from a service based company to a product based company
- Product management - defining the product roadmap, prioritizing the product features, managing the product backlog, and conducting customer interviews
- Software architecture design
- Software development
- Software deployment - CI/CD pipelines, infrastructure as code, and containerization
- Team management
- Technical support

## Results

During my time as CTO, the MVP of the platform was launched on production. The first paying customer was onboarded and started generating monthly subscription revenue. The onboarding of this customer provided work to 4 refugees.
