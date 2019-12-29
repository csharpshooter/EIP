
EIP Phase 1 Assignment 5
------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------
Contributors: Abhijit Mali
--------------------------
Summary
-------
I tried different models like vgg19, Resnet34 and resnet50v2 (the other models are in test folder). But I got good accuracy with this Vgg16 model.
I also used early stopping in this model. I used early stopping as when I tried to train for epochs more than 20-25 validation accuracy would not increase much.
I am also working on  model where I used a method to train for 50 epochs and then load the best model and again train it for 20 more epochs and do this 2-3 more times. But I had not finished working on it till the deadline so have submitted the model with best accuracy I have.
I have used Image data augmentation random cut-out with Person data generator.
I have changed the started model a bit. I tried to implement one cycle policy but was unsuccessfull.
I will still keep on working ont this assignment to improve it further as I learnt a lot of things which I need to do and also
which can go wrong.

----------------------------------------------------------------------------------------------------------------------------------
Output:
----------------------------

Learning rate:  0.001

Epoch 00001: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 114s 317ms/step - loss: 8.7403 - gender_output_loss: 0.6890 - image_quality_output_loss: 0.9957 - age_output_loss: 1.4501 - weight_output_loss: 1.0137 - bag_output_loss: 0.9417 - footwear_output_loss: 1.0351 - pose_output_loss: 0.9403 - emotion_output_loss: 0.9496 - gender_output_acc: 0.5525 - image_quality_output_acc: 0.5422 - age_output_acc: 0.3944 - weight_output_acc: 0.6277 - bag_output_acc: 0.5534 - footwear_output_acc: 0.4688 - pose_output_acc: 0.6157 - emotion_output_acc: 0.7063 - val_loss: 8.4600 - val_gender_output_loss: 0.6831 - val_image_quality_output_loss: 0.9566 - val_age_output_loss: 1.4101 - val_weight_output_loss: 0.9752 - val_bag_output_loss: 0.9065 - val_footwear_output_loss: 1.0045 - val_pose_output_loss: 0.9324 - val_emotion_output_loss: 0.8866 - val_gender_output_acc: 0.5675 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3968 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5699 - val_footwear_output_acc: 0.5501 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282

Epoch 00001: val_loss improved from inf to 8.46000, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.001.h5
Epoch 2/50
Learning rate:  0.001

Epoch 00002: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 294ms/step - loss: 8.5913 - gender_output_loss: 0.6862 - image_quality_output_loss: 0.9866 - age_output_loss: 1.4354 - weight_output_loss: 0.9916 - bag_output_loss: 0.9226 - footwear_output_loss: 0.9925 - pose_output_loss: 0.9318 - emotion_output_loss: 0.9268 - gender_output_acc: 0.5604 - image_quality_output_acc: 0.5493 - age_output_acc: 0.3993 - weight_output_acc: 0.6359 - bag_output_acc: 0.5623 - footwear_output_acc: 0.5393 - pose_output_acc: 0.6186 - emotion_output_acc: 0.7090 - val_loss: 8.3985 - val_gender_output_loss: 0.6835 - val_image_quality_output_loss: 0.9552 - val_age_output_loss: 1.4082 - val_weight_output_loss: 0.9747 - val_bag_output_loss: 0.9068 - val_footwear_output_loss: 0.9581 - val_pose_output_loss: 0.9320 - val_emotion_output_loss: 0.8759 - val_gender_output_acc: 0.5675 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3968 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5699 - val_footwear_output_acc: 0.5551 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282

Epoch 00002: val_loss improved from 8.46000 to 8.39850, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.002.h5
Epoch 3/50
Learning rate:  0.001

Epoch 00003: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 105s 293ms/step - loss: 8.5432 - gender_output_loss: 0.6854 - image_quality_output_loss: 0.9846 - age_output_loss: 1.4307 - weight_output_loss: 0.9879 - bag_output_loss: 0.9224 - footwear_output_loss: 0.9666 - pose_output_loss: 0.9286 - emotion_output_loss: 0.9216 - gender_output_acc: 0.5623 - image_quality_output_acc: 0.5487 - age_output_acc: 0.3982 - weight_output_acc: 0.6359 - bag_output_acc: 0.5628 - footwear_output_acc: 0.5518 - pose_output_acc: 0.6186 - emotion_output_acc: 0.7090 - val_loss: 8.3586 - val_gender_output_loss: 0.6793 - val_image_quality_output_loss: 0.9571 - val_age_output_loss: 1.4039 - val_weight_output_loss: 0.9729 - val_bag_output_loss: 0.9017 - val_footwear_output_loss: 0.9391 - val_pose_output_loss: 0.9296 - val_emotion_output_loss: 0.8732 - val_gender_output_acc: 0.5675 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3968 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5699 - val_footwear_output_acc: 0.5655 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282

Epoch 00003: val_loss improved from 8.39850 to 8.35857, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.003.h5
Epoch 4/50
Learning rate:  0.001

