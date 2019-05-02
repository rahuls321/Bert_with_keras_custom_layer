# Bert_with_keras_custom_layer CPU/GPU
 tensorflow 1.13.1
 
 Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_ids (InputLayer)          (None, 256)          0                                            
__________________________________________________________________________________________________
input_masks (InputLayer)        (None, 256)          0                                            
__________________________________________________________________________________________________
segment_ids (InputLayer)        (None, 256)          0                                            
__________________________________________________________________________________________________
bert_layer_1 (BertLayer)        (None, 768)          110104890   input_ids[0][0]                  
                                                                 input_masks[0][0]                
                                                                 segment_ids[0][0]                
__________________________________________________________________________________________________
dense (Dense)                   (None, 256)          196864      bert_layer_1[0][0]               
__________________________________________________________________________________________________
dense_1 (Dense)                 (None, 1)            257         dense[0][0]                      
==================================================================================================
Total params: 110,302,011
Trainable params: 3,147,009
Non-trainable params: 107,155,002
__________________________________________________________________________________________________
2019-04-30 18:12:27.607763: W tensorflow/core/framework/allocator.cc:124] Allocation of 93763584 exceeds 10% of system memory.
2019-04-30 18:12:27.610406: W tensorflow/core/framework/allocator.cc:124] Allocation of 93763584 exceeds 10% of system memory.
2019-04-30 18:12:27.611246: W tensorflow/core/framework/allocator.cc:124] Allocation of 93763584 exceeds 10% of system memory.
Train on 25000 samples, validate on 25000 samples
2019-04-30 18:12:37.437413: W tensorflow/core/framework/allocator.cc:124] Allocation of 100663296 exceeds 10% of system memory.
2019-04-30 18:12:37.723220: W tensorflow/core/framework/allocator.cc:124] Allocation of 100663296 exceeds 10% of system memory.
25000/25000 [==============================] - 68819s 3s/sample - loss: 0.3261 - acc: 0.8567 - val_loss: 0.2369 - val_acc: 0.9032
