---
title: Using C4 modeling for cloud diagrams
date: 2023-02-09 12:00:00 +GMT
categories: [archetypes, architect-role]
tags: [architecture, diagrams]
author: h_s
toc: true
comments: true
math: true
mermaid: true
# img_path: /img/path/
pin: true

---

> Bridging C4 Software Architecture Modeling with AWS Cloud Infrastructure Diagrams

In my experience, applying the C4 model to AWS architecture design is highly effective.
It gives teams a shared language from high-level context down to implementation detail.

The model has four levels:

1. Context (C1)
2. Container (C2)
3. Component (C3)
4. Code (C4)

For cloud architecture work, C1 to C3 are usually the most useful.

![Desktop View](/assets/img/posts/2023-02-09-using-c4-for-aws-cloud.png){: width="972" height="589" .w-50 .left}  

## How I map C4 to AWS

| C4 level | Purpose | Typical AWS view |
|---|---|---|
| C1 Context | Show system boundaries and external actors | Users, external APIs, identity providers, partner systems |
| C2 Container | Show deployable units and communication | ECS services, Lambda functions, API Gateway, databases |
| C3 Component | Show internals of each container | Microservices, queue consumers, domain modules, storage adapters |

### C1: Context first

At C1, I focus on scope and relationships.
This helps non-technical stakeholders quickly understand what the system does and where it integrates.

### C2: Deployment and communication

At C2, each container maps to cloud runtime choices.
For example, a web API might run on ECS, while an event processor runs on Lambda.
This is where network boundaries and data flow become explicit.

### C3: Internal design quality

At C3, I model the components inside each container:
handlers, domain services, data access layers, and messaging flows.
This level is ideal for engineering discussions about ownership, coupling, and reliability.

## Why this works well

Using C4 for AWS gives teams a path from idea to implementation without losing clarity.
It improves communication across product, engineering, platform, and operations teams.

> Good architecture diagrams are not just pictures.
> They are decision tools.
{: .prompt-tip }
