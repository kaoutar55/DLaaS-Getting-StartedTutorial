#Deep Learning as a Service using IBM Cloud

**Note: These steps use a Command Line Interface (CLI). There is an alternative browser used interface** 

Deep Learning as a Service embraces a wide array of popular open source frameworks like TensorFlow, Caffe, PyTorch and others, and offers them truly as a cloud-native service on IBM Cloud, lowering the barrier to entry for deep learning. It combines the flexibility, ease-of-use, and economics of a cloud service with the compute power of deep learning. 

Here we illustrate how to run deep learning experiments using Deep Learning as a Service (DLaaS) capabilities in Watson Machine Learning.

In order to use IBM DLaaS, you will need to have two IBM Cloud services a Cloud Object Storage and a Watson Machine Learning service.

**Cloud Object Storage (COS)** serves as storage for the training data as well as training results and logging/monitoring data. 
**Watson Machine Learning (WML)** which handles sotring the training and experiment information, executing the training runs and experiments, and deploying trained models.

#### Training a deep learning neural networks involves the following steps:

Create a Watson Machine Learning service instance
Setup COS to define buckets for reading the training data and buckets for writing the training results. Upload yor data to the buckets.
Create training definition which outline the neural network (NN) architecture and the references to the COS bucket containing the input training data and output COS bucket for writing training results.
Create an experiment config file which includes the the COS bucket with input training data, the COS bucket to write the training results, and the required GPU.
Monitor the experiment results.

#### Prerequisites:
Before staring the tutorial make sure you have the following prerequisites.
    *Access to IBM Cloud internal account.
    *Your IBM Cloud API Key
    *Python version > 3.6 
    *IBM Cloud cli 
    *IBM Cloud Machine learning plugin
    *Watson ML Client library

If you do not have the above prerequisites, you can follow the instructions here.

### [Steps for one time Setup:](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/onetimesetup.md)

Step 0. Pre requisites

Step 1. Login to your bluemix account

Step 2. Create a Watson ML Instance

    2.1 Setup a Watson ML Instance : Create WML Access key  
    2.2 Set up Environment variables
    
    
Step 3. Define a [Cloud Object Storage](https://www.ibm.com/cloud/object-storage/faq) Instance to store your data.

    3.1. Create a cloud storage instance
    3.2. Get security credentials
    3.3 Create and configure your aws profile
    3.4. Create an alias
    3.5. Create a bucket
    
You can find the one time setup instructions [HERE](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/onetimesetup.md)
    
 
 ### [Steps for the Demo:](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/demo.md)
 
 0: Get a dataset
 
 1: Upload your dataset to the bucket
 
 2: Edit your manifest file
 
    2.1. Copy the template manifest
    
    2.2. Edit the configuration file
 
 3: Send code to run on Watson Studio!
 
    3.1. Zip all the code and models into a .zip file
    
    3.2. Send your code and manifest to IBM Watson Studio
 
 4: Monitor the training
 
 **You can find the Steps for Demo [HERE](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/demo.md)**

 **Click [HERE](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/usefulcommands.md)  for Other useful commands**