Epoch 00004: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 294ms/step - loss: 8.4882 - gender_output_loss: 0.6796 - image_quality_output_loss: 0.9830 - age_output_loss: 1.4249 - weight_output_loss: 0.9842 - bag_output_loss: 0.9188 - footwear_output_loss: 0.9412 - pose_output_loss: 0.9253 - emotion_output_loss: 0.9188 - gender_output_acc: 0.5623 - image_quality_output_acc: 0.5488 - age_output_acc: 0.3993 - weight_output_acc: 0.6359 - bag_output_acc: 0.5623 - footwear_output_acc: 0.5668 - pose_output_acc: 0.6186 - emotion_output_acc: 0.7090 - val_loss: 8.2570 - val_gender_output_loss: 0.6574 - val_image_quality_output_loss: 0.9599 - val_age_output_loss: 1.3897 - val_weight_output_loss: 0.9745 - val_bag_output_loss: 0.8987 - val_footwear_output_loss: 0.8874 - val_pose_output_loss: 0.9267 - val_emotion_output_loss: 0.8680 - val_gender_output_acc: 0.5734 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3968 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5699 - val_footwear_output_acc: 0.6012 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282


Epoch 00004: val_loss improved from 8.35857 to 8.25698, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.004.h5
Epoch 5/50
Learning rate:  0.001

Epoch 00005: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 295ms/step - loss: 8.4056 - gender_output_loss: 0.6605 - image_quality_output_loss: 0.9827 - age_output_loss: 1.4190 - weight_output_loss: 0.9842 - bag_output_loss: 0.9120 - footwear_output_loss: 0.8981 - pose_output_loss: 0.9206 - emotion_output_loss: 0.9191 - gender_output_acc: 0.5938 - image_quality_output_acc: 0.5471 - age_output_acc: 0.3994 - weight_output_acc: 0.6359 - bag_output_acc: 0.5628 - footwear_output_acc: 0.5879 - pose_output_acc: 0.6186 - emotion_output_acc: 0.7090 - val_loss: 8.1829 - val_gender_output_loss: 0.6222 - val_image_quality_output_loss: 0.9588 - val_age_output_loss: 1.3828 - val_weight_output_loss: 0.9716 - val_bag_output_loss: 0.8932 - val_footwear_output_loss: 0.8734 - val_pose_output_loss: 0.9160 - val_emotion_output_loss: 0.8734 - val_gender_output_acc: 0.6409 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3963 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5804 - val_footwear_output_acc: 0.6076 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282

Epoch 00005: val_loss improved from 8.25698 to 8.18293, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.005.h5
Epoch 6/50
Learning rate:  0.001

Epoch 00006: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 295ms/step - loss: 8.3248 - gender_output_loss: 0.6412 - image_quality_output_loss: 0.9807 - age_output_loss: 1.4138 - weight_output_loss: 0.9815 - bag_output_loss: 0.9045 - footwear_output_loss: 0.8703 - pose_output_loss: 0.9074 - emotion_output_loss: 0.9184 - gender_output_acc: 0.6230 - image_quality_output_acc: 0.5484 - age_output_acc: 0.3982 - weight_output_acc: 0.6359 - bag_output_acc: 0.5674 - footwear_output_acc: 0.6057 - pose_output_acc: 0.6186 - emotion_output_acc: 0.7090 - val_loss: 8.0847 - val_gender_output_loss: 0.6245 - val_image_quality_output_loss: 0.9515 - val_age_output_loss: 1.3730 - val_weight_output_loss: 0.9622 - val_bag_output_loss: 0.8791 - val_footwear_output_loss: 0.8374 - val_pose_output_loss: 0.9042 - val_emotion_output_loss: 0.8663 - val_gender_output_acc: 0.6468 - val_image_quality_output_acc: 0.5749 - val_age_output_acc: 0.3958 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5779 - val_footwear_output_acc: 0.6190 - val_pose_output_acc: 0.6126 - val_emotion_output_acc: 0.7282

Epoch 00006: val_loss improved from 8.18293 to 8.08468, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.006.h5
Epoch 7/50
Learning rate:  0.001

Epoch 00007: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 107s 297ms/step - loss: 8.2354 - gender_output_loss: 0.6163 - image_quality_output_loss: 0.9785 - age_output_loss: 1.4103 - weight_output_loss: 0.9786 - bag_output_loss: 0.8940 - footwear_output_loss: 0.8531 - pose_output_loss: 0.8848 - emotion_output_loss: 0.9147 - gender_output_acc: 0.6593 - image_quality_output_acc: 0.5503 - age_output_acc: 0.3982 - weight_output_acc: 0.6360 - bag_output_acc: 0.5725 - footwear_output_acc: 0.6157 - pose_output_acc: 0.6194 - emotion_output_acc: 0.7090 - val_loss: 7.9915 - val_gender_output_loss: 0.5939 - val_image_quality_output_loss: 0.9588 - val_age_output_loss: 1.3763 - val_weight_output_loss: 0.9613 - val_bag_output_loss: 0.8658 - val_footwear_output_loss: 0.8224 - val_pose_output_loss: 0.8601 - val_emotion_output_loss: 0.8648 - val_gender_output_acc: 0.6920 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3963 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5838 - val_footwear_output_acc: 0.6334 - val_pose_output_acc: 0.6151 - val_emotion_output_acc: 0.7282


