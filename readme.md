# Deep learning - predict malaria using images
This project is predicting a person has malaria or not by training a network (renest)

https://www.pyimagesearch.com/2018/12/03/deep-learning-and-medical-image-analysis-with-keras/

## Files
- pyimagesearch folder: has resnet model
- build_dataset.py will help you set up the dataset
- train_model.py will train the model and make prediction
- load_model.py will load random 16 images with predictions


## How to use this code
1. Import the nexessary packages

2. download the dataset 
$ wget https://ceb.nlm.nih.gov/proj/malaria/cell_images.zip
$ unzip cell_images.zip

3. Run build_dataset.py

4. Run train_model.py

5. Run load_model.py


## How this works
- build_dataset.py will help you set up the dataset
- function poly_decay gives out the learning rate which is used during the training
- Use NUM_EPOCHS = 20, INIT_LR = 1e-1, BS = 32
- Use ImageDataGenerator to data augmentation
- Build the resnet model  with Images (width:64xheight:64xdepth:3), classes: 2, stages: (3,4,6), filters: (64, 128, 256, 512)
- Fit the train set and val set into the model
- After training, use the model to predict the test set
- Save the model on the disk
- Load the model on the disk and make predictions on testing images

## My thoughts
Because of my slow laptop, I just trained on only 1 epoch.  However, the accuracy is pretty good.  The model is able to predict malaria 

![alt pic1](https://github.com/BenjaminDKLuong/Deep-Learning-Malaria-Dectection/blob/master/results.png)
