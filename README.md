# Image-segmebtation-using-Mask-R-CNN

Semantic Segmentation : is a technique that detects , for each pixel , the object category it belongs to ,
Instance Segmentation : it dives a bit deeper, it identifies , for each pixel, the object instance it belongs to. The main difference is that differentiates two objects with the same labels in comparison to semantic segmentation.

we can do image segmentation using many networks like U-net and mask R-CNN

mask R-CNN is based on convolution neural network with some modification as follows :

1-R-cnn:
 which depends on Region proposal , it looks on the image and generate boxes around the area that may contain objects , we crop this regions or boxes from the image and pass it to CNN and we have two outputs , the first one is the predicted class  and the second one is the predicted bounding box  , this method is time intensive
2-Fast R-CNN:
It runs the entire image through the CNN only once , but instead cropping the original image , we get our region of interest from the output feature maps from the CNN which we feed them to a fully connected layer to get the same two outputs as R-CNN
3-Faster R-CNN:
It is the same as Fast R-CNN , but it uses the produced feature maps as input to separate region proposal network , so it predicts its own region from the features inside the network , if the region has corners and edges so its ROI” region of interest ”, then there is a binary classification for each ROI to say its an object or not , if it is an object it continues to the classification step as R-CNN
4- Mask R-CNN:
Mask R-CNN has an additional branch for predicting segmentation masks on each Region of Interest (RoI) in a pixel-to pixel manner