Epoch 00007: val_loss improved from 8.08468 to 7.99149, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.007.h5
Epoch 8/50
Learning rate:  0.001

Epoch 00008: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 296ms/step - loss: 8.1342 - gender_output_loss: 0.5919 - image_quality_output_loss: 0.9748 - age_output_loss: 1.4055 - weight_output_loss: 0.9758 - bag_output_loss: 0.8829 - footwear_output_loss: 0.8334 - pose_output_loss: 0.8545 - emotion_output_loss: 0.9127 - gender_output_acc: 0.6896 - image_quality_output_acc: 0.5487 - age_output_acc: 0.3997 - weight_output_acc: 0.6359 - bag_output_acc: 0.5848 - footwear_output_acc: 0.6296 - pose_output_acc: 0.6250 - emotion_output_acc: 0.7090 - val_loss: 7.8731 - val_gender_output_loss: 0.5525 - val_image_quality_output_loss: 0.9414 - val_age_output_loss: 1.3655 - val_weight_output_loss: 0.9668 - val_bag_output_loss: 0.8661 - val_footwear_output_loss: 0.8028 - val_pose_output_loss: 0.8279 - val_emotion_output_loss: 0.8673 - val_gender_output_acc: 0.7168 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3963 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.5804 - val_footwear_output_acc: 0.6438 - val_pose_output_acc: 0.6334 - val_emotion_output_acc: 0.7282

Epoch 00008: val_loss improved from 7.99149 to 7.87309, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.008.h5

Epoch 00007: val_loss improved from 8.08468 to 7.99149, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.007.h5
Epoch 9/50
Learning rate:  0.001

Epoch 00009: LearningRateScheduler setting learning rate to 0.001.
359/360 [============================>.] - ETA: 0s - loss: 8.0455 - gender_output_loss: 0.5677 - image_quality_output_loss: 0.9719 - age_output_loss: 1.4033 - weight_output_loss: 0.9748 - bag_output_loss: 0.8760 - footwear_output_loss: 0.8257 - pose_output_loss: 0.8146 - emotion_output_loss: 0.9099 - gender_output_acc: 0.7063 - image_quality_output_acc: 0.5504 - age_output_acc: 0.3982 - weight_output_acc: 0.6356 - bag_output_acc: 0.5935 - footwear_output_acc: 0.6360 - pose_output_acc: 0.6453 - emotion_output_acc: 0.7088
Epoch 00008: val_loss improved from 7.99149 to 7.87309, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.008.h5
360/360 [==============================] - 107s 296ms/step - loss: 8.0439 - gender_output_loss: 0.5671 - image_quality_output_loss: 0.9716 - age_output_loss: 1.4035 - weight_output_loss: 0.9747 - bag_output_loss: 0.8757 - footwear_output_loss: 0.8256 - pose_output_loss: 0.8146 - emotion_output_loss: 0.9095 - gender_output_acc: 0.7067 - image_quality_output_acc: 0.5507 - age_output_acc: 0.3982 - weight_output_acc: 0.6358 - bag_output_acc: 0.5936 - footwear_output_acc: 0.6361 - pose_output_acc: 0.6452 - emotion_output_acc: 0.7090 - val_loss: 7.7828 - val_gender_output_loss: 0.5348 - val_image_quality_output_loss: 0.9387 - val_age_output_loss: 1.3668 - val_weight_output_loss: 0.9586 - val_bag_output_loss: 0.8610 - val_footwear_output_loss: 0.8012 - val_pose_output_loss: 0.7750 - val_emotion_output_loss: 0.8634 - val_gender_output_acc: 0.7222 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3988 - val_weight_output_acc: 0.6344 - val_bag_output_acc: 0.6012 - val_footwear_output_acc: 0.6438 - val_pose_output_acc: 0.6682 - val_emotion_output_acc: 0.7282

Epoch 00009: val_loss improved from 7.87309 to 7.78284, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.009.h5
Epoch 10/50
Learning rate:  0.001

Epoch 00010: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 294ms/step - loss: 7.9235 - gender_output_loss: 0.5356 - image_quality_output_loss: 0.9691 - age_output_loss: 1.3950 - weight_output_loss: 0.9736 - bag_output_loss: 0.8711 - footwear_output_loss: 0.8153 - pose_output_loss: 0.7657 - emotion_output_loss: 0.9006 - gender_output_acc: 0.7294 - image_quality_output_acc: 0.5514 - age_output_acc: 0.3998 - weight_output_acc: 0.6359 - bag_output_acc: 0.5995 - footwear_output_acc: 0.6385 - pose_output_acc: 0.6720 - emotion_output_acc: 0.7090 - val_loss: 7.7347 - val_gender_output_loss: 0.5192 - val_image_quality_output_loss: 0.9451 - val_age_output_loss: 1.3597 - val_weight_output_loss: 0.9586 - val_bag_output_loss: 0.8635 - val_footwear_output_loss: 0.7931 - val_pose_output_loss: 0.7655 - val_emotion_output_loss: 0.8501 - val_gender_output_acc: 0.7361 - val_image_quality_output_acc: 0.5764 - val_age_output_acc: 0.3998 - val_weight_output_acc: 0.6344 - val_bag_output_acc: 0.6047 - val_footwear_output_acc: 0.6483 - val_pose_output_acc: 0.6632 - val_emotion_output_acc: 0.7282

