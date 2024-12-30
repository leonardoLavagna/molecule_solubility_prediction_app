# melecule_solubility_app
![solubility-logo](https://user-images.githubusercontent.com/91341004/166319326-a10e6703-a670-4445-bc0b-3aa9d3b01e5f.jpg)

In this repository there is the surce code for the application `molecule_solubility_app` which allows the user to input a SMILE formula, e.g. the aspirin  CC(=O)OC1=CC=CC=C1C(=O)O, and it predicts its solubility (in log scale). We've trained a simple linear model to predict the solubility value from some features. 

### Use the app
Here is the link at the app: [https://moleculesolubilityprediction.streamlit.app](https://moleculesolubilityprediction.streamlit.app/). On the left hend side it is possible to input one ore more SMILE formula (divided by a newline) and then the system will provide the solubility prediction based on some molecular descriptors. Notice that at the beginning some default SMILE formula are provided.

### What's in here?
- The **dataset** I've worked on `delaney_solubility_with_descriptors.csv`
- **Configuration files** `packages.txt` and `requirements.txt` which are needed to deploy the app on Streamlit
- The **script** for the app `solubility-app.py`
- The **Jupiter Notebook** in which the linear model can be found `solubility-web-app.ipynb`
- The results of the trained linear model asi **pickle file** `solubility_model.pkl.
- A **logo** `solubility-logo.jpg

### Dataset 
The dataset we used for the training process is the following: *John S. Delaney. ESOL:  Estimating Aqueous Solubility Directly from Molecular Structure. J. Chem. Inf. Comput. Sci. 2004, 44, 3, 1000-1005.* Available here:[ESOL:  Estimating Aqueous Solubility Directly from Molecular Structure](https://pubs.acs.org/doi/10.1021/ci034243x) (*J. Chem. Inf. Comput. Sci.* 2004, 44, 3, 1000-1005). The dataset is in csv format with the following features:

- **MolLogP** (partition coefficient octane/wather) abbreviated as **LogP**
- **MolWt** (melecular weight) abbreviated as **MW**
- **NumRotatableBonds** (number of specific chemical bonds) abbreviated as **RB**
- **AromaticProportion** (aromatic proportion) abbreviated as **AR**
- **logS** (logarithm of the solubility)

The feature of interest is logS.

### Disclamair
This project was part of a bigger project I worked on with Unilab. I couldn't provide here all the results we obtained, but I've tryied to show here some important intermediate steps which I think can be valuable on their own.
