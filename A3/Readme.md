EIP Phase 1 Assignment 3

Contributors: Abhijit Mali

--------------------------------------------------------------------------------------------------------------------------------
Summary
-------
Got to learn about regularization techniques while working on this assignment along with use of depth wise separable convolutions. I tried using global average pooling instead of flatten in my model but in this case the accuracy was decreasing. I have used image augmentation in this model along with learning rate scheduler.

--------------------------------------------------------------------------------------------------------------------------------
Final Validation accuracy for Base Network
------------------------------------------
  Accuracy on test data is: 83.22
  
--------------------------------------------------------------------------------------------------------------------------------
Model definition with output channel size and receptive field
--------------------------------------------------------------
model = Sequential()

model.add(SeparableConv2D(32, 3, 3,  input_shape=(32, 32, 3),kernel_regularizer=l2(0.01))) #30,3

model.add(BatchNormalization())

model.add(Activation('relu'))

model.add(SeparableConv2D(64, 3, 3,kernel_regularizer=l2(0.02))) #28,5

model.add(BatchNormalization())

model.add(Activation('relu'))

model.add(SeparableConv2D(64, 3, 3,kernel_regularizer=l2(0.02))) #26,7

model.add(BatchNormalization())

model.add(Activation('relu'))

model.add(SeparableConv2D(128, 3, 3,kernel_regularizer=l2(0.02))) #24,9

model.add(BatchNormalization())

model.add(Activation('relu'))

model.add(SeparableConv2D(256, 3, 3,kernel_regularizer=l2(0.02))) #22,11

model.add(BatchNormalization())

model.add(Dropout(0.4))

model.add(Activation('relu'))

model.add(MaxPooling2D(pool_size=(2, 2))) #11,12

model.add(SeparableConv2D(10, 11, 11)) 

model.add(Flatten())

model.add(Activation('softmax'))

