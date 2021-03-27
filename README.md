# semester_project


In my work, I have applied Faster RCNN architecture to my dataset.

From my understanding, we should have at least 10+ images with different angles of the individual objects. So in my case for 10 classes it should be at least 100 pictures. Data augmentation is a method to provide robustness such as shear, rotation, and exposure. Basically the more quantities and diversity of each object in the training set, the better performance it will have. In my case, I have originial 204 pictures in total for individual objects, and with shear/exposure, I have 494 train images. As for my validation and test dataset, I utilized tote images and splited them in to 1:1 (82:81). The overall actual spliting frames is 494:82:81.
Based on my mAP performance now, it implys that the training images are not enough.

<div style="text-align:center"><img src="./Images/image1.jpg" width="500">

B) I ran experiemnts on Yolov5 and Faster Rcnn with the tote images in test dataset. For Yolov5 the mAP was always at 0 with different epochs and model widths; on the other hand, Faster Rcnn model did converge and return some results when I set epochs = 1500. As mentioned above, individual objects are selected as training sets with top/side views and top/side/ambient light sources. Ideally it should be providing good performance since this is a non-occluded testing set with the same top/side views and top/side/ambient light sources but with all in the tote.

<div style="text-align:center"><img src="./Images/image3.jpg" width="300">

C) Here I used mAP since it provide both false potivie and true positive feedback (also mAP is based on top of IoU). Here my best performance I get 0.227 at mAP_50. My best observation for this low performance is that I noticed that the augmentation didn't take bounding boxes into consideration, so the IoU effects the results.
<div style="text-align:center"><img src="./Images/image2.jpg" width="1000">

<div style="text-align:center"><img src="./Images/image4.jpg" width="500">

d) A short commentary related to the observed accuracy. Your solutions probably won't be perfect, and that's perfectly fine. An important thing is if you understand why it is not perfect and what should be corrected in the second half of the semester, especially in a more complex setup when objects with obstruct each other. 

Note: There is no page limit for a report since you may want to attach pictures, graphs, etc. One page is probably too little to present the entire work, but try to be concise and think about 8 two-column pages (a typical limit for a vision conference paper) should be absolute maximum.

2. Current version of your programs with instructions how to run them.

Your program(s) should pick one picture of the tote from the validation set (please attach this sample to your codes) and present the processing result. We should be able to run your programs without any edits -- please double check before submission that the codes are complete and run correctly. Please provide detailed instructions in your report how to run the codes: which version of Python you use, which packages we need to install (attaching the dependency file is a nice thing to do), etc.

3. Only for students working in groups:

Indicate in the report which part was done by which teammate, as in Computer Vision I class.

