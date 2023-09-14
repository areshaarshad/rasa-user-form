# rasa-user-form

## Overview
This project showcases the development of a chatbot using the Rasa framework, specifically focusing on creating and handling forms. The chatbot is designed to gather essential user information through a conversational form, including name, phone number, email address, and date of birth.

## Features
- Form-based conversational flow: The chatbot engages with users in a structured conversation to gather specific information.
- User-friendly data collection: Users are prompted to provide their personal information in a clear and friendly manner.
- Data validation: The chatbot performs validation to ensure that the entered data is accurate and complete (i.e. date of birth format etc.).
- Database integration: User data is stored in a PostgreSQL database for future reference and analysis.
- Confirmation and submission: The chatbot confirms the data provided by the user and allows them to submit it.

## Prerequisites

Before running the chatbot, make sure you have the following prerequisites installed:

- [Rasa](https://rasa.com/docs/rasa/installation)
- [Python](https://www.python.org/downloads/)

## Project Structure

- `data/`: Contains training data for the Rasa chatbot.
- `actions/`: Contains custom actions and logic for handling user data.
- `config.py`: Configuration file for database and other settings.
- `domain.yml`: Defines the chatbot's domain, including intents, entities, and responses.
- `rules.yml`: Defines conversation rules for handling user interactions.
- `nlu.yml`: Contains NLU training data for intent recognition.

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Set up the Rasa environment and install the necessary dependencies.
4. Configure PostgreSQL database connection in the `actions.py` file.
5. Train the chatbot with the provided training data using the 'rasa train' command in the command prompt. 
6. Once the model is trained, start the rasa run actions server using the 'rasa run actions' command.
7. To interact with the bot, use the 'rasa shell' command.
8. The bot can be interacted with on Postman using 'http://localhost:5005/webhooks/rest/webhook'.
9. The bot stores user information in PostgreSQL (the command can be found on the `actions/` file). 

## Usage
This chatbot demonstrates the use of forms to collect user data. The user is prompted to provide their name, phone number, email address, and date of birth. Once the user confirms the data, it is saved to the PostgreSQL database. We can customize the conversation flow, responses, and database interactions according to our specific requirements.
