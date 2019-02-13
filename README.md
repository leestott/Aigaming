# AIGaming Cognitive Services Computer Vision API

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