# Online Health Enquiry Chatbot (STAT4011 Group Project)
<br>

if you want to reproduce the project, you need to ADD OPENAI API KEY in .env

**Code description**
- main.py used for run the project.
- api.model is to ask for the response of the model through api.
- tree_model_medicine.py is the code to implement the symptoms to disease prediction, it receive the input from user and provide the feedback.
- input_process.py is the intermediate program to decide the version of model (tree/API)
- gui.py is the PyQt5 class to generate GUI.
- disease_prediction_model_generator.py is the file to generate the pretrained models.
- .env is used for store the API key (PLEASE add your own OPENAI API key in this file)
- inference_model_training.ipynb is model selection process in the chatbot development. (Not used)
<br>

1. Create a conda virtual environment
```bash
conda env create -f environment.yml
```
Then activate the virtual environment
```bash
conda activate medical_chatbot
```
if you want to exit the virtual environment
```bash
conda deactivate
```
<br>

<!-- 2. Run api_generate.py to generate the GLOVE model we used in the program. The model will be prepared under the directory ./working -->

2. Run the main.py to use the chatbot

