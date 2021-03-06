# List of contributors
1. Abin Pilot
2. Anjima S
3. Arya S Nair
4. Harisankar B
5. Joseph Francis Pellissery
6. Rekhil C R

College: Rajiv Gandhi Institute of Technology, Kottayam

## Problem Statement
As the pandemic goes by, psychological state has become a vital side of our daily lives. Individuals still become a vital side of our daily lives. Individual still don't feel comfortable to speak to people regarding their psychological state and frequently tend to keep their isues to themselves this typically results in the build-up stress in their minds.

## Personas of the system

The software system is mainly created for users who are facing mental stress and loneliness. 

![Use Case Diagram](https://github.com/josephfrancis-07/Mental-Health-Chat-Bot/blob/main/Use%20Case%20Diagram.jpg)

# RASA-Mental-Health-Chatbot

Mental health chatbot developed in RASA Framework, to analyse person's chances of mental illness on the basis of survey questionnaire. Have a fun conversation with the bot and upplift your mood!

# Made using RASA Framework

RASA is an open-source framework used to Build contextual AI assistants and chatbots in text and voice with open source machine learning framework.

# Mental Health Chatbot development and Getting Started with RASA:


## Rasa Architecture

The diagram below provides an overview of the Rasa Open Source architecture. The two primary components are Natural Language Understanding (NLU) and dialogue management.

NLU is the part that handles intent classification, entity extraction, and response retrieval. It's shown below as the NLU Pipeline because it processes user utterances using an NLU model that is generated by the trained pipeline.

The dialogue management component decides the next action in a conversation based on the context. This is displayed as the Dialogue Policies in the diagram.

![Architecture Of Rasa](https://github.com/josephfrancis-07/Mental-Health-Chat-Bot/blob/main/Arch.jpg)

RASA Installation and Setup
#1. Install RASA
### Prerequisite:
    1. Download Anaconda Prompt 
    2. Download Microsoft build tools here.
    3. Create a directory on your system where you would like to store your Rasa project.

Once all of that has been done, open the Anaconda Prompt application and ???cd??? into the directory you created, mine is called ???RasaBot???.


1. Create a virtual environment using the command below.
    conda create -n rasavirtualenv python=3.6


2. Activate your environment using the command
    conda activate rasavirtualenv


3. Install Rasa Open Source.
    pip install rasa


## 2. Setup the  project
rasa init:
>command creates a new Rasa project in a local directory, which you will specify by providing the directory name.


Rasa will automatically populate it with the project files and example training data, and it will train the NLU and dialogue models. By default, rasa init trains a simple assistant called moodbot which will ask how you feel, and if you are unhappy it will try to cheer you up by sending you a picture of a cute tiger cub.


RASA Components
1. __init__.py
>Initiates the directory containing the packages required for running the chatbot.


2. endpoints.yml:
>This contains the different endpoints the chatbot can utilize. One of the important endpoints is action_endpoint which exposes the chatbot to the Custom Action server and the UI.


3. domain.yml:
>Defines the boundaries (environment) of the chatbot and the guidelines on how the chatbot should function. Some key aspects of the domain file are entity, intents, responses, actions, slots, session_config. Entities are keywords used to identify and extract useful data from inputs, like users??? names.


4. credentials.yml:
> As the name suggests, this file is used to store the details (credentials) of various connected services.

5. config.yml:
> This file contains the configuration we set up for our NLU and Core models. Policies, pipelines, etc are defined here.

6. actions.py:
> This file contains the main logic of the chatbot. Actions define the responses of the chatbot.
Actions are the things your bot runs in response to user input. There are three kinds of actions in Rasa Core:
i. default actions (action_listen, action_restart, action_default_fallback)
ii. utter actions, starting with utter_, which just sends a message to the user.
iii. custom actions ??? any other action, these actions can run arbitrary code

7. models:
> This folder stores the trained models.

8. data:
> This is the brain of the chatbot. The context, learning, and improvement help with the files existing in the data folder. What are those files, you ask? They are nlu.md and stories.md

9. nlu.md:
> This file contains the training data. Natural Language Understanding is the name given by RASA which helps turn User Messages into structured data. Basically, these are the samples (and examples) which we can expect the user may input. The NLU training data also labels the entities, or important keywords, the assistant should extract from the example utterance. In each intent, are defined examples of user utterances, entities, and how to respond. Basically, intents are labels that represent the goal or meaning, of a user???s specific input. nlu.md basically consists of intent examples ie user input

10. stories.md:
> This file contains the conversational flow of the chatbot and the user, which we have defined (trained). Stories are examples of end-to-end conversations. These are important in deciding the next action of the chatbot. Dialogue Management can be the term used to loosely define stories.md.
Stories are basically dialog flow of the chatbot
