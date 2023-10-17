## Experiment code for IPCK
This is the code demo for the paper ''Incorprating Prompt tuning for Commit classification with prior Knowledge(IPCK)''.In order to easily reproduce our method, we use pip freeze > requirements.txt to output the packages used in our experimental environment. you can try pip install -r requirements.txt to obtain the similar environment with us.
## Datasets
The datasets we used can be find from the dataset folder Commit_datasets.csv is the dataset with 3 labels, you can also find download it straight from https://zenodo.org/record/4266643#.X6vERuLPxPY

negative+CC-900repos and positive+CC-900repos are the dataset with 2 labels, you can also find download it straight from https://github.com/davidleejy/wnut21-cotrain. And we concatenated and randomly shuffled them as dataset.csv

You can validate the experiment result and our framework directly from one notebook. Each notebook is for one experiment result.  For example, in folder notebook/E-5, it means the experiments for 5 shots scenario.
