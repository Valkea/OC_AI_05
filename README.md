# Customer Segmentation ("Segmentez des clients d'un site e-commerce")

[This project is part of the AI Engineer cursus on OpenClassrooms]

We are provided with a dataset from [Olist](https://www.kaggle.com/olistbr/brazilian-ecommerce) which contains informations of about 100 000 orders.

The data are dispatched accross 8 datasets:
![alt text](medias/olist_datasets.png)

> The goal is to find an interesting customer segmentation that can help the marketing department to tailor and send approriate offers to the clients.
> However, given the nature of the project, we also need to be able to check for the model or data-drifting over time.

1. At first, we will conduce and EDA (01_EDA.ipynb)
2. Then we will test several models to find those that best work with the dataset (02_Clustering)
3. Finally, we will try to study the performance degradation in order to decide the frequency of the re-training (03_DataDrift.ipynb)

## Running the notebook online

As the notebooks use hyperlinks for the navigation, and because this doesn't work on GitHub, they are also avaible on [nbviewer.org](https://nbviewer.org/github/Valkea/OC_AI_04/tree/main/) for convenience.

## Running the notebook locally

In order to use this project locally, you will need to have Python and Jupyter notebook installed.
Once done, we can set the environment by using the following commands:

### First, 
let's duplicate the project github repository

```bash
>>> git clone https://github.com/Valkea/OC_AI_05
>>> cd OC_AI_05
```

### Secondly,
let's download the [datasets](https://www.kaggle.com/olistbr/brazilian-ecommerce) and put them in the 'data' folder.

### Thirdly,
let's create a virtual environment and install the required Python libraries

(Linux or Mac)
```bash
>>> python3 -m venv venvP5
>>> source venvP5/bin/activate
>>> pip install -r requirements.txt
```

(Windows):
```bash
>>> py -m venv venvP5
>>> .\venvP5\Scripts\activate
>>> py -m pip install -r requirements.txt
```

### Finally,
let's configure and run the virtual environment for Jupyter notebook


#### Install jupyter kernel for the virtual environment using the following command:

```bash
>>> pip install ipykernel
>>> python -m ipykernel install --user --name=venvP5
```

#### Select the installed kernel

In order to run the various notebooks, you will need to use the virtual environnement created above.
So once the notebooks are opened (see below), prior to running it, follow this step:
![alt text](medias/venv_selection.png)

#### Run the jupyter notebooks

1. in order to see the interactive EDA, run:
```bash
>>> voila 01_EDA.ipynb
```

2. to see the clustering models' selection, use the following command:
```bash
>>> jupyter notebook 02_Clustering.ipynb
```

3. finally, in order to get explore the data-drifting notebook use:
```bash
>>> jupyter notebook 03_DataDrift.ipynb 
```

#### Uninstalling the venv kernel
Once done with the project, the kernel can be listed and removed using the following commands:

```bash
>>> jupyter kernelspec list
>>> jupyter kernelspec uninstall venvp5
```

