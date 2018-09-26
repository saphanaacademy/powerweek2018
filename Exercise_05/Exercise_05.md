<table width=100% border=>
<tr><td colspan=2><img src="images/spacer.png"></td></tr>
<tr><td colspan=2><h1>EXERCISE 05 - ML APIs Exploration</h1></td></tr>
<tr><td><h3>SAP Partner Workshop</h3></td><td><h1><img src="images/clock.png"> &nbsp;30 min</h1></td></tr>
</table>


## Description
In this exercise, you’ll learn how

* To consume pretrained SAP Leonardo Machine Learning services from SAP API Business Hub sandbox using API Business Hub and Postman

## Target group

* Developers
* People interested in SAP Leonardo and Machine Learning


## Goal

In this exercise you can experience how easy it is to use the SAP Leonardo Machine Learning foundation services sandbox on SAP API Business Hub. The models are already pre-trained and can be tried out on the web page.


## Prerequisites

Here below are prerequisites for this exercise.

* A trial account on the SAP Cloud Platform. You can get one by registering here <https://account.hanatrial.ondemand.com>
* Download the files [Topic_Detection.zip](files/Topic_Detection.zip?raw=true) and [test_images.zip](files/test_images.zip?raw=true) and save them - they will be used later in this exercise.


## Steps

1. [Use SAP Leonardo ML Topic Detection on API Business Hub](#topic-detection)
1. [Use SAP Leonardo ML Image Classification on API Business Hub](#image-classification)
1. [Use SAP Leonardo ML Image Classification on API Business Hub from Postman](#image-classification-postman)



### <a name="topic-detection"></a> Use SAP Leonardo ML Topic Detection on API Business Hub
1. Open SAP Business Hub in your browser <https://api.sap.com>
	![](images/01.png)

1. 	Search on **leonardo func**  
	![](images/02.png)

1. 	Choose the API Package **SAP Leonardo Machine Learning - Functional Services** then search on **topic**  
	![](images/03.png)

1. 	Choose **Inference Service for Topic Detection**  
	![](images/04.png)

1. We need to login to test the service: click on the **Log On** button at the top right corner  
	![](images/05.png)

1. Enter the credentials for your SAP Cloud Platform trial account and click on the **Log On** button  
	![](images/06.png)

1. For **POST** request **/topic-detection** click on **Try out**
	![](images/07.png)

1. Under **files** press the **Choose File** button  
	![](images/08.png)

1. Choose the *Topic_Detection.zip* file (you have already downloaded it in the prerequisites section) containing some text files  
	![](images/09.png)

1. Scroll down and under **options**, paste the following parameters then click on the **Execute** button  

	```json
	{"numTopics":3, "numTopicsPerDoc":2, "numKeywordsPerTopic":15}
	```
	![](images/10.png)

1. You should receive a **Response Code** of **200**. Check the result in the **Response body**: you should see a content like this  
	![](images/11.png)

1. Try again by changing the values for **numTopics** to **2** and **numTopicsPerDocs** to **1**  then pressing **Execute**
	![](images/12.png)

1. What has changed? You should receive an answer similar to this  
	![](images/13.png)

1. You have successfully used the Topic Detection API service to find **numKeywordsPerTopic** keywords and **numTopics** topics across all documents. The topics get a number, starting with 0. So, if you define 3 Topics, they will be numbered with 0, 1, 2. With **numTopicsPerDoc** you define how many of the topics of the entire document corpus can be found in one document. The algorithm chooses the number of topics which fits best and assigns them a score which is normalized to be between 0 and 1.


### <a name="image-classification"></a> Use SAP Leonardo ML Image Classification on API Business Hub

1. Go back to the **SAP API Business Hub** page, search on **leonardo func**, choose the API Package **SAP Leonardo Machine Learning - Functional Services**, then search on **image class** and select **Inference Service for Customizable Image Classification**  
	![](images/14.png)

1. For **POST** request **/classification** click on **Try out** then scroll down and click the **Choose File** button
	![](images/15.png)

1. Choose the *test_images.zip* file (you have already downloaded it in the prerequisites section) and press the **Execute** button  
	![](images/16.png)

1. Look at the response code: it should be 200, meaning that the request was successful. Then look at the *Response body* - you should be able to read the predictions against the images contained in the zip file you uploaded. For example here you can see that the *iPhoneX.jpg* has been labeled as a *cellular telephone* with a score of *0.47*  
	![](images/17.png)

1. Looking down at another image, like the *tennis_ball.jpg* you can see that the it has been correctly labeled as a *tennis ball* with a score of *0.99*  
	![](images/18.png)

1. Congratulations! You have successfully performed image classification on API Business Hub


### <a name="image-classification-postman"></a> Use SAP Leonardo ML Image Classification on API Business Hub from Postman

1. Open a new tab in **Chrome** and open **Postman** from the **Apps** menu
	![](images/19.png)

1. Go back to **Chrome** and *copy* the **Request URL** for image classification
	![](images/20.png)

1. Back in **Postman** set the *method* to **POST** and paste the **Request URL**
  ![](images/21.png)

1. Go back to **Chrome**, scroll up and press the **Show API Key** button then press the **Copy Key and Close** button
  ![](images/22.png)
  ![](images/23.png)

1. Back in **Postman** select the **Headers** tab, add a *key* named **apikey** and paste your API Key as *Value*
  ![](images/24.png)

1. Select the **Body** tab and ensure **form-data** is selected. Enter a *key* named **files**, set the option to **File** then press the **Choose Files** button and choose the *test_images.zip* file as used earlier in this exercise
  ![](images/25.png)

1. Press the **Send** button to send the request
  ![](images/26.png)

1. Look at the status: it should be *200 OK*, meaning that the request was successful. Then look at the *Body* - you should be able to read the predictions against the images contained in the zip file you uploaded and the values should be the same as when using the API Business Hub previously

1. Congratulations! You have successfully performed image classification from Postman


## Summary
This concludes the exercise. You should have learned how to use the SAP Leonardo Machine Learning foundation sandbox services on SAP API Business Hub.

You are now able to:

* Browse through API Business Hub to find the latest functional and business services of SAP Leonardo ML foundation
* Test SAP Leonardo ML foundation services directly on API Business Hub
* Test SAP Leonardo ML foundation services from Postman

Please proceed with the next exercise.