Epoch 00010: val_loss improved from 7.78284 to 7.73469, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.010.h5
360/360 [==============================]Epoch 11/50
Learning rate:  0.001

Epoch 00011: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 105s 293ms/step - loss: 7.8048 - gender_output_loss: 0.5103 - image_quality_output_loss: 0.9623 - age_output_loss: 1.3896 - weight_output_loss: 0.9687 - bag_output_loss: 0.8613 - footwear_output_loss: 0.8047 - pose_output_loss: 0.7142 - emotion_output_loss: 0.8989 - gender_output_acc: 0.7463 - image_quality_output_acc: 0.5523 - age_output_acc: 0.4001 - weight_output_acc: 0.6376 - bag_output_acc: 0.6089 - footwear_output_acc: 0.6438 - pose_output_acc: 0.6987 - emotion_output_acc: 0.7090 - val_loss: 7.5351 - val_gender_output_loss: 0.4738 - val_image_quality_output_loss: 0.9363 - val_age_output_loss: 1.3496 - val_weight_output_loss: 0.9533 - val_bag_output_loss: 0.8434 - val_footwear_output_loss: 0.7940 - val_pose_output_loss: 0.6545 - val_emotion_output_loss: 0.8553 - val_gender_output_acc: 0.7798 - val_image_quality_output_acc: 0.5759 - val_age_output_acc: 0.4028 - val_weight_output_acc: 0.6349 - val_bag_output_acc: 0.6176 - val_footwear_output_acc: 0.6468 - val_pose_output_acc: 0.7192 - val_emotion_output_acc: 0.7282

Epoch 00011: val_loss improved from 7.73469 to 7.53510, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.011.h5

Epoch 00010: val_loss improved from 7.78284 to 7.73469, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.010.h5
Epoch 12/50
Learning rate:  0.001

Epoch 00012: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 295ms/step - loss: 7.6894 - gender_output_loss: 0.4765 - image_quality_output_loss: 0.9600 - age_output_loss: 1.3843 - weight_output_loss: 0.9622 - bag_output_loss: 0.8545 - footwear_output_loss: 0.7985 - pose_output_loss: 0.6673 - emotion_output_loss: 0.8939 - gender_output_acc: 0.7734 - image_quality_output_acc: 0.5510 - age_output_acc: 0.4001 - weight_output_acc: 0.6355 - bag_output_acc: 0.6106 - footwear_output_acc: 0.6502 - pose_output_acc: 0.7217 - emotion_output_acc: 0.7090 - val_loss: 7.5561 - val_gender_output_loss: 0.4636 - val_image_quality_output_loss: 0.9369 - val_age_output_loss: 1.3637 - val_weight_output_loss: 0.9580 - val_bag_output_loss: 0.8549 - val_footwear_output_loss: 0.7962 - val_pose_output_loss: 0.6416 - val_emotion_output_loss: 0.8593 - val_gender_output_acc: 0.7743 - val_image_quality_output_acc: 0.5769 - val_age_output_acc: 0.4072 - val_weight_output_acc: 0.6354 - val_bag_output_acc: 0.6037 - val_footwear_output_acc: 0.6503 - val_pose_output_acc: 0.7242 - val_emotion_output_acc: 0.7282

Epoch 00012: val_loss did not improve from 7.53510
Epoch 13/50
Learning rate:  0.001

Epoch 00013: LearningRateScheduler setting learning rate to 0.001.
359/360 [============================>.] - ETA: 0s - loss: 7.6103 - gender_output_loss: 0.4586 - image_quality_output_loss: 0.9591 - age_output_loss: 1.3780 - weight_output_loss: 0.9582 - bag_output_loss: 0.8514 - footwear_output_loss: 0.7885 - pose_output_loss: 0.6383 - emotion_output_loss: 0.8892 - gender_output_acc: 0.7783 - image_quality_output_acc: 0.5540 - age_output_acc: 0.4014 - weight_output_acc: 0.6374 - bag_output_acc: 0.6136 - footwear_output_acc: 0.6504 - pose_output_acc: 0.7333 - emotion_output_acc: 0.7091

Epoch 00013: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 107s 297ms/step - loss: 7.6106 - gender_output_loss: 0.4583 - image_quality_output_loss: 0.9591 - age_output_loss: 1.3781 - weight_output_loss: 0.9587 - bag_output_loss: 0.8512 - footwear_output_loss: 0.7884 - pose_output_loss: 0.6384 - emotion_output_loss: 0.8894 - gender_output_acc: 0.7786 - image_quality_output_acc: 0.5540 - age_output_acc: 0.4013 - weight_output_acc: 0.6371 - bag_output_acc: 0.6137 - footwear_output_acc: 0.6505 - pose_output_acc: 0.7332 - emotion_output_acc: 0.7090 - val_loss: 7.5094 - val_gender_output_loss: 0.4568 - val_image_quality_output_loss: 0.9315 - val_age_output_loss: 1.3491 - val_weight_output_loss: 0.9489 - val_bag_output_loss: 0.8524 - val_footwear_output_loss: 0.7714 - val_pose_output_loss: 0.6782 - val_emotion_output_loss: 0.8464 - val_gender_output_acc: 0.7892 - val_image_quality_output_acc: 0.5744 - val_age_output_acc: 0.4033 - val_weight_output_acc: 0.6374 - val_bag_output_acc: 0.6171 - val_footwear_output_acc: 0.6523 - val_pose_output_acc: 0.7083 - val_emotion_output_acc: 0.7282

