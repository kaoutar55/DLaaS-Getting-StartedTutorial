# Deep Learning as a Service using IBM Cloud

**Note: These steps use a Command Line Interface (CLI). There is an alternative browser used interface** 

Deep Learning as a Service embraces a wide array of popular open source frameworks like TensorFlow, Caffe, PyTorch and others, and offers them truly as a cloud-native service on IBM Cloud, lowering the barrier to entry for deep learning. It combines the flexibility, ease-of-use, and economics of a cloud service with the compute power of deep learning. 

Here we illustrate how to run deep learning experiments using Deep Learning as a Service (DLaaS) capabilities in Watson Machine Learning.

In order to use IBM DLaaS, you will need to have two IBM Cloud services a Cloud Object Storage and a Watson Machine Learning service.**Cloud Object Storage (COS)** serves as storage for the training data as well as training results and logging/monitoring data. **Watson Machine Learning (WML)** which handles sotring the training and experiment information, executing the training runs and experiments, and deploying trained models.

#### Training a deep learning neural networks involves the following steps:

Create a Watson Machine Learning service instance
Setup COS to define buckets for reading the training data and buckets for writing the training results. Upload yor data to the buckets.
Create training definition which outline the neural network (NN) architecture and the references to the COS bucket containing the input training data and output COS bucket for writing training results.
Create an experiment config file which includes the the COS bucket with input training data, the COS bucket to write the training results, and the required GPU.
Monitor the experiment results.

#### Prerequisites:
Before staring the tutorial make sure you have the following prerequisites.

    1. Access to IBM Cloud internal account.
    2. Your IBM Cloud API Key
    3. Python version > 3.6 
    4. IBM Cloud cli 
    5. IBM Cloud Machine learning plugin
    6. Watson ML Client library
    7. AWS Cli

If you do not have the above prerequisites, you can follow the instructions [here.](https://github.com/nfairoza/DLaaS-Getting-StartedTutorial/blob/master/pre-req.md)

### Setting up your account to run experiments

IBM Cloud account includes many interacting components and systems such as Orgs, Spaces, Resource groups, Access groups etc,.
You can click [here](https://console.bluemix.net/docs/account/account_overview.html#overview) for more information. 

`Note: MIT-IBM AI Lab users should have access to your project-specific Org and Resource group`

Before you start running your experiments, you need to target right Cloud Foundry org, space and resource group. Then, set up your account with a Watson Machine Learning service, a Cloud Object store instance and create your aws profile.


### Login to IBM Cloud and target the correct Region, Resource group, Org and Space 

#### Login Using API Key:   
Login to your IBM Cloud account using the apiKey (see [pre-requisite document](https://github.com/nfairoza/DLaaS-Getting-StartedTutorial/blob/master/pre-req.md) for . instructions on how to get your API key.

```
$ bx login --apikey <your_api_key>
```

#### Target correct Region, Resource group, Org and Space.
After log in you need to target the correct region, organization, space and resourcegroup.
It is recomended to target 'us-south' region and space 'dev'.
You can find the list of orgs you have access to using the command `$ bx target account orgs`

`Note: MIT-IBM Watson AI Lab users can target'MITIBMWatsonAiLab' org and resource group. It is recomended to use your project-specific org name. If you use your project specific org your resource group name will be <orgname>_resourcegroup.`

Use the "bx target" command to target the correct Cloud parameters.
```
$ bx target -r us-south -g MITIBMWatsonAiLab -o MITIBMWatsonAiLab -s dev
```
You can click [here](https://github.com/nfairoza/DLaaS-Getting-StartedTutorial/edit/master/onetimesetup.md) and follow the instructions to set up your Cloud Object Store and Watson ML service.

 
 ### DLaas Tutorial with sample model and Data
 
 After the setup from previous section, you are ready to use DLaaS to run your training. 
 
 
 In this repository we provide you, sample data and model. You can follow the inscructions [here](https://github.com/mypublicorg/DLaaS-Getting-StartedTutorial/blob/master/demo.md) to run and monitor training in your DLaaS setup using our sample data and model.


 **Click [HERE](https://github.com/mypublicorg/pytorch-cifar10-in-ibm-cloud/blob/master/usefulcommands.md)  for Other useful commands**
