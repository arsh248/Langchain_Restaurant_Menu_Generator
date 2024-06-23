# LangChain Restaurant Menu Generator

This project is a web application that generates a restaurant name and menu items based on the selected cuisine using the Streamlit framework and LangChain library.

## Table of Contents
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Project Details](#project-details)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

## Description
The LangChain Restaurant Menu Generator allows users to select a cuisine from a sidebar and generates a fancy restaurant name along with a list of menu items. The application uses Google's Generative AI model to generate the content.

## Installation

1. **Clone the repository**
    ```sh
    git clone https://github.com/arsh248/Langchain_Restaurant_Menu_Generator.git
    ```

2. **Create and activate a virtual environment**
    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install the required packages**
    ```sh
    pip install -r requirements.txt
    ```

4. **Set up your Google API Key**
    - Create a file named `secret_key.py` in the project root and add your Google API key:
      ```python
      # secret_key.py
      GOOGLE_API_KEY = 'your-google-api-key'
      ```

## Usage

1. **Run the Streamlit application**
    ```sh
    streamlit run main.py
    ```

2. **Open the application in your browser**
    - The Streamlit application will open automatically in your default web browser. If not, navigate to `http://localhost:8501` to access the app.

3. **Generate restaurant name and menu**
    - Select a cuisine from the sidebar to generate a restaurant name and menu items.

## Project Details

### main.py
This is the main entry point of the application, which uses Streamlit to create a web interface:
- Displays a title for the application.
- Provides a sidebar for users to select a cuisine.
- Calls `langchain_helper.generate_restaurant_name_and_items` to generate and display the restaurant name and menu items.

### langchain_helper.py
This module handles the interaction with Google's Generative AI model to generate restaurant names and menu items:
- Sets up the Google API key for authentication.
- Defines the logic to generate restaurant names and menu items using LangChain's `LLMChain` and `SequentialChain`.

### secret_key.py
This file stores the Google API key required for accessing the Generative AI model:
- Contains a single line defining the `GOOGLE_API_KEY`.

## Technologies Used

### LangChain Framework
LangChain is a framework for developing applications powered by language models. It provides utilities for working with prompt templates, chains, and various language model integrations. In this project, LangChain is used to create sequential chains of prompts that generate restaurant names and menu items based on the selected cuisine.

### Google PaLM LLM Model
The Google PaLM (Pathways Language Model) is a generative language model that leverages large-scale transformer architecture. In this project, the model is accessed through the `GooglePalm` class in LangChain, utilizing the model `text-bison-001`. The model generates the restaurant name and menu items based on the provided prompts and the selected cuisine.

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

