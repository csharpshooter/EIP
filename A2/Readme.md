EIP Phase 1 Assignment 2

Contributors: Abhijit Mali


Logs for 20 epochs
-------------------------------------------------------------------------------------------------------------
Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 11s 175us/step - loss: 0.2193 - acc: 0.9302 - val_loss: 0.0641 - val_acc: 0.9794
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0635 - acc: 0.9796 - val_loss: 0.0468 - val_acc: 0.9844
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0493 - acc: 0.9849 - val_loss: 0.0288 - val_acc: 0.9908
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0416 - acc: 0.9871 - val_loss: 0.0310 - val_acc: 0.9902
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0377 - acc: 0.9888 - val_loss: 0.0246 - val_acc: 0.9919
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0327 - acc: 0.9899 - val_loss: 0.0256 - val_acc: 0.9918
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0299 - acc: 0.9907 - val_loss: 0.0254 - val_acc: 0.9919
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 5s 87us/step - loss: 0.0287 - acc: 0.9908 - val_loss: 0.0203 - val_acc: 0.9935
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 5s 88us/step - loss: 0.0255 - acc: 0.9923 - val_loss: 0.0204 - val_acc: 0.9931
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 5s 86us/step - loss: 0.0250 - acc: 0.9918 - val_loss: 0.0216 - val_acc: 0.9936
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0224 - acc: 0.9928 - val_loss: 0.0187 - val_acc: 0.9942
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0226 - acc: 0.9923 - val_loss: 0.0197 - val_acc: 0.9940
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 5s 87us/step - loss: 0.0216 - acc: 0.9926 - val_loss: 0.0208 - val_acc: 0.9932
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 5s 86us/step - loss: 0.0205 - acc: 0.9931 - val_loss: 0.0220 - val_acc: 0.9925
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 5s 86us/step - loss: 0.0194 - acc: 0.9937 - val_loss: 0.0188 - val_acc: 0.9942
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 5s 85us/step - loss: 0.0195 - acc: 0.9935 - val_loss: 0.0210 - val_acc: 0.9931
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 5s 87us/step - loss: 0.0175 - acc: 0.9943 - val_loss: 0.0174 - val_acc: 0.9952
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0172 - acc: 0.9942 - val_loss: 0.0198 - val_acc: 0.9945
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0179 - acc: 0.9944 - val_loss: 0.0207 - val_acc: 0.9935
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0165 - acc: 0.9947 - val_loss: 0.0183 - val_acc: 0.9941
<keras.callbacks.History at 0x7f6268700128>

------------------------------------------------------------------------------------------------------------------------------------

Result of model.evaluate (on test data)
------------------------------------------------------------------------------------------------------------------------------------
[0.01834861671927647, 0.9941]
------------------------------------------------------------------------------------------------------------------------------------
If figured that one way to reduce the no of parameters we can do it by reducing the number of filters on the second convolution. 
So I changed the no of filter from 32 to 16. So for that I got the following output:
Total params: 13,914
Trainable params: 13,722
Non-trainable params: 192

But after that when I ran "model.fit" I figured out that my model is underfitting as the accuracy on the validation set is more than
the training set. So I checked and found that there was a batch normalisation and a dropout of 0.1 for last layer. 
Also the reason for underfitting might be the dropout, as dropout is only used when our model is overfitting. But here my model was 
underfitting so I removed the dropout. 

I also removed batch normalisation from the last layer as the last layer is sacrosanct we avoid adding anything after the last layer. 
Also batch normalisation might decrease accuracy, as incase of mnist as mnist is black and white dataset and batch normalisation 
makes smaller gaps bigger.

I have done the assignment with and without batch normalisation in last layer. The above logs are for the model 
without batch normalisation for last layer.

My observation is there we get more accuracy without batch normalisation in last layer. The difference is not much still 
there is some difference.
 
