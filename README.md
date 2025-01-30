# deepseek-colab

## Hey there!

Welcome to **deepseek-colab**! 🎉 This is a **free-to-use** Jupyter Notebook that helps you set up and interact with the awesome Ollama API using the DeepSeekR1_14B model. Whether you're a beginner or a pro, this notebook makes it super easy to get started with one of the best open-source models out there.

## What You Need Before You Start

Before diving in, make sure you have the following:

- **Operating System**: Linux or Windows
- **Python**: 3.11 or higher (because who wants outdated stuff?)
- **Jupyter Notebook**: Installed and ready to go
- **GitHub Account**: To clone the repo and maybe contribute
- **Ollama API Access**: Get the keys you need to use the Ollama API

## Let’s Get This Going!

Follow these simple steps to set everything up:

1. **Clone the Repository**

    ```bash
    git clone https://github.com/AniketKumar10/deepseek-colab.git
    ```

    **Or Use Google Colab**

    - Go to [Google Colab](https://colab.research.google.com/).
    - Click on **File** > **Open notebook**.
    - Navigate to the **GitHub** tab and enter the repository URL:
        ```
        https://github.com/AniketKumar10/deepseek-colab.git
        ```
    - Select `DeepSeekR1_14B.ipynb` and click **Open**.

2. **Navigate to the Project Folder** (if running locally)

    ```bash
    cd deepseek-colab
    ```

3. **Install the Python Packages You Need**

    ```bash
    pip install -r requirements.txt
    ```

4. **Set Up Ollama**

    - Install the Ollama package:

        ```bash
        pip install ollama
        ```

    - Install `pciutils` (you might need administrator rights):

        ```bash
        sudo apt install pciutils
        ```

    - Run the Ollama installation script:

        ```bash
        curl -fsSL https://ollama.com/install.sh | sh
        ```

## How to Use This Notebook

Using **deepseek-colab** is as easy as following the commands in the notebook. Here's a quick rundown to show you how simple it is:

1. **Open the Notebook**

    - **Locally**:
        - Launch Jupyter Notebook from your terminal:
            ```bash
            jupyter notebook
            ```
        - Open `DeepSeekR1_14B.ipynb` from the browser that pops up.
    - **Or Use Google Colab**:
        - Follow the steps in the "Let’s Get This Going!" section to open the notebook in Google Colab.

2. **Run the Cells One by One**

    - **Installation Cells**:
        - The first few cells handle installing necessary packages. Simply run them:
            ```bash
            !pip install ollama
            !sudo apt install pciutils
            !curl -fsSL https://ollama.com/install.sh | sh
            ```
        - These commands set up the Ollama environment effortlessly.

    - **Start the Ollama Server**:
        - Run the cell to start the server:
            ```python
            import subprocess
            process = subprocess.Popen("ollama serve", shell=True)
            ```
        - This command initializes the Ollama server in the background.

    - **Interact with the API**:
        - List available models:
            ```bash
            !ollama list
            ```
        - Generate responses using the DeepSeekR1_14B model:
            ```python
            from ollama import chat
            from ollama import ChatResponse

            response: ChatResponse = chat(model='deepseek-r1:14b', messages=[
              {
                'role': 'user',
                'content': 'use a recursive function to solve a Fibonacci series considering f(40)',
              },
            ])
            print(response['message']['content'])
            # or access fields directly from the response object
            print(response.message.content)
            ```
        - These commands demonstrate how you can effortlessly generate complex computations using the API.

3. **Enjoy the Simplicity**
    - With each command clearly laid out in the notebook, you can easily follow along without any hassle. Whether you're setting up the environment or generating responses, everything is just a few clicks away!

## Cool Features

- **Easy Setup**: Automatically installs and configures everything you need.
- **Server Management**: Starts the Ollama server in the background so you don’t have to worry about it.
- **Model Interaction**: Check out all available Ollama models and see how DeepSeekR1_14B stacks up.
- **Practical Examples**: Learn by doing with examples like generating a Fibonacci series using recursion.

## Why Choose deepseek-colab?

We believe in making powerful tools accessible to everyone. With deepseek-colab, you get a seamless experience running one of the top open-source models without any hassle. Perfect for your projects, experiments, or just exploring what AI can do!

## License

This project is licensed under the MIT License. Feel free to use, modify, and share as you like!

## Let’s Connect

Got questions or feedback? Feel free to [open an issue](https://github.com/AniketKumar10/deepseek-colab/issues) or reach out!

Happy Coding! 🚀