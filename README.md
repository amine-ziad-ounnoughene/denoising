# image-denoising-convolutional-autoencoder
image denoising convolutional autoencoder neural nets
# loss
i had an MSE of 0.02 after 10 epochs
# dataset used
from kaggle.com https://www.kaggle.com/adityachandrasekhar/image-super-resolution
which contains RGB images of shape 256,256,3 
with noise images as features and denoised one as label
# model's architecture
'''bash
Model: "model_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_2 (InputLayer)         [(None, 256, 256, 3)]     0         
_________________________________________________________________
conv2d_6 (Conv2D)            (None, 256, 256, 256)     7168      
_________________________________________________________________
max_pooling2d_5 (MaxPooling2 (None, 128, 128, 256)     0         
_________________________________________________________________
conv2d_7 (Conv2D)            (None, 128, 128, 128)     295040    
_________________________________________________________________
max_pooling2d_6 (MaxPooling2 (None, 64, 64, 128)       0         
_________________________________________________________________
conv2d_8 (Conv2D)            (None, 64, 64, 64)        73792     
_________________________________________________________________
max_pooling2d_7 (MaxPooling2 (None, 32, 32, 64)        0         
_________________________________________________________________
conv2d_9 (Conv2D)            (None, 32, 32, 32)        18464     
_________________________________________________________________
max_pooling2d_8 (MaxPooling2 (None, 16, 16, 32)        0         
_________________________________________________________________
conv2d_10 (Conv2D)           (None, 16, 16, 32)        9248      
_________________________________________________________________
max_pooling2d_9 (MaxPooling2 (None, 8, 8, 32)          0         
_________________________________________________________________
conv2d_transpose_5 (Conv2DTr (None, 16, 16, 32)        9248      
_________________________________________________________________
conv2d_transpose_6 (Conv2DTr (None, 32, 32, 32)        9248      
_________________________________________________________________
conv2d_transpose_7 (Conv2DTr (None, 64, 64, 64)        18496     
_________________________________________________________________
conv2d_transpose_8 (Conv2DTr (None, 128, 128, 128)     73856     
_________________________________________________________________
conv2d_transpose_9 (Conv2DTr (None, 256, 256, 256)     295168    
_________________________________________________________________
conv2d_11 (Conv2D)           (None, 256, 256, 1)       2305      
=================================================================
Total params: 812,033
Trainable params: 812,033
Non-trainable params: 0
'''
