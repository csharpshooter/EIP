EIP Phase 1 Assignment 4

Contributors: Abhijit Mali

--------------------------------------------------------------------------------------------------------------------------------------------
Assignment 4a submitted annotations on online tool.
---------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------
Assignment 4b 
-------------
Summary
1. Got to learn about image augmentation and cutout. Also learnt a lot about gradcam. I did gradcam on my ResNet20v1 model. As cifar10 has 
32x32 size as I resized my input image to 32x32, and then after getting heatmap I resized them again to 224x224.
2. for heatmap I have used all 10 images from internet. Some of the images also have multiple objects.
3. In the gradcam heatmaps i was not able to detect heatmaps for cats. For most of the images I have got heatmaps at the last convolution layer
or just 2-3 layers belore the last convolution layer. I think that I would have trained my model for more epochs and higher accuracy 
I would have been able to get cat heatmaps as well.
4. Also one thing I found that I have got heatmaps of different objects at different convolution layers. I dont know think this is expected 
behaviour may be something is missing from my side while implementing gradcam


--------------------------------------------------------------------------------------------------------------------------------------------
10000/10000 [==============================] - 2s 166us/step

Test loss: 0.48736147136688235

Test accuracy: 0.8841

--------------------------------------------------------------------------------------------------------------------------------------------
