# Botium Experiment
[CONGA](https://saraperezsoler.github.io/CONGA/) is a MDE solution to implement chatbots. It consists of:
- A DSL to define chatbot models
- A code generator for several chatbot development tools
- A recommender that suggests the best development tool based on the chatbot definition and a questionnaire about the technical requirement
- A parser from chatbot tools to the CONGA DSL

The repository contains the results of evaluations of the CONGA parser and code generator. To perform it, we take ten chatbots for [Dialogflow](https://dialogflow.cloud.google.com/) and ten for [Rasa](https://rasa.com/). [Here](https://github.com/Conga-dsl/ValidationSetup), you can find the models and DSLs of these chatbots as well as the locations of the original files. First, to evaluate the CONGA parser, we convert the chatbots into CONGA. To assess if CONGA is able to capture all its relevant details, we map them back to the original platform and compare its behaviour with runtime testing. Then, to evaluate the CONGA code generator, we migrate the Rasa chatbots to Dialogflow and vice-versa. To validate behaviour preservation we perform cross-validation testing.  

We have created the tests using [Botium](https://botium-docs.readthedocs.io/en/latest/) a black box testing tool that runs test scripts on the chatbot under test, and checks the obtained results with the desired ones.
The folder Botium test contains the created Botium test, and the results of its execution. The folder Generated Chatbots contains the generated chatbot in Rasa and Dialogflow for each chatbot. 
