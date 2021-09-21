This is a Python implementaion for Jupyter/Colab Notebooks of "Countermeasures against Backdoor Attackstowards Malware Detectors".

The datasets used in our validation (EMBER) are not included in the repository.

You can download the dataset from https://github.com/elastic/ember

### How to produce our results in our manuscripts

1.  Please prepare an EMBER dataset consists of 2351-dimensional features extracted from the EMBER 2018 (version 2) dataset.
2.  Run each cell of ```ae_against_backdoor.ipynb``` sequentially.
3.  By adjusting the values of the following variables, you can change the backdoor generation algorithm to be used, etc.

### Variables

* ```algType``` : ```1``` for Independent Selection Attack, ```2``` for Greedy Combined Selection Attack, and ```3``` for FGSM-based Label-flip Attack. 
* ```encOnly``` : ```False(default)``` to generate surrogate data by feeding through both the encoder and decoder, ```True``` to generate surrogate data using only the encoder.
* ```epsilon``` : The noise parameter $\epsilon$ in the FGSM attack.
* ```p``` : Number of poisoning data to be added to the training data. 
* ```N``` : Number of backdoor dimension.
* ```nShap``` : Number of training data sampled to construct a simplified model for SHAP.
