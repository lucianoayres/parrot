# 🦜 Parrot

![parrot-banner](https://github.com/lucianoayres/parrot/blob/main/images/banner_parrot.png?raw=true)

## Generate Custom PARAMETER Settings for Your AI Models

[What's Parrot? 🦜](#whats-parrot) · [Why Use Parrot? 🚀](#why-use-parrot) · [How Does It Work? ⚙️](#how-does-it-work) · [Who Is It For? 🎯](#who-is-it-for) · [How to Use 🛠️](#how-to-use) · [Using Nino with Ollama 🐶](#using-nino-with-ollama) · [Templates 📄](#templates) · [Examples 📂](#examples) · [License 📄](#license) · [Contribution 🤝](#contribution)

### What's Parrot? 🦜

**Parrot** is an AI model designed to help you effortlessly generate custom `PARAMETER` settings for Modelfiles used in [Ollama](https://github.com/ollama/ollama). By providing a prompt that describes the model or task you want to accomplish, Parrot outputs tailored `PARAMETER` content to include in your Modelfile, streamlining the creation of new models that perfectly fit your specific needs.

### Why Use Parrot? 🚀

-   **Simplify Configuration 🔧**: Automatically generate optimal `PARAMETER` settings based on your goals.
-   **Save Time ⏱️**: Eliminate the guesswork in configuring model parameters.
-   **Customized Output 🎨**: Receive `PARAMETER` settings tailored to your project's requirements.
-   **Seamless Integration 🔄**: Fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring a smooth workflow in model creation and deployment.

### How Does It Work? ⚙️

Parrot uses AI to interpret your prompt and generate the appropriate `PARAMETER` settings for your Modelfile. By understanding the nuances of your desired model or task, Parrot provides you with a set of parameters that optimize performance and output quality.

The generated parameters are based on the official list supported by Ollama's Modelfile specification. You can refer to the [Ollama Modelfile Documentation](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#parameter) for a comprehensive list of available parameters and their descriptions.

## Who Is It For? 👥

Parrot is ideal for anyone looking to optimize AI models:

-   **AI Developers 👩‍💻**: Streamlining the model configuration process.
-   **Data Scientists 📊**: Fine-tuning models for specific tasks.
-   **Machine Learning Enthusiasts 🤖**: Experimenting with different model parameters.
-   **Educators 👨‍🏫**: Teaching about AI model configuration and optimization.
-   **Researchers 🔬**: Optimizing models for experimental purposes.

## How to Use 🛠️

Follow these steps to use Parrot and generate custom `PARAMETER` settings for your Modelfiles:

### 1. Clone the Repository

```bash
git clone https://github.com/lucianoayres/parrot.git
cd parrot
```

### 2. Ensure Ollama is Installed

Make sure you have [Ollama](https://github.com/ollama/ollama) installed on your system. Installation instructions can be found in the [Ollama GitHub repository](https://github.com/ollama/ollama).

### 3. Create the Parrot Model

```bash
ollama create parrot1.0 -f ./modelfiles/Parrot1.0
```

### 4. Run Parrot

```bash
ollama run parrot1.0
```

### 5. Provide Your Prompt

When prompted, input a description of the model or task you want to accomplish. For example:

```
I need a model that generates creative and imaginative storytelling with high variability.
```

### 6. Review the Output

Parrot will output custom `PARAMETER` settings tailored to your description. For example:

```
temperature 1.0
top_p 0.95
top_k 60
repeat_penalty 0.8
```

These parameters correspond to those defined in the [Ollama Modelfile specification](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#parameter). Each parameter adjusts specific aspects of the model's behavior to suit your needs.

### 7. Update Your Modelfile

Copy the generated `PARAMETER` settings and include them in your Modelfile to optimize your model according to your requirements.

## Using Nino with Ollama 🐶

You can also use [**Nino**](https://github.com/lucianoayres/nino-cli) to interact with your Ollama models more efficiently. Nino allows you to send prompts directly to the models from the command line and export the AI's response to a local file.

### Example Command

```bash
nino "I want a model that excels in factual accuracy for educational content." --model parrot1.0 --output parameters.txt
```

## Templates 📄

### Structure 🏗️

The Parrot model file templates streamline parameter generation by organizing key components, making it easy to configure and customize AI models while ensuring compatibility with Ollama. The structure includes:

1. **Objective and Rules** 📜: Defines the assistant's purpose and lays out guidelines to ensure the generated output meets your needs.

2. **Command Specification** 📝: Details essential commands used in a Modelfile, such as:

    - **META**: Contains metadata about the Modelfile, added as comments.
    - **FROM**: Specifies the base model version (e.g., `llama2`). See [Ollama's Modelfile documentation](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#from) for more details.
    - **PARAMETER**: Sets model parameters like `temperature`, `top_p`, and `repeat_penalty`. Refer to the [`PARAMETER` section](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#parameter) for the full list of parameters and their descriptions.
    - **MESSAGE**: Provides initial messages or prompts for the assistant.
    - **LICENSE**: Includes licensing information for the Modelfile.

3. **Template and Configuration** 🧩: Offers a standard Modelfile template with placeholders (`<< >>`) that can be customized based on your specific idea, goal, or problem.

4. **User Input** 💡: The specific idea, goal, or problem to generate the most effective output.

### Using Modelzilla to Generate Custom AI Models

We recommend using [**Modelzilla**](https://github.com/lucianoayres/modelzilla) to generate custom-tailored AI models based on the parameters generated by Parrot. Modelzilla can help you create Modelfiles for your specific tasks, allowing you to build personalized AI assistants perfectly suited to your needs.

By combining Parrot and Modelzilla, you can streamline the process of defining tasks and creating custom AI models, enhancing productivity and efficiency.

### Prompts

The original prompt templates are available for reference in the [prompts directory](./prompts). These resources are valuable for understanding the structure of Modelfiles and can serve educational purposes.

## Examples 📂

### Example Prompts 📝

Here are some examples of prompts you can provide to Parrot:

-   **Creative Writing Model**: "I need a model that generates imaginative and creative stories."
-   **Technical Documentation Model**: "I want a model optimized for generating clear and concise technical documentation."
-   **Chatbot Model**: "I need a model for a customer service chatbot that provides accurate and helpful responses."

#### Output Examples

For the prompt "I need a model that generates imaginative and creative stories," Parrot might output:

```
temperature 1.0
top_p 0.95
top_k 60
mirostat 0
repeat_penalty 0.8
```

For the prompt "I want a model optimized for generating clear and concise technical documentation," Parrot might output:

```
temperature 0.5
top_p 0.7
top_k 40
mirostat 1
mirostat_tau 5.0
repeat_penalty 1.2
```

For detailed explanations of these parameters, please refer to the [`PARAMETER` section of the Ollama Modelfile documentation](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#parameter).

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution 🤝

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.
