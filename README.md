# Computer Vision Pokedex

### Tools used

This was built with PyTorch/FastAI for the Machine Learning part and Flask as a Webserver. For containerization and easy deployment, I use Docker. 

### Data

To create the data set I've used two different Data Sources. First I've used an already exiting pokemon (first-generation only) dataset got from [Kaggle](https://www.kaggle.com/lantian773030/pokemonclassification). To increase the number of Images I've used the Bing Image API to automate the download of more images for each pokemon. You can find it how in this [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NyRL1KD4CikfH5eY0gGzva_Tm8uQOw0A)

I've mixed the data from both data sources in a unique dataset. I have manually checked it to delete as many duplications as possible. I have also take care that each pokemon type has been saved in a folder with the pokemon name and that each image file has the pokemon name too.

You can find the final data set to be downloaded [here](https://drive.google.com/drive/folders/11qPNGvI-Ks0-5AAPSffbCc668FZCaoJF?usp=sharing)

### Model

To create and train the model I've used the Fast.ai library. I've followed the Fast.ai course and documentation to learn and understand how to use Fast.ai. I've tried different architectures and setups not only for finding the best performance but mainly to understand how Fast.ai works. The current architecture is the one that has given me until now the best results but I will keep working on different setups to improve its performance.  You can find how I did it and more information about the process in this  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HzM7NuluadB0Wjm5dgt19Smej10eWEb)


### Deployment

I have created a Flask web application that can take images uploaded from the user from their PC or mobile phone and get a prediction. For containerization and easy deployment, I've used Docker.

How to run it yourself

To play with the image classification model:

1.- Download the already curated dataset from  [here](https://drive.google.com/drive/folders/11qPNGvI-Ks0-5AAPSffbCc668FZCaoJF?usp=sharing) and upload it to your Google Drive account.

2.- Open this [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10HzM7NuluadB0Wjm5dgt19Smej10eWEb)
 file and play with it. Remember to set the path where you have put the Pokemon dataset in Google drive. 

3.- As soon as you get a performance you are comfortable enough with just download the PKL file of your model. 

To deploy the web app in your local machine:

1.- Download the repository
2.- Replacing the model (server/export.pkl) with your model
3.- Install Docker
4.- Command to launch the container:

docker build -t pokemon . && docker run --rm -it -p 5000:5000 pokemon

5.- Enjoy classifying pokemon ( remember, first-generation only) or uploading selfies from you or your family to check which pokemon they look like the most. 


