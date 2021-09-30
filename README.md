# Casting Defect Detection
## Based on data from Kaggle

This system can detect any defect in casting process based on data.
## Database
The database has been taken from kaggle, based on data provided
by Ravirajsinh Dabhi. It contains 6633 training images and 715 testing images.
The images have been distributed into two classes - def_front (defective)
and ok_front(OK).
The images have already been preprocessed into 300x300 grayscale resolution.

You can find the database on this [link](https://www.kaggle.com/ravirajsinh45/real-life-industrial-dataset-of-casting-product).


## Tech

- Python - Google Colab/Jupyter Notebook
- Pandas library
- Numpy library
- Keras library

## Data Augmentation
- rotation_range
- width_shift_range
- height_shift_range
- shear_range
- zoom_range
- horizontal_flip
- vertical_flip
- brightness_range
- rescale
- validation_split

## Models Used

- Convolutional Neural Network
-- Conv2D(filters = 16)
-- MaxPooling2D
-- Conv2D(filters = 32)
-- MaxPooling2D
-- Flatten
-- Dense(128)
-- Dropout(0.2)
-- Dense(64)
-- Dropout(0.2)
-- Dense(1)

#### Model summary
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 149, 149, 16)      160       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 74, 74, 16)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 36, 36, 32)        4640      
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 18, 18, 32)        0         
_________________________________________________________________
flatten (Flatten)            (None, 10368)             0         
_________________________________________________________________
dense (Dense)                (None, 128)               1327232   
_________________________________________________________________
dropout (Dropout)            (None, 128)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 64)                8256      
_________________________________________________________________
dropout_1 (Dropout)          (None, 64)                0         
_________________________________________________________________
dense_2 (Dense)              (None, 1)                 65        
=================================================================
Total params: 1,340,353
Trainable params: 1,340,353
Non-trainable params: 0
_________________________________________________________________


Happy predictions!!!

Also, feel free to contact me via email (kulshreshthabhinav@gmail.com) if you have any suggestions for the model or you find a model better than this.
