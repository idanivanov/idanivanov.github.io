---
layout: post
title: "4 Stages of a Data Science Project and How to Manage Them"
author: "Ivan Danielov Ivanov"
image: "/assets/images/4_stages_post_cover.png"
date: 2022-09-16 14:16:00 +0300
categories: data science project management
summary: "Managing projects that involve machine learning and advanced analytics is challenging. The biggest challenge is the uncertainty if actual business value can be extracted from the available data. Such projects have 4 common stages associated with different levels of uncertainty: conceptual research, technical research, implementation, and maintenance."
published: true
---
Let me tell you a story about Dianne -- an experienced IT project manager who has delivered a lot of great software products.

Dianne is excited about a new project she is just starting -- an AI powered web application for predictive maintenance of factory equipment. For the first time in her career she will be working with a team of data scientists alongside the software engineers, QAs and designers that she already has experience working with. The data science team will be taking care of the machine learning part of the project.

A couple of weeks into the project, the development of the application is going on track but the ML part is lagging behind. The data science team seems to be working hard but the predictive services are still not delivered. The task updates from the team are so vague that it seems only the data scientists know what's going on in their team.

Dianne is getting concerned about this lack of visibility and starts to wonder what could be the reason for it. Maybe the data scientists are not doing their job properly and need to be micromanaged? Or maybe the management approach that works well for software engineers needs an adjustment for the data scientists?

## Data Science is not (exactly) Software Engineering

It is tempting to expect data science teams to behave the same way as software engineering teams. At the end, both provide a software solution. So why are they different?

The biggest difference comes from the __uncertainty__ of the research that data science work requires prior to building the software solution. In order to build a data pipeline or a service, data scientists first need to make sure that the data transformations and models at the core of the solution would provide valuable results. Consider the example of Dianne's predictive maintenance project. What if the data that is collected about the factory equipment doesn't provide any information about potential equipment failure? Even if she employs the best data scientists with PhD degrees from MIT to build the most scalable cloud Big Data pipelines and train the latest state-of-the-art deep learning models, the solution will still not bring any value to the client. This is the biggest risk in data science and in any other R&D initiative for that matter.

So, if there is such a difference between data science and software engineering, how does one deal with data scientists? To make sense of it all, let's consider the __4 common stages__ of a typical data science project and how to handle them from a management perspective.

Disclaimer: The idea of this post is not to challenge your current agile methodology, whichever framework you might use, but rather to compliment it. It is meant to equip you with a mindset about the data science work process that can help you get optimal results from your data science team. I believe these principles can fit into any agile framework.

![4 Stages of a Data Science Project](/assets/images/4_stages_of_a_data_science_project.png)

## Stage 1: Conceptual Research

This is the beginning of the data science workflow. It follows directly the initial discovery phase that led to forging the requirements for the project. In the general case this stage requires the following __inputs__:

- General project requirements
- Access to client stakeholders (internal or external)
- Existing historical data

At this stage chaos turns into order. The data scientists need to discuss the requirements with the client and the greater project team. They need to find all relevant data sources and gain access to them. They need to dig into the data to understand which parts can be used as input or ground truth. The technical objectives are framed. The data science team handles the exploration uncertainty of this stage by quickly iterating over different hypotheses. The hypothesis validation process is in a way similar to The Lean Startup [<a href="#ref-1">1</a>] approach. Validation in this case means to provide evidence that the project requirements are achievable using the available data, time and resources.

In the example of Dianne's predictive maintenance project, this stage might include things like: understanding what specific factory equipment should the machine learning services cover; what data is collected about each type of equipment and where is it stored; when should an equipment item be replaced; etc. A technical objective in this case might be: to build a supervised machine learning model that takes as input time series from sensor readings and predicts if an equipment item of type X is going to fail within the next 24 hours.

This stage requires a high degree of __proactiveness__ and __leadership__ from the data scientists. Moreover, the mentioned activities are not something universities usually teach, so fresh graduates may get overwhelmed by them. Therefore, it is a good idea to delegate the work at this stage to more experienced data scientists.

It is also a good idea to provide the team with some degree of freedom. It is OK if the task updates at this stage are more vague than usual. It is an __exploration__ process. The data science activities during the conceptual research are very dynamic and require creative thinking. Asking the team to provide too detailed reports of their activities might negatively impact the exploration. Keeping the bureaucratic overhead to a necessary minimum can improve the performance of the team.

