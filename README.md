# Computer Vision Pokedex

### Tools used

This was built with PyTorch/FastAI for the Machine Learning part and Flask as a Webserver. For containerization and easy deployment I use Docker. 

### Data

To create the data set I've used two different Data Sources. First I've used an alredy exiting pokemon (first generation only) dataset got from [Kaggle](https://www.kaggle.com/lantian773030/pokemonclassification). To increase the number of Image I've used the Bing Image API to automate the download more images for each pokemon. You can find it how in this collab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1NyRL1KD4CikfH5eY0gGzva_Tm8uQOw0A)

I've mixed the data from both data sources in a unique dataset. I have manually checked it to delete as many duplications as possible. I have also take care that each pokemon type has been saved in a folder with the pokemon name and that each image file has the pokemon name too.


