# Online Health Enquiry Chatbot (STAT4011 Group Project)
<br>

if you want to reproduce the project, you can use git clone to get the source code.

**For developers: I will try to improve the quality of the chatbot by**
-  Use XGBoot or simple NN or parameter tuning to further increase the symptoms -> disease prediction accuracy.
-  The current logic of the code is comparing the query similarity with symptoms keywords. Then use the predicted symptoms keywords to predict the disease. Then the output will simply follow the template hard-coded. Clearly, in this kind of design, the accuracy of the code will decrease. May be change the format from one-round QA to multi-round QAs or symptoms label selection by users will be a better choice (模仿网络天才，连环猜，超出一定阈值就返回，是这个吗？不是就继续随机抽没问过的一个症状再确认，或者抽几个概率最大的病里的症状问). I will update the source code recently.
-  The current design only support symptoms -> disease, but not other questions. We can train a question topic classifier (with training set generated by ChatGPT) or just apply the multi-round QAs setting.
-  For LLM-related models, probably we can buy some ChatGPT-3.5 turbo APIs from taobao or use free API (openGML). Then simply plug in the prompt with user's query or labels to get the output.

**Code description**
- traditional.py is the code to implement the symptoms to disease prediction
- input_process.py is the intermediate program to decide the version of model (traditional/advanced)
- GUI.py is the PyQt5 class to generate GUI.
- disease-symptom-prediction-ml-99.ipynb is the visualization and model selection part in the chatbot development,
  it will produce the working/random_forest.joblib model which is called in traditional.py. You may generate your own model in the notebook.
  It would not be used in the chatbot
  (是从Kaggle上抄的。后面再改改)


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

2. Run api_generate.py to generate the GLOVE model we used in the program. The model will be prepared under the directory ./working

3. Run the main.py to use the chatbot