The __duration__ of this stage depends on the specificity of the project requirements. If the project is, for example, about clustering of customers using survey data, this stage might even be skipped. But, in the case of Dianne's predictive maintenance project, it might take weeks. As a rule of thumb, providing the team with 2 weeks for conceptual research might be a good starting point for common data science projects.

The following __deliverables__ can be expected from the conceptual research:

- Defined technical objective
- List of candidate input and ground truth data sources

The most important outcome from this stage, however, is the solid __understanding of the business domain and data collection processes__. This knowledge is not measurable, but it is essential for the data science team, in order to be able to deliver on the next stages of the project.

## Stage 2: Technical Research

During the technical research the data science team aims to achieve the technical objective using the input and ground truth data. This work is usually done with tools like Jupyter Notebook. It includes activities, such as: data cleaning and analysis; feature engineering; training and evaluation of multiple machine learning models; presentation of results; etc.

This is the stage that data scientists usually love the most. It is what universities teach them to do best. The keyword here is __experimentation__. The activities can be handled by both fresh graduates and seasoned data scientists. It is a great opportunity to let motivated junior team members gain practical experience and bring new ideas with proper supervision from senior members.

The team would usually try to achieve the highest possible quality results using the available resources. For example, to maximize the accuracy of the predictive maintenance machine learning model. Getting to this goal, however, might take forever. The process is iterative and each iteration produces a new model. The quality of this model is then compared to the previously built models. The set of possible models to build is infinite, so this process can easily go out of hand and take a long time without producing any significant improvements.

For this reason it is important to find the right __balance__ between the accepted quality of the solution and the time spent on technical research. One way to optimize this trade-off would be to set beforehand a limited amount of time for technical research. If the produced results at the end are not satisfactory, then provide additional limited time. Repeat that until the results are good enough or the acceptable time limit is reached.

The following __deliverables__ can be expected from the technical research:

- Comparison report of the different technical approaches
- Working prototype of the best performing models and/or data transformations (usually provided as Python/R/SQL code in Jupyter Notebooks)
- Documentation of the technical approach with theoretical explanations (such documentation would enable the transferability of the project)

Another important outcome from this stage is a common understanding between the data science team, the greater project team, and the client stakeholders about the __expected performance__ of the selected technical approach. For example, everybody should be on the same page about what accuracy would be expected of the predictive models once they go live and what that would mean for the business. The data science team should communicate this information properly, so that all parties are aligned and agree to proceed with the implementation of the solution.

## Stage 3: Implementation

This is the stage where the code from the Jupyter Notebooks is transformed into a set of automated data pipelines and services on production. The implementation process resembles a standard software engineering workflow. It doesn't involve the high uncertainty typical for the research stages. For this reason, the data science team at this stage can be managed as any other software engineering team. Often the work at this stage is delegated to engineers who specialize in bringing machine learning solutions to production - MLOps.

The following __deliverables__ can be expected from the implementation stage:

- Data pipelines and services working on production
- Monitoring mechanisms
- Technical documentation

## Stage 4: Maintenance

This is a long running stage typical for any software product. The data science team has the responsibility of maintaining the data pipelines and services. The activities included are: monitoring of the solution; health checkups; bug fixing; client support; performance improvements; refactoring; etc.

An important phenomenon to keep in mind during the maintenance phase of machine learning products is the so-called __data drift__. A machine learning model is always designed based on some assumptions about the input data. If those assumptions change over time, the performance of the model might decrease. For example, imagine that in Dianne's project the predictive models were designed with the assumption that the air temperature in the factory is always 20&deg;C (68&deg;F). For some reason, after one year the air temperature has decreased to 15&deg;C (59&deg;F). This temperature change can cause changes in the working life of the factory equipment and the ML models would have to be redesigned.

From a management perspective, the data science team at this stage is not very different from any other team of software engineers. The only difference might appear, if the data science team would need to redesign the machine learning models, for example, due to data drift. In such cases, the project might have to go through the 4 stages all over again.

## Conclusion

Understanding the 4 stages of a data science project can help team managers to gain the most value from their data science team. During the conceptual research the exploration process can be optimized by reducing the bureaucratic bourdain. During the technical research the iterative experimentation process should be kept in check by setting time constraints. During the implementation and maintenance stages the data science team can be managed as any other software engineering team. It is important to keep in mind the possible data drift that may occur during the maintenance stage. For big projects, it is common that multiple streams of the project go in parallel through the 4 stages, independently from each other.

## References

<a name="ref-1"></a>[1] Ries, Eric. [The Lean Startup](https://en.wikipedia.org/wiki/The_Lean_Startup){: target="_blank"}, 2011
