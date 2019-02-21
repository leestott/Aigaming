# AIGaming Cognitive Services Computer Vision API

Azure's Computer Vision service provides developers with access to advanced algorithms that process images and return information. To analyze an image, you can either upload an image or specify an image URL. The images processing algorithms can analyze content in several different ways, depending on the visual features you're interested in. For example, Computer Vision can determine if an image contains adult or racy content, or it can find all of the human faces in an image.

You can use Computer Vision in your application by using either a native SDK or invoking the REST API directly. [Computer Vision Docs page](https://docs.microsoft.com/en-us/azure/cognitive-services/Computer-vision/Home) broadly covers what you can do with Computer Vision

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fleestott%2FAigaming%2Fmaster%2Fazuredeploy.json" target="_blank">
<img src="https://github.com/leestott/Aigaming/blob/master/Images/deploytoazure.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fleestott%2FAigaming%2Fmaster%2Fazuredeploy.json" target="_blank">
<img src="https://github.com/leestott/Aigaming/blob/master/Images/visualizebutton.png"/>
</a>

This template deploys an Cognitive Services Computer Vision API for the AIGaming Challenge.
In the outputs section it will show the Keys and the Endpoint.

Top deploy simply click on the Deploy to Azure Button above, this will launch the Azure Portal and sign up in you will then be presented with the following screen.

![AzureDeploy](/Images/Deploy.PNG)

* On the resource group select create new and create a new resource group called AIGaming
![ResourceGroupName](/Images/Aigaming.PNG)
* Tick I agree to the terms and conditions stated above check box
* Finally select purchase.

This will now create and deploy a Microsoft Cognitive Services Key for Cognitive Vision called AIGamingCVApi under the S1 plan (This plan is chargeable to ensure your competitive when playing the AIGaming challenge) and host it within the WestEurope region

## Getting your Cognitive Services Key

To get the key required for your cognitive services vision key go to [http://portal.azure.com](http://portal.azure.com)

Log into your Portal account account and select resource groups, Select AIGaming Resource Group

![ResourceGroups](/Images/Cognitive.png)

Then click on the AIGamingCVApi

![CognitiveKey](/Images/CognitiveKey.png)

Then Click 1. The Cognitive Keys this will display your keys please use Key1 simply copy and paste Key 1 from [http://portal.azure.com](http://portal.azure.com) to your AIGaming Coding Template

![Key](/Images/Key.png)

Simply replace the following 'YOUR-MICROSOFT-COMPUTER-VISION-API-KEY-HERE' with your Key

<code>

headers_vision = {'Ocp-Apim-Subscription-Key': 'YOUR-MICROSOFT-COMPUTER-VISION-API-KEY-HERE'}
vision_base_url = "https://westeurope.api.cognitive.microsoft.com/vision/v2.0/"

</code>

If your more familiar with the Azure CLI you can use the following command to create a resource group and key and list your keys
See getting started with [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest)

<code>

az login

az group create -n AIGaming -l westeurope

az cognitiveservices account create -n AIGamingCVApi -g AIGaming --sku S1 --kind ComputerVision -l westeurope

az cognitiveservices account show -g AIGaming -n AIGamingCVApi

az cognitiveservices account keys list -g AIGaming -n AIGamingCVApi

</code>

Your now ready to take part in the challenge