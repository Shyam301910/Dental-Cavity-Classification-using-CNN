# Introduction
Dental caries is a major public health problem. Even though in the past50 years there has been a significant decline in dental caries, it is the most common ailment in the U.S., and large segments of the population
experience various barriers to care. Among children and adolescents, dental caries is 4 to 5 times more common than asthma. Data from the National Health and Nutrition Examination Survey, 2011–2012, show that among
children aged 2 to 8 years, 37% had dental caries in their primary teeth. Among adolescents aged 12 to 19 years, the prevalence of dental caries in the permanent teeth was 58%. About 90% of adults aged ≥ 20 years 
had dental caries. The novel approach of our project is to classify images into two classes (binary classification): cavity and non-cavity, and henceforth detect the images with cavity with the help of Convolutional
Neural Network (CNN). 

Due to poverty or unhygienic practices, these diseases are common, and it is estimated that 5% of total medical expenditure in the world is on oral diseases. In this paper, we have focused on detecting cavities. Recent developments in Data Analytics, Machine Learning and Artificial Intelligencehave helped a lot in medical science. The real disease burden of dental caries is the amount of unmet needs or untreated decay. In recent years, there has been a shift in the peak prevalence of untreated tooth decay from children to adults, possibly attributable to socioecological factors. The prevalence of untreated decay in children and adolescents was about 15%. However, the prevalence of untreated decay among adults aged 20 to 64 years was higher: 27% of the adults had decayed teeth that were left untreated. The rates of untreated decay among these adults were higher among Hispanics (36%) and non-Hispanic blacks (42%) than among non- Hispanic whites (22%) and non-Hispanic Asians (17%). Despite the decline in dental caries, disparities persist among different racial, ethnic, educational, and income groups; it remains a modern curse for large segments of the population.

# Architecture of proposed model
![image](https://github.com/Shyam301910/Dental-Cavity-Classification-using-CNN/assets/95332840/054a1d34-a62d-4785-96f0-68564d6b6d78)

# Flowchart of model
![image](https://github.com/Shyam301910/Dental-Cavity-Classification-using-CNN/assets/95332840/33e863b4-80f2-4774-b0d9-0f13293b28b9)

# Dataset
This study was conducted using the pictures we have specifically chosen from Google Images for teeth cavities. It contains images of cavity and non- cavity teeth. The dataset  comprises of 125 images of which 100 images were used for training purposes and 25 images were used for testing purpose. Training set contains 65 images of caries and 35 images of non- caries. Testing set contains 15 images of caries  and 10 images of non- caries. The snapshot of the dataset obtained from the data exploration strategies above is shown in the below Figure.
![image](https://github.com/Shyam301910/Dental-Cavity-Classification-using-CNN/assets/95332840/2764a4ba-edc3-4161-9e4d-064890d2f880)

# Implementation
The proposed approach comprises applying pre-processing methods to our images. All the images were in JPG format in the dataset. We have used ImageDataGenerator from keras.preprocessing.image in python. . These images are then randomly provided to the Deep CNN model as input. The architecture of our Deep CNN model is inspired by functional API to make it the most optimal one. The model proposed for this research  is  a sequential model. The input and output shape of the model is 150 x 150 x 3 and 1 respectively. Our model comprises of 10 layers (3 Convolutional Layers, 3 MaxPooling Layers, 2 Dense Layers, 1 Flatten Layer and 1 Dropout Layer).

The input of shape W x H x V first goes through a Convolution operation of filter size 3x3 and a stride of 1 with same padding and N filters. The kernel is initialized with random numbers and is steadily trained. Same padding is used for the convolutional operation and hence the width and height of the output would also be W and H respectively and the volume would be N. The output of the Convolutional layer (W x H x N) is then passed to the Max Pooling layer of filter size 2 and a stride of 3 with valid padding. The output shape of the Max Pooling layer would be [W/2] x [H/2] x N. To reduce overfitting in the model, we then use a Dropout layer which drops a node with the probability of 0.5% in each iteration. All blocks of the above given architecture are joined sequentially to build the proposed model. The Convolutional layer of first block has 32 filters. Convolutional layer of every block after first block has twice the number of filters as their previous block. Final output of our model is obtained by adding a 1 node  - completely connected layer which predicts class of input as 0 or 1. All convolutional and fully connected layers are activated using rectified linear activation unit (‘relu’) function except for the last 1 node - completely attached layer that is sigmoid function.

The dataset is split into train and test in the ratio of 80:20 respectively. Images from training were used for validation along with random horizontal flip. For zooming purpose, zoom range of 0.2 was used randomly. Graph (Scatter Plot) is also plotted for training and validation accuracy as well as for training and accuracy loss. We also took some pictures from Google (other than the dataset) to check whether our project was working properly for images outside our dataset.

# Model Output Screenshots
![image](https://github.com/Shyam301910/Dental-Cavity-Classification-using-CNN/assets/95332840/15486e45-b015-4262-bf61-4f457b9f0b24)

![image](https://github.com/Shyam301910/Dental-Cavity-Classification-using-CNN/assets/95332840/03891729-e040-4b21-94de-9503ffabec64)