--------------------------------------------------------------------------------------------------------------------------------
Logs for 50 epochs
-------------------
Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.005.
781/781 [==============================] - 37s 47ms/step - loss: 1.4414 - acc: 0.4845 - val_loss: 1.8222 - val_acc: 0.3661
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0037907506.
781/781 [==============================] - 34s 44ms/step - loss: 1.0546 - acc: 0.6298 - val_loss: 1.1044 - val_acc: 0.6223
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.0030525031.
781/781 [==============================] - 35s 44ms/step - loss: 0.9014 - acc: 0.6837 - val_loss: 1.0646 - val_acc: 0.6388
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.002554931.
781/781 [==============================] - 35s 44ms/step - loss: 0.7985 - acc: 0.7248 - val_loss: 0.9124 - val_acc: 0.6858
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0021968366.
781/781 [==============================] - 35s 44ms/step - loss: 0.7338 - acc: 0.7438 - val_loss: 0.8054 - val_acc: 0.7285
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.0019267823.
781/781 [==============================] - 34s 44ms/step - loss: 0.6842 - acc: 0.7615 - val_loss: 0.6806 - val_acc: 0.7760
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0017158545.
781/781 [==============================] - 35s 44ms/step - loss: 0.6454 - acc: 0.7748 - val_loss: 0.7223 - val_acc: 0.7594
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0015465512.
781/781 [==============================] - 34s 44ms/step - loss: 0.6102 - acc: 0.7890 - val_loss: 0.7020 - val_acc: 0.7558
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0014076577.
781/781 [==============================] - 35s 44ms/step - loss: 0.5909 - acc: 0.7967 - val_loss: 0.7079 - val_acc: 0.7545
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0012916559.
781/781 [==============================] - 35s 45ms/step - loss: 0.5660 - acc: 0.8037 - val_loss: 0.6225 - val_acc: 0.7906
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.0011933174.
781/781 [==============================] - 36s 45ms/step - loss: 0.5460 - acc: 0.8102 - val_loss: 0.6294 - val_acc: 0.7837
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.0011088933.
781/781 [==============================] - 36s 46ms/step - loss: 0.5339 - acc: 0.8145 - val_loss: 0.5746 - val_acc: 0.8114
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.0010356255.
781/781 [==============================] - 35s 45ms/step - loss: 0.5149 - acc: 0.8231 - val_loss: 0.5611 - val_acc: 0.8135
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.0009714397.
781/781 [==============================] - 36s 45ms/step - loss: 0.5027 - acc: 0.8266 - val_loss: 0.5935 - val_acc: 0.7977
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0009147457.
781/781 [==============================] - 35s 45ms/step - loss: 0.4915 - acc: 0.8320 - val_loss: 0.5451 - val_acc: 0.8171
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.0008643042.
781/781 [==============================] - 35s 44ms/step - loss: 0.4744 - acc: 0.8342 - val_loss: 0.5654 - val_acc: 0.8105
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.000819135.
781/781 [==============================] - 34s 44ms/step - loss: 0.4689 - acc: 0.8387 - val_loss: 0.6214 - val_acc: 0.7850
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0007784524.
781/781 [==============================] - 35s 44ms/step - loss: 0.4625 - acc: 0.8400 - val_loss: 0.5611 - val_acc: 0.8068
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0007416197.
781/781 [==============================] - 35s 44ms/step - loss: 0.4472 - acc: 0.8453 - val_loss: 0.5441 - val_acc: 0.8162
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.000708115.
781/781 [==============================] - 35s 44ms/step - loss: 0.4434 - acc: 0.8484 - val_loss: 0.5195 - val_acc: 0.8225
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0006775068.
781/781 [==============================] - 35s 44ms/step - loss: 0.4323 - acc: 0.8499 - val_loss: 0.5108 - val_acc: 0.8224
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.000649435.
781/781 [==============================] - 35s 44ms/step - loss: 0.4333 - acc: 0.8499 - val_loss: 0.5087 - val_acc: 0.8293
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0006235969.
781/781 [==============================] - 35s 45ms/step - loss: 0.4251 - acc: 0.8526 - val_loss: 0.5099 - val_acc: 0.8240
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0005997361.
781/781 [==============================] - 35s 44ms/step - loss: 0.4209 - acc: 0.8542 - val_loss: 0.5047 - val_acc: 0.8286
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.000577634.
781/781 [==============================] - 35s 44ms/step - loss: 0.4136 - acc: 0.8572 - val_loss: 0.5035 - val_acc: 0.8279
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0005571031.
781/781 [==============================] - 35s 44ms/step - loss: 0.4094 - acc: 0.8585 - val_loss: 0.4984 - val_acc: 0.8293
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.0005379815.
781/781 [==============================] - 35s 44ms/step - loss: 0.4079 - acc: 0.8602 - val_loss: 0.5272 - val_acc: 0.8181
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.000520129.
781/781 [==============================] - 35s 44ms/step - loss: 0.3991 - acc: 0.8627 - val_loss: 0.5022 - val_acc: 0.8291
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.0005034233.
781/781 [==============================] - 35s 44ms/step - loss: 0.4003 - acc: 0.8623 - val_loss: 0.4903 - val_acc: 0.8324
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.0004877573.
781/781 [==============================] - 34s 44ms/step - loss: 0.3919 - acc: 0.8652 - val_loss: 0.4939 - val_acc: 0.8305
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.0004730369.
781/781 [==============================] - 35s 44ms/step - loss: 0.3859 - acc: 0.8658 - val_loss: 0.4809 - val_acc: 0.8354
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 0.000459179.
781/781 [==============================] - 35s 45ms/step - loss: 0.3844 - acc: 0.8664 - val_loss: 0.4863 - val_acc: 0.8344
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 0.0004461099.
781/781 [==============================] - 34s 44ms/step - loss: 0.3795 - acc: 0.8679 - val_loss: 0.5003 - val_acc: 0.8269
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 0.0004337642.
781/781 [==============================] - 34s 44ms/step - loss: 0.3758 - acc: 0.8679 - val_loss: 0.4785 - val_acc: 0.8361
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 0.0004220834.
781/781 [==============================] - 34s 44ms/step - loss: 0.3758 - acc: 0.8699 - val_loss: 0.5034 - val_acc: 0.8289
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 0.0004110152.
781/781 [==============================] - 34s 44ms/step - loss: 0.3719 - acc: 0.8708 - val_loss: 0.4750 - val_acc: 0.8370
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 0.0004005127.
781/781 [==============================] - 34s 44ms/step - loss: 0.3715 - acc: 0.8716 - val_loss: 0.4736 - val_acc: 0.8367
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 0.0003905335.
781/781 [==============================] - 34s 44ms/step - loss: 0.3679 - acc: 0.8729 - val_loss: 0.4861 - val_acc: 0.8340
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 0.0003810395.
781/781 [==============================] - 34s 44ms/step - loss: 0.3583 - acc: 0.8743 - val_loss: 0.4715 - val_acc: 0.8389
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 0.0003719961.
781/781 [==============================] - 34s 44ms/step - loss: 0.3603 - acc: 0.8750 - val_loss: 0.4789 - val_acc: 0.8396
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 0.0003633721.
781/781 [==============================] - 34s 44ms/step - loss: 0.3552 - acc: 0.8770 - val_loss: 0.4619 - val_acc: 0.8441
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 0.0003551389.
781/781 [==============================] - 34s 44ms/step - loss: 0.3539 - acc: 0.8762 - val_loss: 0.4757 - val_acc: 0.8363
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 0.0003472705.
781/781 [==============================] - 34s 44ms/step - loss: 0.3519 - acc: 0.8766 - val_loss: 0.4730 - val_acc: 0.8382
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 0.0003397432.
781/781 [==============================] - 34s 43ms/step - loss: 0.3518 - acc: 0.8775 - val_loss: 0.4838 - val_acc: 0.8361
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 0.0003325352.
781/781 [==============================] - 34s 43ms/step - loss: 0.3520 - acc: 0.8775 - val_loss: 0.4698 - val_acc: 0.8384
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 0.0003256268.
781/781 [==============================] - 34s 43ms/step - loss: 0.3411 - acc: 0.8795 - val_loss: 0.4728 - val_acc: 0.8369
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 0.0003189996.
781/781 [==============================] - 34s 43ms/step - loss: 0.3466 - acc: 0.8794 - val_loss: 0.4572 - val_acc: 0.8425
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 0.0003126368.
781/781 [==============================] - 34s 43ms/step - loss: 0.3361 - acc: 0.8838 - val_loss: 0.4794 - val_acc: 0.8342
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 0.0003065228.
781/781 [==============================] - 34s 44ms/step - loss: 0.3411 - acc: 0.8818 - val_loss: 0.4619 - val_acc: 0.8415
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 0.0003006434.
781/781 [==============================] - 34s 44ms/step - loss: 0.3375 - acc: 0.8809 - val_loss: 0.4651 - val_acc: 0.8441
Model took 1727.32 seconds to train

Accuracy on test data is: 84.41
--------------------------------------------------------------------------------------------------------------------------------