Epoch 00013: val_loss improved from 7.53510 to 7.50940, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.013.h5
Epoch 14/50
Learning rate:  0.001

Epoch 00014: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 106s 294ms/step - loss: 7.5013 - gender_output_loss: 0.4328 - image_quality_output_loss: 0.9550 - age_output_loss: 1.3728 - weight_output_loss: 0.9554 - bag_output_loss: 0.8386 - footwear_output_loss: 0.7771 - pose_output_loss: 0.5970 - emotion_output_loss: 0.8862 - gender_output_acc: 0.7970 - image_quality_output_acc: 0.5543 - age_output_acc: 0.4036 - weight_output_acc: 0.6364 - bag_output_acc: 0.6224 - footwear_output_acc: 0.6562 - pose_output_acc: 0.7554 - emotion_output_acc: 0.7090 - val_loss: 7.3668 - val_gender_output_loss: 0.4238 - val_image_quality_output_loss: 0.9322 - val_age_output_loss: 1.3522 - val_weight_output_loss: 0.9481 - val_bag_output_loss: 0.8352 - val_footwear_output_loss: 0.7596 - val_pose_output_loss: 0.5885 - val_emotion_output_loss: 0.8512 - val_gender_output_acc: 0.7986 - val_image_quality_output_acc: 0.5779 - val_age_output_acc: 0.4127 - val_weight_output_acc: 0.6339 - val_bag_output_acc: 0.6190 - val_footwear_output_acc: 0.6696 - val_pose_output_acc: 0.7540 - val_emotion_output_acc: 0.7282

Epoch 00014: val_loss improved from 7.50940 to 7.36682, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.014.h5

Epoch 00013: val_loss improved from 7.53510 to 7.50940, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.013.h5
Epoch 15/50
Learning rate:  0.001

Epoch 00015: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 107s 296ms/step - loss: 7.4213 - gender_output_loss: 0.4130 - image_quality_output_loss: 0.9506 - age_output_loss: 1.3612 - weight_output_loss: 0.9503 - bag_output_loss: 0.8346 - footwear_output_loss: 0.7695 - pose_output_loss: 0.5785 - emotion_output_loss: 0.8829 - gender_output_acc: 0.8086 - image_quality_output_acc: 0.5577 - age_output_acc: 0.4075 - weight_output_acc: 0.6372 - bag_output_acc: 0.6275 - footwear_output_acc: 0.6655 - pose_output_acc: 0.7650 - emotion_output_acc: 0.7089 - val_loss: 7.3146 - val_gender_output_loss: 0.4074 - val_image_quality_output_loss: 0.9357 - val_age_output_loss: 1.3539 - val_weight_output_loss: 0.9468 - val_bag_output_loss: 0.8233 - val_footwear_output_loss: 0.7576 - val_pose_output_loss: 0.5718 - val_emotion_output_loss: 0.8413 - val_gender_output_acc: 0.8145 - val_image_quality_output_acc: 0.5779 - val_age_output_acc: 0.4092 - val_weight_output_acc: 0.6369 - val_bag_output_acc: 0.6354 - val_footwear_output_acc: 0.6617 - val_pose_output_acc: 0.7679 - val_emotion_output_acc: 0.7282

Epoch 00015: val_loss improved from 7.36682 to 7.31464, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.015.h5
Epoch 16/50
Learning rate:  0.001

Epoch 00016: LearningRateScheduler setting learning rate to 0.001.
360/360 [==============================] - 107s 297ms/step - loss: 7.3247 - gender_output_loss: 0.3913 - image_quality_output_loss: 0.9469 - age_output_loss: 1.3532 - weight_output_loss: 0.9461 - bag_output_loss: 0.8222 - footwear_output_loss: 0.7567 - pose_output_loss: 0.5512 - emotion_output_loss: 0.8806 - gender_output_acc: 0.8237 - image_quality_output_acc: 0.5573 - age_output_acc: 0.4058 - weight_output_acc: 0.6370 - bag_output_acc: 0.6416 - footwear_output_acc: 0.6738 - pose_output_acc: 0.7773 - emotion_output_acc: 0.7087 - val_loss: 7.3213 - val_gender_output_loss: 0.4207 - val_image_quality_output_loss: 0.9209 - val_age_output_loss: 1.3521 - val_weight_output_loss: 0.9463 - val_bag_output_loss: 0.8320 - val_footwear_output_loss: 0.7649 - val_pose_output_loss: 0.5679 - val_emotion_output_loss: 0.8404 - val_gender_output_acc: 0.8011 - val_image_quality_output_acc: 0.5769 - val_age_output_acc: 0.4043 - val_weight_output_acc: 0.6379 - val_bag_output_acc: 0.6344 - val_footwear_output_acc: 0.6667 - val_pose_output_acc: 0.7624 - val_emotion_output_acc: 0.7282

