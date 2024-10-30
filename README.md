# IPCK

## Environment
Code demo for paper ```A commit classification framework incorporated with Prompt tuning and external Knowledge```
In order to easily reproduce our method, we use ```pip freeze > requirements.txt``` to output the packages used in our experimental environment.
you can try ```pip install -r requirements.txt``` to obtain the similar environment with us.

### You should also download Hugginface models, if you are facing the VPN issue. Please download the models by running req.py
. 
## Datasets
The datasets we used can be found from the dataset folder 
Commit_datasets.csv is the dataset with 3 labels, you can also find download it straight from https://zenodo.org/record/4266643#.X6vERuLPxPY

negative+CC-900repos and positive+CC-900repos are the dataset with 2 labels, you can also find download it straight from https://github.com/davidleejy/wnut21-cotrain. And we concatenated and randomly shuffled them as dataset.csv 

### The file in the dataset folder is larger than GitHub's recommended maximum file size of 50.00 MB, so we have to use git lfs to manage them
Since the files in the dataset folder is big, you can't git clone this repo to directly get the dataset. You have to do this following commands in the terminal to fully get the datasets.
1. git lfs install
2. git lfs pull

## Experimental results
All experiment results are stored in the ```notebooks``` folder. The overall experiment result are in the ```E-All ``` folder.

The few-shot experiment results are in the ```E-5,E-10,E-15,E-20,E-50``` folders.  For example, the folder with the name E-2-5 means, the E(experiment) result on Dataset II (Single-label multi-class classification) with 5 shots(5 samples for each label). 

The ablation study results are shown in  ```M-BASE-PKG_I, M-Flan-T5-PKG_I , K-BASE-PKG_I and K-Flan-PKG_I``` , where  ```M-BASE-PKG_I``` stands for pipeline with T5 model and no knowledgeable_verbalizer, while K-Flan-PKG_I stands for pipeline with FLAN-T5 and knowledgeable_verbalizer.
 
To test the performance of multi-task, we first merged the two datasets, expanded the knowledgeable verbalizer, and finally conducted experiments on the test set of {Dataset}_{II}, the code are shared in https://github.com/AppleMax1992/IPCK/blob/master/notebooks/E-All/K-Flan-PKG_Unified.ipynb.  However, the results were not ideal. Therefore, we still adopted the method of separate training.

