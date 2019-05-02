<table width=100% border=>
<tr><td colspan=2><img src="images/spacer.png"></td></tr>
<tr><td colspan=2><h1>EXERCISE 07 - ML Foundation in SAP Cloud Foundry - Preparation</h1></td></tr>
<tr><td><h3>SAP Partner Workshop</h3></td><td><h1><img src="images/clock.png"> &nbsp;60 min</h1></td></tr>
</table>


## Description
In this exercise, you’ll learn how to

* access SAP Cloud Foundry Org and Space via SAP CP Cockpit
* create Service Instance and Service Key for ML Foundation
* generate an access token with Postman
* adapt your SAPUI5 app to use your trial ML services instead of the SAP API Business Hub sandbox

## Target group

* Developers
* People interested in SAP Leonardo and Machine Learning


## Goal

The goal of this exercise is to understand how to access SAP Cloud Foundry cockpit, how to setup the ML Foundation service and how to generate a service key for accessing it from an external application.



## Steps

1. [SAP Cloud Foundry Org and Space via SAP CP Cockpit](#cf-org-space)
1. [Create Service Instance and Service Key for ML Foundation](#service-instance-key)
1. [Generate Access Token](#access-token)
1. [Adapt SAPUI5 App to use your Trial ML Foundation Services](#adapt-app)


### <a name="cf-org-space"></a> SAP Cloud Foundry Org and Space via SAP CP Cockpit
You used your SAP Cloud Platform trial account to access the SAP API Business Hub and the SAP Cloud Platform - Neo environment. Now you will learn how to work with ML Foundation Services that are available within your SAP Cloud Platform Global Account.

1. Using Chrome login to the SAP Cloud Platform trial <https://account.hanatrial.ondemand.com/cockpit#/home/trialhome>  
	![](images/01.png)

1. Click on **Cloud Foundry Trial** then the **Trial** subaccount  
	![](images/04.png)

1.	Here you can see some your Cloud Foundry details like the name of your Organization, the number of Spaces and the API endpoint. Click  **Spaces** in the left menu
 	![](images/05.png)

1. Click on the tile named "dev" which is the one related to your space  
	![](images/06.png)

1. You have reached your Cloud Foundry cockpit. At moment there should be no applications available  
	![](images/07.png)

1. You have finished with the preparation of your Cloud Foundry environment.


### <a name="service-instance-key"></a> Create Service Instance and Service Key for ML Foundation
Before we continue we need to create a service instance and get a service key from the ML Foundation service. A service key enables the ML Foundation Service to be used outside the CF environment. In this exercise, you need to create such a key to be used by an external application like Swagger UI or Postman. The service key contains all the URLs and credentials (clientid and clientsecret) required for you to access the ML Foundation service running for your trial account.

1.	Within your space navigate to **Services -> Service Marketplace**, then click on the **ml-foundation-trial-beta** tile  
	![](images/08.png)

1.	Select Instances on the left menu bar and click on **New Instance**  
	![](images/09.png)

1.	Select the Plan **standard** and click **Next**  
	![](images/10.png)

1.	Click **Next**  
	![](images/11.png)

1.	Click **Next**  
	![](images/12.png)

1.	Enter a name for the new instance, like **ml** and click **Finish**  
	![](images/13.png)

1.	Click on the newly created instance  
	![](images/14.png)

1.	Select **Service Keys** in the left menu bar and click the **Create Service Key** button to create a new service key for your instance  
	![](images/15.png)

1.	 Enter a name for this service key like **ml-sk** then click **Save** to save the service key  
	![](images/16.png)

1.	You get a screen like this. Please keep this page open or copy the service key somewhere because you'll need it in the upcoming exercises  
	![](images/17.png)

1. You have successfully generated a service key for the ML Foundation service.


### <a name="access-token"></a> Generate Access Token
For the upcoming exercises you will need an **OAuth2** token to access the ML Foundation services in your Cloud Foundry environment.

1. You can obtain the access token using Postman. Open a new tab in **Chrome** and open **Postman** from the **Apps** menu
	![](images/21.png)

1. Go back to **Chrome** and *copy* the service key **url** and paste it into **Postman** and add the following path to the end of the URL: **/oauth/token?grant\_type=client\_credentials**
	![](images/22.png)

1. Select the **Authorization** tab, choose **Basic Auth** and paste the service key **clientid** as *Username* and **clientsecret** as *Password*
  ![](images/23.png)

1. Press the **Send** button to send the request and the token will be returned in the **access_token** item. You don't need the access token just yet - but now you know how to generate one. Typically an access token is valid for up to 12 hours. Don't forget to add the prefix **Bearer** with a space when pasting into your application!
	![](images/24.png)


### <a name="adapt-app"></a> Adapt SAPUI5 App to use your Trial ML Foundation Services
For the upcoming exercises you will need an **OAuth2** token to access the ML Foundation services in your Cloud Foundry environment.

1. Go back to the **Neo Trial** in SAP Cloud Platform cockpit and navigate to **Connectivity** then **Destinations** and **Edit** the item *sapui5ml-api*
	![](images/25.png)

1. Change the URL to your trial URL for image classification as defined in your Service Key item **IMAGE_CLASSIFICATION_URL** after removing **/image/classification** from the end, then press **Save**
	![](images/26.png)

1. Open SAP Web IDE Full-Stack as used in the previous exercise and for the **MLFSAPUI5_Project_Exercise** project edit **settings.json**. In the *headers* section replace **APIKey** with **Authorization** and paste in your access token as value prefixed by **Bearer** and a space. Finally, **Save** the file
	![](images/27.png)

1. Run the application and test as previously. All should be working OK except that this time it's using your trial ML service rather than the sandbox service from SAP API Business Hub.



## Summary
This concludes the exercise. You should have learned how to

* access SAP Cloud Foundry Org and Space via SAP CP Cockpit
* create Service Instance and Service Key for ML Foundation
* generate an access token with Postman
* adapt your SAPUI5 app to use your trial ML services instead of the SAP API Business Hub sandbox

Please proceed with next exercise.
