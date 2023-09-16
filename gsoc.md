
# DFlow: Textual DSL for Rapid Virtual Assistant Development

  

## Google Summer of Code 2023 - Final Report



- ****Developer:**** [Haralabos Metaxas](https://github.com/harabalos)

- ****Mentor:**** [Nikolas Malamas](https://github.com/malamasn)
- ****Organisation:**** [GFOSS - Open Technology Alliance](https://github.com/eellak/)
-  ****Central Repository:**** [DFlow ](https://github.com/robotics-4-all/dFlow)
- ****Contributions:**** [OpenApi-to-Dflow](https://github.com/robotics-4-all/dFlow/pull/6)


## Table of Contents

1. [Project Overview](#project-overview)

2. [Objectives and Learnings](#objectives-and-learnings)

4. [Future Work](#future-work)

---
### Project Overview

  
Dflow is a DSL that is used to define and generate task based dialogue flows for virtual assistants. It's designed to be user friendly, flexible, and extensible, allowing developers to easily specify intents, services, and responses for a variety of use cases. It can generate complete Rasa models while supporting dynamic REST requests.

 

As a result, developers have the opportunity to produce intelligent virtual assistants easier and quicker, which are able to interact with users in a more natural and intuitive way.

  

During the course of the GSoC 2023, my main task was the development of  ****OpenAPI-to-dFlow M2M transformation**** and an extension of that was to create a ****Automation of intent examples creation from OpenAPI description****. To accomplish this, a new metamodel was required that could use the OpenAPI Specification, which has standardized all REST web services, and the corresponding OpenAPI-to-dFlow Model-to-Model (M2M) transformation component. This way developers will be able to build complete dFlow models for VAs by defining REST endpoints using the OpenAPI specifications enriched with optional VA-specific parameters.

---


### Objectives and Learnings

  *****M2M Transformation from OpenApi to Dflow*****
- At the beggining of the project, it was clear that i had to deep dive into APIs, learn all about the documentation, structure and operation. I researched, tested and did experiments on RESTfull APIs and later i focused on the OpenApi Specification. I had to know what it is at first in order to be able to transform it into another form.

- After that, i knew i wanted to find a tool to build a bridge between OpenApi and dFlow. With the help of my mentor, he told me that i should learn and implement Jinja template language. That would read the Specification from the OpenApi and transform into this DSL's grammar. 

- The journey took a turn to NLP, as i focused on learning deeply and understanding it at its core. What is it? What does it do? Those questions came to me when i started wondering how my code would automatically know in what entity the wanted word in the given intent example belonged. So, I learned to effectively use spaCy, a leading library in NLP.

*****Automation Of Intent examples*****

- Next Objective was the creation of different sentences a user would ask a chatbot his intent, based on the description of the operation. To do that the only way was for a Large Language Model (LLM) to handle it. I learned a lot about LLMs as i researched a bunch of them in the [Hugging Face platform](https://huggingface.co/). After reviewing, testing and running, i saw that the best one was the [falcon-instruct](https://huggingface.co/tiiuae/falcon-7b-instruct) model, where i created a prompt with few-shot examples, it ended up beautiful, the model could create diverse and human-like text. 

- The next logical step was crafting human-like responses that a chatbot would provide. Leveraging the power of the falcon-instruct model, I not only created intuitive prompts but also managed to formulate responsive and engaging replies. 

*****Git/Github/Coding*****
- As the project progressed, I found myself writing code faster, better and more fluently than before, as this program refined my Python coding abilities. Engaging with various libraries and frameworks, understanding the coding patterns, and implementing optimized solutions became a part of my improved skill set.

- Additionally, I learned a lot about Git/Github and open source in general as I picked up essential skills for managing and contributing to big projects. These are skills that, I've realized, are crucial for any developer, no matter what kind of project they are working on.
---
### Future Work
- Support OpenApi 3.x
- Mapping between OpenApi paths and dFlow intents
- Handle Non-required Parameters
- Enhanced Error Handling and Reporting
- Create a way automate header parameters
- Cloud Deployment

Special Thanks to my mentor Nikolas. Whether through messages or video calls, he was always there to assist and guide me.

After the Gsoc program, i will stay on the dFlow team and continue contributing and evolve the project! 🚀

  

---

  

