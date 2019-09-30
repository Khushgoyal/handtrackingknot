# handtrackingknot


This thesis project focuses on the automated framework for video-based surgical knot assessment that is building on the work of the Irfan Essa's paper "Video Based Assessment of OSATS Using Sequential Motion Textures". He showed assessments using the OSATS (Objective Structured Assessment of Technical Skills) criteria, whereas this thesis focuses on the following aspects
of surgical motion. Our surgical knot tying hand gesture system divides the video into two classes forefinger throw and backhand throw. The framework is tested on different levels performing basic surgical knot on knot tying kit. This thesis demonstrates the extraction of features like HOG-HOF from the video, compressed by k-means cluster and pass it to SVM
with different kernel. Subsequent to extricating the features or keypoints for each video after using the Saptiotemporal
Interest Point (STIPs), a vector quantization method maps key points or features from each video into a unified dimensional histogram vector (bag-of-words) after K-means clustering. This histogram is treated as a feature vector for a binary class SVM to fabricate the classifier where data is divided into 80:20(training, testing) dataset and also performs 3-fold cross-validation on the dataset.
