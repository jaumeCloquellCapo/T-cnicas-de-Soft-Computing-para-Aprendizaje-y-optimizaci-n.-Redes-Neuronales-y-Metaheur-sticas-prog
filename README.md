# Técnicas de Soft Computing para Aprendizaje y optimización. Redes Neuronales y Metaheurísticas, programación evolutiva y bioinspirada
Repositorio para los contenidos y trabajos de la asignatura "Técnicas de Soft Computing para Aprendizaje y optimización. Redes Neuronales y Metaheurísticas, programación evolutiva y bioinspirada " del máster en ciencia de datos e ingeniería de computadores. 

# Histopathologic Cancer Detector

Python Jupyter Notebook leveraging **Transfer Learning**  and **Convolutional Neural Networks** implemented with **Keras**. 

Part of the [Kaggle competition](https://www.kaggle.com/c/histopathologic-cancer-detection). 

Submitted [Kernel](https://www.kaggle.com/jaumecloquellcapo/t-cnicas-de-soft-computing-cnn-v2) with 0.92 LB score.

## Data

**Dataset:** [Link](https://www.kaggle.com/c/histopathologic-cancer-detection/data)

**Description:** Binary classification whether a given histopathologic image contains a tumor or not.

**Training:** 153k (0.9) images

**Validation:** 17k (0.1) images

**Testing:** 57.5k images

## Model
<h3>
  <img src="assets/model_plot.png" width="500">
</h3>

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 94, 94, 32)        896       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 92, 92, 32)        9216      
_________________________________________________________________
batch_normalization_1 (Batch (None, 92, 92, 32)        128       
_________________________________________________________________
activation_1 (Activation)    (None, 92, 92, 32)        0         
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 46, 46, 32)        0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 46, 46, 32)        0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 44, 44, 64)        18432     
_________________________________________________________________
batch_normalization_2 (Batch (None, 44, 44, 64)        256       
_________________________________________________________________
activation_2 (Activation)    (None, 44, 44, 64)        0         
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 42, 42, 64)        36864     
_________________________________________________________________
batch_normalization_3 (Batch (None, 42, 42, 64)        256       
_________________________________________________________________
activation_3 (Activation)    (None, 42, 42, 64)        0         
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 21, 21, 64)        0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 21, 21, 64)        0         
_________________________________________________________________
conv2d_5 (Conv2D)            (None, 19, 19, 128)       73728     
_________________________________________________________________
batch_normalization_4 (Batch (None, 19, 19, 128)       512       
_________________________________________________________________
activation_4 (Activation)    (None, 19, 19, 128)       0         
_________________________________________________________________
conv2d_6 (Conv2D)            (None, 17, 17, 128)       147456    
_________________________________________________________________
batch_normalization_5 (Batch (None, 17, 17, 128)       512       
_________________________________________________________________
activation_5 (Activation)    (None, 17, 17, 128)       0         
_________________________________________________________________
max_pooling2d_3 (MaxPooling2 (None, 8, 8, 128)         0         
_________________________________________________________________
dropout_3 (Dropout)          (None, 8, 8, 128)         0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 8192)              0         
_________________________________________________________________
dense_1 (Dense)              (None, 256)               2097152   
_________________________________________________________________
batch_normalization_6 (Batch (None, 256)               1024      
_________________________________________________________________
activation_6 (Activation)    (None, 256)               0         
_________________________________________________________________
dropout_4 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 1)                 257       
=================================================================
Total params: 2,386,689
Trainable params: 2,385,345
Non-trainable params: 1,344
_________________________________________________________________


## Training

<h3>
  <img src="assets/training.png" width="500">
</h3>

<h3>
  <img src="assets/validation.png" width="500">
</h3>

<h3>
  <img src="assets/roc.png" width="500">
</h3>

## Results

Kaggle score: **0.92**