Epoch 00016: val_loss did not improve from 7.31464
Epoch 17/50
Learning rate:  0.0001
360/360 [==============================] - 107s 296ms/step - loss: 7.4213 - gender_output_loss: 0.4130 - image_quality_output_loss: 0.9506 - age_output_loss: 1.3612 - weight_output_loss: 0.9503 - bag_output_loss: 0.8346 - footwear_output_loss: 0.7695 - pose_output_loss: 0.5785 - emotion_output_loss: 0.8829 - gender_output_acc: 0.8086 - image_quality_output_acc: 0.5577 - age_output_acc: 0.4075 - weight_output_acc: 0.6372 - bag_output_acc: 0.6275 - footwear_output_acc: 0.6655 - pose_output_acc: 0.7650 - emotion_output_acc: 0.7089 - val_loss: 7.3146 - val_gender_output_loss: 0.4074 - val_image_quality_output_loss: 0.9357 - val_age_output_loss: 1.3539 - val_weight_output_loss: 0.9468 - val_bag_output_loss: 0.8233 - val_footwear_output_loss: 0.7576 - val_pose_output_loss: 0.5718 - val_emotion_output_loss: 0.8413 - val_gender_output_acc: 0.8145 - val_image_quality_output_acc: 0.5779 - val_age_output_acc: 0.4092 - val_weight_output_acc: 0.6369 - val_bag_output_acc: 0.6354 - val_footwear_output_acc: 0.6617 - val_pose_output_acc: 0.7679 - val_emotion_output_acc: 0.7282

Epoch 00017: LearningRateScheduler setting learning rate to 0.0001.
359/360 [============================>.] - ETA: 0s - loss: 7.0616 - gender_output_loss: 0.3290 - image_quality_output_loss: 0.9242 - age_output_loss: 1.3293 - weight_output_loss: 0.9307 - bag_output_loss: 0.8004 - footwear_output_loss: 0.7247 - pose_output_loss: 0.4918 - emotion_output_loss: 0.8669 - gender_output_acc: 0.8595 - image_quality_output_acc: 0.5630 - age_output_acc: 0.4136 - weight_output_acc: 0.6402 - bag_output_acc: 0.6522 - footwear_output_acc: 0.6848 - pose_output_acc: 0.8069 - emotion_output_acc: 0.7087
Epoch 00017: LearningRateScheduler setting learning rate to 0.0001.
 - 107s 297ms/step - loss: 7.3247 - gender_output_loss: 0.3913 - image_quality_output_loss: 0.9469 - age_output_loss: 1.3532 - weight_output_loss: 0.9461 - bag_output_loss: 0.8222 - footwear_output_loss: 0.7567 - pose_output_loss: 0.5512 - emotion_output_loss: 0.8806 - gender_output_acc: 0.8237 - image_quality_output_acc: 0.5573 - age_output_acc: 0.4058 - weight_output_acc: 0.6370 - bag_output_acc: 0.6416 - footwear_output_acc: 0.6738 - pose_output_acc: 0.7773 - emotion_output_acc: 0.7087 - val_loss: 7.3213 - val_gender_output_loss: 0.4207 - val_image_quality_output_loss: 0.9209 - val_age_output_loss: 1.3521 - val_weight_output_loss: 0.9463 - val_bag_output_loss: 0.8320 - val_footwear_output_loss: 0.7649 - val_pose_output_loss: 0.5679 - val_emotion_output_loss: 0.8404 - val_gender_output_acc: 0.8011 - val_image_quality_output_acc: 0.5769 - val_age_output_acc: 0.4043 - val_weight_output_acc: 0.6379 - val_bag_output_acc: 0.6344 - val_footwear_output_acc: 0.6667 - val_pose_output_acc: 0.7624 - val_emotion_output_acc: 0.7282
360/360 [==============================] - 108s 301ms/step - loss: 7.0620 - gender_output_loss: 0.3291 - image_quality_output_loss: 0.9250 - age_output_loss: 1.3294 - weight_output_loss: 0.9303 - bag_output_loss: 0.8006 - footwear_output_loss: 0.7244 - pose_output_loss: 0.4921 - emotion_output_loss: 0.8664 - gender_output_acc: 0.8596 - image_quality_output_acc: 0.5626 - age_output_acc: 0.4137 - weight_output_acc: 0.6405 - bag_output_acc: 0.6518 - footwear_output_acc: 0.6851 - pose_output_acc: 0.8068 - emotion_output_acc: 0.7090 - val_loss: 7.2041 - val_gender_output_loss: 0.3942 - val_image_quality_output_loss: 0.9159 - val_age_output_loss: 1.3391 - val_weight_output_loss: 0.9372 - val_bag_output_loss: 0.8127 - val_footwear_output_loss: 0.7507 - val_pose_output_loss: 0.5440 - val_emotion_output_loss: 0.8406 - val_gender_output_acc: 0.8284 - val_image_quality_output_acc: 0.5694 - val_age_output_acc: 0.4102 - val_weight_output_acc: 0.6344 - val_bag_output_acc: 0.6389 - val_footwear_output_acc: 0.6662 - val_pose_output_acc: 0.7832 - val_emotion_output_acc: 0.7282

