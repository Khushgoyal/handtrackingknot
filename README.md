# Classical Machine Learning applied to surgical knot analysis( hand tracking knot )


This thesis project focuses on the automated framework for video-based surgical knot assessment that is building on the work of the Irfan Essa's paper "Video Based Assessment of OSATS Using Sequential Motion Textures". He showed assessments using the OSATS (Objective Structured Assessment of Technical Skills) criteria, whereas this thesis focuses on the following aspects
of surgical motion. Our surgical knot tying hand gesture system divides the video into two classes forefinger throw and backhand throw. The framework is tested on different levels performing basic surgical knot on knot tying kit. This thesis demonstrates the extraction of features like HOG-HOF from the video, compressed by k-means cluster and pass it to SVM
with different kernel. Subsequent to extricating the features or keypoints for each video after using the Saptiotemporal
Interest Point (STIPs), a vector quantization method maps key points or features from each video into a unified dimensional histogram vector (bag-of-words) after K-means clustering. This histogram is treated as a feature vector for a binary class SVM to fabricate the classifier where data is divided into 80:20(training, testing) dataset and also performs 3-fold cross-validation on the dataset.

This the data collection part where RGB and Depth Image is identified and video has been captured from it.
![sample](https://user-images.githubusercontent.com/44482765/65905494-92ecf080-e3b8-11e9-8aa9-5dd7aeadddc5.png)

Flow Chart of the project.
<img width="680" alt="graph" src="https://user-images.githubusercontent.com/44482765/65905641-d7788c00-e3b8-11e9-80a0-fac15488af50.png">

How STIP features have been detected from the .avi file

![hand](https://user-images.githubusercontent.com/44482765/65905710-fc6cff00-e3b8-11e9-8bb3-314c38ae498c.png)

This whole process is done by the Laptev Software where you can insert .avi file as input and retrive STIP points of the video which helps to identifies movable object per frame.

After detecting points, we divided into two parts fft and bht where both are grouped by kmeans cluster and after BOW are applied on it.
After whole process we got 1D array from more than 10k-40k STIP points of moveable object per frame.

We got the corelation data after distribution
<img width="907" alt="co" src="https://user-images.githubusercontent.com/44482765/65905972-86b56300-e3b9-11e9-8652-24c15247d60f.png">


Confusion Matrix of the results using linear kernel.
<img width="350" alt="con1" src="https://user-images.githubusercontent.com/44482765/65905993-8e750780-e3b9-11e9-8732-c33bbc2da60b.png">




Confusion Matrix of the results using rbf kernel.
<img width="334" alt="con2" src="https://user-images.githubusercontent.com/44482765/65906014-99c83300-e3b9-11e9-9f0d-b851618bda22.png">



Confusion Matrix of the results using poly kernel.
<img width="323" alt="con3" src="https://user-images.githubusercontent.com/44482765/65906075-b82e2e80-e3b9-11e9-9bb7-6e14b46dc71e.png">




Finally, we got accuracy of 90 degree camera position
<img width="400" alt="Screenshot 2019-09-30 at 7 37 34 PM" src="https://user-images.githubusercontent.com/44482765/65906184-f297cb80-e3b9-11e9-8d96-b9f52b7d8bb1.png">



and Accuracy for egocentric data.
<img width="407" alt="Screenshot 2019-09-30 at 7 37 39 PM" src="https://user-images.githubusercontent.com/44482765/65906188-f4fa2580-e3b9-11e9-9d22-40f961b08956.png">





