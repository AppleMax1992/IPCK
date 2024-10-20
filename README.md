# CommitFit

## Environment
Code demo for paper ``A commit classification framework incorporated with Prompt tuning and external Knowledge''
In order to easily reproduce our method, we use ```pip freeze > requirements.txt``` to output the packages used in our experimental environment.
you can try ```pip install -r requirements.txt``` to obtain the similar environment with us.

You should also download Hugginface models, if you are facing the vpn issue. Please download the models by running req.py
. 
## Datasets
The datasets we used can be find from the dataset folder 
Commit_datasets.csv is the dataset with 3 labels, you can also find download it straight from https://zenodo.org/record/4266643#.X6vERuLPxPY

negative+CC-900repos and positive+CC-900repos are the dataset with 2 labels, you can also find download it straight from https://github.com/davidleejy/wnut21-cotrain. And we concatenated and randomly shuffled them as dataset.csv 

### The file in the dataset folder is larger than GitHub's recommended maximum file size of 50.00 MB, so we have to use git lfs to manage them
Since the files in the dataset folder is big, you can't git clone this repo to directly get the dataset. You have to do this following commands in the terminal to fully get the datasets.
1. git lfs install
2. git lfs pull

## Expermental results
All experiment results are stored in the notebook folder, for example, the folder with the name E-2-5 means, the E(experiment) result on 2(dataset with 2 labels) with 5 shots(5 samples for each label). 