Epoch 00017: val_loss improved from 7.31464 to 7.20405, saving model to /content/gdrive/My Drive/EIP/Assignment5Dataset/saved_models/A5_2019-12-28 05:38:51.888049_model.017.h5
Epoch 18/50
Learning rate:  0.0001

Epoch 00018: LearningRateScheduler setting learning rate to 0.0001.
360/360 [==============================] - 107s 298ms/step - loss: 6.9183 - gender_output_loss: 0.3038 - image_quality_output_loss: 0.9169 - age_output_loss: 1.3109 - weight_output_loss: 0.9230 - bag_output_loss: 0.7828 - footwear_output_loss: 0.7088 - pose_output_loss: 0.4543 - emotion_output_loss: 0.8626 - gender_output_acc: 0.8714 - image_quality_output_acc: 0.5609 - age_output_acc: 0.4220 - weight_output_acc: 0.6408 - bag_output_acc: 0.6635 - footwear_output_acc: 0.6904 - pose_output_acc: 0.8239 - emotion_output_acc: 0.7091 - val_loss: 7.2113 - val_gender_output_loss: 0.3971 - val_image_quality_output_loss: 0.9136 - val_age_output_loss: 1.3369 - val_weight_output_loss: 0.9366 - val_bag_output_loss: 0.8164 - val_footwear_output_loss: 0.7524 - val_pose_output_loss: 0.5503 - val_emotion_output_loss: 0.8397 - val_gender_output_acc: 0.8264 - val_image_quality_output_acc: 0.5685 - val_age_output_acc: 0.4067 - val_weight_output_acc: 0.6324 - val_bag_output_acc: 0.6399 - val_footwear_output_acc: 0.6716 - val_pose_output_acc: 0.7837 - val_emotion_output_acc: 0.7282

Epoch 00018: val_loss did not improve from 7.20405
Epoch 19/50
Learning rate:  0.0001

Epoch 00019: LearningRateScheduler setting learning rate to 0.0001.
360/360 [==============================] - 107s 298ms/step - loss: 6.8393 - gender_output_loss: 0.2924 - image_quality_output_loss: 0.9092 - age_output_loss: 1.3003 - weight_output_loss: 0.9171 - bag_output_loss: 0.7700 - footwear_output_loss: 0.6956 - pose_output_loss: 0.4411 - emotion_output_loss: 0.8634 - gender_output_acc: 0.8780 - image_quality_output_acc: 0.5658 - age_output_acc: 0.4261 - weight_output_acc: 0.6419 - bag_output_acc: 0.6738 - footwear_output_acc: 0.6944 - pose_output_acc: 0.8293 - emotion_output_acc: 0.7089 - val_loss: 7.2286 - val_gender_output_loss: 0.4083 - val_image_quality_output_loss: 0.9143 - val_age_output_loss: 1.3374 - val_weight_output_loss: 0.9350 - val_bag_output_loss: 0.8222 - val_footwear_output_loss: 0.7548 - val_pose_output_loss: 0.5458 - val_emotion_output_loss: 0.8421 - val_gender_output_acc: 0.8279 - val_image_quality_output_acc: 0.5699 - val_age_output_acc: 0.4062 - val_weight_output_acc: 0.6305 - val_bag_output_acc: 0.6443 - val_footwear_output_acc: 0.6726 - val_pose_output_acc: 0.7847 - val_emotion_output_acc: 0.7282

Epoch 19/50

Epoch 00019: val_loss did not improve from 7.20405
Epoch 20/50
Learning rate:  0.0001

Epoch 00020: LearningRateScheduler setting learning rate to 0.0001.
359/360 [============================>.] - ETA: 0s - loss: 6.7660 - gender_output_loss: 0.2816 - image_quality_output_loss: 0.9069 - age_output_loss: 1.2925 - weight_output_loss: 0.9153 - bag_output_loss: 0.7600 - footwear_output_loss: 0.6840 - pose_output_loss: 0.4162 - emotion_output_loss: 0.8632 - gender_output_acc: 0.8844 - image_quality_output_acc: 0.5700 - age_output_acc: 0.4294 - weight_output_acc: 0.6447 - bag_output_acc: 0.6780 - footwear_output_acc: 0.7010 - pose_output_acc: 0.8384 - emotion_output_acc: 0.7087
Epoch 00019: val_loss did not improve from 7.20405

