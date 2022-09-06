---
layout: project
title: "Predictive Maintenance of Cryopumps"
image: "/assets/images/manufacturing.png"
project_summary: "Machine learning system for early warning of failing industrial pumps helping to reduce unscheduled downtime of semiconductor manufacturing processes."
project_duration: "10 months"
team_size: "11 team members, 4 data scientists"
industry: "Manufacturing"
published: true
---

## Customer

Leading global producer of cryopumps for the semiconductor manufacturing industry.

## Business Case

Semiconductor manufacturing requires a specific environment which is maintained using cryopumps. Cryopumps are reliable and have a long life, but when they fail they can cause unscheduled downtime of the manufacturing process which may have high opportunity cost. To reduce unscheduled downtime, cryopumps should be replaced before they fail.

Each cryopump is equipped with a set of sensors that constantly measures its state. This data is being used by support engineers who manually flag cryopumps for early replacement.

## Solution

Our team built a software system that helps support engineers identify more easily cryopumps at risk of failing. The system uses a machine learning model that predicts if a cryopump is going to fail. The model was trained on a large set of historical data from cryopumps that have previously failed. It is also regularly re-trained on fresh data and feedback from human domain experts using Azure ML pipelines.

The solution also identifies abnormal behavior of the cryopumps using anomaly detection algorithms. Engineers can inspect the sensor measurements of the cryopump on interactive dashboards enriched with the flagged anomalous events and the risk estimation of cryopump failure.

## Tools & Technologies

- Microsoft Azure
- Azure Machine Learning
- Python
- R
- Azure SQL
- Azure Anomaly Detector
- Docker

## My Role & Responsibilities

I was technical lead of the data science team working on the machine learning part of the project. My responsibilities were:

- Technical consultancy
- Data science team management
- Definition of the cloud architecture of the ML solution
- Data analysis
- Productionalization of the machine learning solution
