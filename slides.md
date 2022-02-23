---
theme: purplin
title: DDD Cognitive Load

---
## MySQL Performance and Indexing

We can alter the MySQL configuration like so:

```
/etc/my.cnf
slow_query_log_file             =/var/log/mysqld.log.slow
slow_query_log                  = 1
long_query_time                 = 5
log_queries_not_using_indexes   = 1
log_slow_verbosity              = explain
```

EXPLAIN command

```
CREATE INDEX `CustOrderOfferID` ON `CustomerOrder` (`OfferID`);
```
---
layout: default
---

# Team Cognitive Load

Making life easier for everyone

---
layout: default
---

# What is Cogitive Load?

## Intrinsic cognitive load
Relates to aspects of the task fundamental to the problem space (e.g., “What is the structure of a Java class?” “How do I create a new method?”)


---
layout: default
---

# What is Cogitive Load?

## Intrinsic cognitive load
Relates to aspects of the task fundamental to the problem space (e.g., “What is the structure of a Java class?” “How do I create a new method?”)

## Extraneous cognitive load
Relates to the environment in which the task is being done (e.g., “How do I deploy this component again?” “How do I configure this service?”)

---
layout: default
---

# What is Cogitive Load?

## Intrinsic cognitive load
Relates to aspects of the task fundamental to the problem space (e.g., “What is the structure of a Java class?” “How do I create a new method?”)

## Extraneous cognitive load
Relates to the environment in which the task is being done (e.g., “How do I deploy this component again?” “How do I configure this service?”)

## Germane cognitive load
Relates to aspects of the task that need special attention for learning or high performance (e.g., “How should this service interact with the ABC service?”)

---
layout: default
---

# What is Cogitive Load?

## Summary
Intrinsic -- Skills/Technology

Extraneous -- Company and Systems

Germane -- How does THIS app or solution work

---

# What is Team Cogitive Load?
* How much &ldquo;extra&rdquo; thinking is required to complete a project.

* Causes
    - **Intrinsic load** from mismatched skillset for tasks
    - **Extraneous load** from not having thin, easy or consitent platforms.
    - **Germane load** from lead developers having everything in thier head and no big picture communication.
    - This germane load spills into cognitive load for Tech Support

---

# What are the effects of high congitive load?

* Prioritization is hard, and the frequent context switching even throughout a single sprint leads to a dip in people’s motivation.

* Split Attention Effect (all parties)

* Cost/Time overuns

* Bottlenecks

---

# What are the effects of high congitive load?

## Reduced motivation

This is not surprising if we consider the three elements of intrinsic motivation: *autonomy* (quashed by constant juggling of requests and priorities from multiple teams), *mastery* (“jack of all trades, master of none”), and *purpose* (too many domains of responsibility).

---

# Where do we fail now?
* Big Picture communication
* Old Monoliths like Incom/DeBrand/Board&Brush
* No legacy metamemory

---

# How do we improve?
* Reduce **Intrinsic Load** by improving overall skillset

https://docs.google.com/forms/d/1dLb-HFs4raqs84pYphlJLKkmjN22tImw2pozvXSAUJA/edit

---

# How do we improve?
* Reduce **Extraneous Load** by continuing to improve process, consitency and plaforms.
    - Tiffany's Efforts / Trello / Jira
	- Ferg Framework
	- Ferg Local
	- Git / Version Control
	- Cypress Testing

---

# How do we improve?
* Reduce *Germane Load* by committing specific developer in-brain memory to metamemory (writing it down)
    - Wiki
	- Trello

---

# How do we improve?
* Reduce *Germane Load* by committing specific developer in-brain memory to metamemory (writing it down)
    - Wiki
	- Trello

## Coming Soon:
Architecture Diagrams
* Data Flow
* Entity Relationship
* UML

---
layout: center
---
# Late Binding
## Reducing Cognitive Load

---
layout: default
---
# Early vs Late Binding

* Early Binding -- Software knows what the data is and what format and purpose is, (Monoliths)
* Late Binding -- Software is agnostic to form and use of data. (Microservices)

---
layout: default
---
# Late Binding Pros and Con

## Pros
* Late binding reduces team cognitive load
* Late binding is more flexible and reusable saving  development time

## Con
* Late binding has poorer performance than an early bound method call.
---

# Late Binding Examples

* Hadoop and NoSQL have no schema till they are used.
* Microservices - "Extreme Late Binding"
* This is why style and content should not be mixed. Why HTML should be semantic.
	
---

# Comparisons

* Monoliths vs Microservices
* Monoliths are generally not reusable
* Monoliths perpetuate side-effects
* Microservices: Software that fits in our heads.

---

# Software that fits in our heads

* Doesn't have to be microservices, can be object oriented. Thsi was the point of object oriented.

* How many verbs are you using to descibe the thing?

* Avoid Host Affinity
    * No assumptions can be made about the host on which the service would run.

* Design with server deployment in mind.

* Design a Well-Defined Entry Point and Exit Point
    * Well documented contract. Success/failure need to be consistent.

---


# Software that fits in our heads (cont&lsquo;d)


* Functions should have one verb.

* Don't over modularize = greater cognitive load.

* Do Not Share Libraries or SDKs between microservice
    * Don't repeat yourself.
	* Updates have bad side effects

* Build the thinnest viable platform
    * Can Just be a Wiki page that tells about consistency.