Epoch 00020: LearningRateScheduler setting learning rate to 0.0001.
360/360 [==============================] - 107s 298ms/step - loss: 6.7640 - gender_output_loss: 0.2814 - image_quality_output_loss: 0.9071 - age_output_loss: 1.2925 - weight_output_loss: 0.9150 - bag_output_loss: 0.7599 - footwear_output_loss: 0.6836 - pose_output_loss: 0.4156 - emotion_output_loss: 0.8627 - gender_output_acc: 0.8844 - image_quality_output_acc: 0.5699 - age_output_acc: 0.4297 - weight_output_acc: 0.6445 - bag_output_acc: 0.6780 - footwear_output_acc: 0.7015 - pose_output_acc: 0.8388 - emotion_output_acc: 0.7089 - val_loss: 7.2203 - val_gender_output_loss: 0.4042 - val_image_quality_output_loss: 0.9136 - val_age_output_loss: 1.3380 - val_weight_output_loss: 0.9368 - val_bag_output_loss: 0.8178 - val_footwear_output_loss: 0.7530 - val_pose_output_loss: 0.5495 - val_emotion_output_loss: 0.8383 - val_gender_output_acc: 0.8328 - val_image_quality_output_acc: 0.5714 - val_age_output_acc: 0.4072 - val_weight_output_acc: 0.6310 - val_bag_output_acc: 0.6404 - val_footwear_output_acc: 0.6706 - val_pose_output_acc: 0.7862 - val_emotion_output_acc: 0.7282

Epoch 00020: val_loss did not improve from 7.20405
Epoch 21/50
Learning rate:  0.0001

Epoch 00021: LearningRateScheduler setting learning rate to 0.0001.
360/360 [==============================] - 107s 298ms/step - loss: 6.6844 - gender_output_loss: 0.2576 - image_quality_output_loss: 0.9016 - age_output_loss: 1.2749 - weight_output_loss: 0.9072 - bag_output_loss: 0.7562 - footwear_output_loss: 0.6819 - pose_output_loss: 0.4124 - emotion_output_loss: 0.8553 - gender_output_acc: 0.8957 - image_quality_output_acc: 0.5720 - age_output_acc: 0.4377 - weight_output_acc: 0.6443 - bag_output_acc: 0.6779 - footwear_output_acc: 0.7073 - pose_output_acc: 0.8408 - emotion_output_acc: 0.7087 - val_loss: 7.2798 - val_gender_output_loss: 0.4199 - val_image_quality_output_loss: 0.9132 - val_age_output_loss: 1.3437 - val_weight_output_loss: 0.9375 - val_bag_output_loss: 0.8246 - val_footwear_output_loss: 0.7577 - val_pose_output_loss: 0.5720 - val_emotion_output_loss: 0.8394 - val_gender_output_acc: 0.8269 - val_image_quality_output_acc: 0.5739 - val_age_output_acc: 0.4072 - val_weight_output_acc: 0.6329 - val_bag_output_acc: 0.6324 - val_footwear_output_acc: 0.6721 - val_pose_output_acc: 0.7872 - val_emotion_output_acc: 0.7282

Epoch 00021: val_loss did not improve from 7.20405
Epoch 00020: val_loss did not improve from 7.20405
Epoch 21/50

Epoch 22/50
Learning rate:  0.0001

Epoch 00022: LearningRateScheduler setting learning rate to 0.0001.
360/360 [==============================] - 107s 298ms/step - loss: 6.6106 - gender_output_loss: 0.2533 - image_quality_output_loss: 0.8925 - age_output_loss: 1.2681 - weight_output_loss: 0.9011 - bag_output_loss: 0.7455 - footwear_output_loss: 0.6648 - pose_output_loss: 0.3932 - emotion_output_loss: 0.8579 - gender_output_acc: 0.8973 - image_quality_output_acc: 0.5747 - age_output_acc: 0.4411 - weight_output_acc: 0.6476 - bag_output_acc: 0.6870 - footwear_output_acc: 0.7111 - pose_output_acc: 0.8494 - emotion_output_acc: 0.7084 - val_loss: 7.2699 - val_gender_output_loss: 0.4174 - val_image_quality_output_loss: 0.9127 - val_age_output_loss: 1.3451 - val_weight_output_loss: 0.9345 - val_bag_output_loss: 0.8241 - val_footwear_output_loss: 0.7614 - val_pose_output_loss: 0.5620 - val_emotion_output_loss: 0.8402 - val_gender_output_acc: 0.8358 - val_image_quality_output_acc: 0.5670 - val_age_output_acc: 0.3998 - val_weight_output_acc: 0.6300 - val_bag_output_acc: 0.6369 - val_footwear_output_acc: 0.6771 - val_pose_output_acc: 0.7862 - val_emotion_output_acc: 0.7277

Epoch 00022: val_loss did not improve from 7.20405

Epoch 22/50
Learning rate: Epoch 00022: early stopping

63/63 [==============================] - 6s 90ms/step
Out[19]:
{'age_output_acc': 0.3998015873015873,
 'age_output_loss': 1.3450532943483382,
 'bag_output_acc': 0.6369047619047619,
 'bag_output_loss': 0.8241012739756751,
 'emotion_output_acc': 0.7276785714285714,
 'emotion_output_loss': 0.8401664069720677,
 'footwear_output_acc': 0.6770833333333334,
 'footwear_output_loss': 0.7614402539200253,
 'gender_output_acc': 0.8358134920634921,
 'gender_output_loss': 0.4173677440673586,
 'image_quality_output_acc': 0.5669642857142857,
 'image_quality_output_loss': 0.9127496717468141,
 'loss': 7.269928137461345,
 'pose_output_acc': 0.7862103174603174,
 'pose_output_loss': 0.561992614515244,
 'weight_output_acc': 0.6299603174603174,
 'weight_output_loss': 0.9345301654603746}
