<embed src="https://github.com/LynetteGao/Facial-Expression-Recognition/blob/master/639_project_proposal.pdf" width="1000px" height="800px" toolbar=0/>



## 639 project proposal - Facial Expression Classification

September 2020

Katherine Fu jfu57@wisc.edu

Lynette Gao qgao38@wisc.edu

Flossie Wan kwan9@wisc.edu

### Abstract

Image processing and recognition are essential and widely used in different areas of studies. Classifying facial and emotional expression is of great interest in the deep learning field as a high-performance recognition model could lead to more complex classification tasks. Facial and emotional expression classification could be commonly applied in the real world. For example, businesses could perform facial recognition on users' selfies and analyze their rate of satisfaction on the products. More advanced applications could be the development of humanoid robots with the integration of facial and emotional recognition functionality. Thus, we need to have a better understanding of its basic implementation. In this project, we will utilize the image samples from the Real-world Affective Faces (RAF) Database. Its database contains 15339 facial images with 12271 training samples and 3068 testing samples and 37 landmark location labels. The images are grouped into 7 emotions including surprise, fear, disgust, happiness, sadness, anger, and neutral. We will implement multiple Convolutional Neural Network (CNN) architectures and evaluate their performance using accuracy metric.  

### Significance
Detecting facial expression promotes communication between individuals. For humans, recognizing facial expressions and emotions is a basic skill that is learned at an early age. We can look at a person’s face and can quickly recognize the common emotions of anger, happiness, surprise, disgust, sadness, and fear. However, to transfer this skill to a machine is a complex task. Meanwhile,there are many practical uses of the emotion detection, if the facial expression algorithm can be successfully implemented. For example, the US Department of Transportation claims that driving-related errors cause around 95 percent fatal road accidents \cite{Gupta2018}. In this case, facial emotion detection can find us find subtle changes in facial micro-expressions that precedes drowsiness and send personalized alerts to the driver. Therefore, we are interested in developing a deep learning algorithm to automatically understand human's emotion given an image.

### Current work
Researchers have devoted decades of engineering time to writing computer programs that recognize a feature with accuracy. In the field of computer vision and machine learning, various facial expression recognition  systems have been explored to encode expression information from facial representations. The majority of the traditional methods have used handcrafted features or shallow learning, such as local binary pattern. Recently, with large amount of data available, deep learning has recently become a hot research topic and has achieved state-of-the-art performance. Some of the example algorithm includes Convolutional neural network (CNN), Deep belief network (DBN), Deep autoencoder (DAE) and Generative Adversarial Network (GAN) \cite{Li_2020}.

### Planning
Oct 1 - Oct 15:  Reading reference materials and start to build a benchmark model 

Oct 16 - Nov 3: Implementing network and algorithms

Nov 3 - Dec 2: Training and improving models. Prepare for presentation and final write-up

### Experiments
##### Image processing
Our image data have already been aligned based on the two-eye locations and the position of the mouths and resized to 100*100 pixels. Since our samples include faces from different genders and races, it becomes important for us to take this information into consideration. Faces in some photos are pointing into different angles, which could result in various light and color intensity. Since the upright faces are of great interest, we will perform basic rotations to those images. 

In some photos, people wear glasses. Those images would not be a big issue for our project since these glasses are transparent and we can still be able to detect the facial features. 

It is also essential to include the images that show neutral emotion in our samples. We will use those images to improve the facial detection ability.

##### Network Training
There are many existing architectures and techniques that can be applied to facial expression recognition. We plan to implement multiple models using Convolutional Neural Network (CNN) architectures, including VGGNet \cite{simonyan2014deep}, AlexNet \cite{NIPS2012_4824}, GoogLeNet \cite{szegedy2014going} and ResNet \cite{he2015deep}. CNN is one of the most widely-used technique for facial expression recognition, as it has been proved to be robust to face location and good at normalization \cite{Fasel_2002}. All of the models we choose are competitors in ImageNet Large Scale Visual Recognition Challenge (ILSVRC), with different training methods and achievements \cite{Khan_2020}\cite{Li_2020}. We want to experiment on the parameters of those models. By manipulating parameters like batch size, layer type, etc., we hope to achieve best performance of each model, and evaluate the advantages and shortcomings of our models.

### Evaluation
To evaluate the performance of our model, we primarily plan to use their accuracy of recognizing facial expressions.  Confusion matrix can also be used to evaluate whether our model is biased toward one or more classes (emotions, in our case). We can also detect over-fitting issue by evaluating validation metric, like loss. The turning point of loss function from going down to going up indicates over-fitting in our model.

### Resources
Our project will be written in python with basic python libraries. We are using Real-world Affective Faces Database (RAF-DB) \cite{li2017reliable} for labeled facial expressions. All our models can be implemented with TensorFlow Keras API. TensorBoard will be used for analyze the performance of our model by evaluating loss and accuracy. All the training, testing and analyzing processes will be done on our personal laptops.
