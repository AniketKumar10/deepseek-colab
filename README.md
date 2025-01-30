# deepseek-colab

## Overview

deepseek-colab is a **free to use** Jupyter Notebook designed to set up and interact with the Ollama API for running the DeepSeekR1_14B model. This notebook facilitates the installation of necessary packages, configuration of the Ollama server, and demonstrates generating responses using the Ollama API.

## Prerequisites

- **Operating System**: Windows
- **Python**: 3.11 or higher
- **Jupyter Notebook**: Installed and configured
- **GitHub Account**: To access the repository
- **Ollama API Access**: Ensure you have the necessary access to use the Ollama API.

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/AniketKumar10/deepseek-colab.git
    ```
2. **Navigate to the Project Directory**
    ```bash
    cd deepseek-colab
    ```
3. **Install Required Python Packages**
    ```bash
    pip install -r requirements.txt
    ```
4. **Set Up Ollama**
    - Install the Ollama package:
        ```bash
        pip install ollama
        ```
    - Install `pciutils` using apt:
        ```bash
        sudo apt install pciutils
        ```
    - Download and run the Ollama installation script:
        ```bash
        curl -fsSL https://ollama.com/install.sh | sh
        ```

## Usage

1. **Open the Jupyter Notebook**
    - Launch Jupyter Notebook from your terminal:
        ```bash
        jupyter notebook
        ```
    - Open `DeepSeekR1_14B.ipynb` from the browser interface.

2. **Run the Notebook Cells Sequentially**
    - The notebook will install necessary packages, set up the Ollama server, and demonstrate generating a Fibonacci series using a recursive function up to F(40).

3. **Interact with the Ollama API**
    - The notebook includes code snippets to interact with the Ollama API, start the server, list available models, and generate responses.

## Features

- **Environment Setup**: Automatically installs and configures required packages and dependencies.
- **Ollama Server Management**: Starts the Ollama server as a subprocess for seamless API interaction.
- **Model Interaction**: Lists available Ollama models and demonstrates generating responses using the DeepSeekR1_14B model.
- **Fibonacci Series Example**: Provides a practical example of solving the Fibonacci series using a recursive function via the Ollama API.

## License

This project is licensed under the MIT License.