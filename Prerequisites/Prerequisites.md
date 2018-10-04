<table width=100% border=>
<tr><td colspan=2><h1>PREREQUISITES</h1></td></tr>
<tr><td><h3>SAP Partner Workshop</h3></td><td><h1><img src="images/clock.png"> &nbsp;30 min</h1></td></tr>
</table>


## Description

In this exercise, you’ll go through the basic steps of setting up the development environment required for SAP Leonardo and SAP Cloud Platform workshop.  


## Target group

* Application Developers
* People interested in learning about SAP Leonardo and SAP Cloud Platform  


## Goal

The goal of this exercise is to have your workstation/laptop well prepared in order to attend to the SAP Leonardo and SAP Cloud Platform workshop.  


## Prerequisites

Below are prerequisites required for the exercises in this workshop.  


1. [Bring Your Own Laptop with Admin Access](#laptop)
1. [Remote Desktop Connection](#rdc)
1. [Sign up for SAP Cloud Platform Neo trial account](#sign-up-neo)
1. [Sign up for SAP Cloud Platform Cloud Foundry trial account](#sign-up-cf)
1. [Install Cloud Foundry CLI](#install-cf-cli)
1. [Install MTA Plugin](#install-mta-cli)
1. [Install ML Foundation CLI](#install-ml-cli)
1. [Install Minio Client](#install-minio-client)
1. [Install Java JRE](#install-java-jre)
1. [Install Paho Client](#install-paho-client)
1. [Install Chrome Postman application](#postman)
1. [Install Chrome Postman Interceptor extension](#postman-interceptor)  
1. [Install Python](#install-python)
1. [Install OpenSSL](#install-openssl)


## <a name="laptop"></a> Bring Your Own Laptop with Admin Access

Please bring the laptop that you have admin access for hands-on exercises.   


## <a name="rdc"></a> Remote Desktop Connection

In order to connect with the Virtual Machines we have prepared for you, you need to have the Remote Desktop Connection (RDC) tool installed on your machine. For Windows users, RDC comes already installed, so if you have Windows you don't have to worry about it. If you are MAC user, instead, you can download it for free from the Mac App Store.  
	![](images/01.png)


## <a name="sign-up-neo"></a>Sign up for SAP Cloud Platform Neo trial account
You need Neo trial SAP Cloud Platform to complete some of the hands-on exercises.

1.	Sign up for SAP Cloud Platform trial account from <https://account.hanatrial.ondemand.com/>  
	![](images/11.png)

	> NOTE: If you don’t have an account on SAP Cloud Platform yet, go to the Sign up for a free trial account tutorial, and then come back to this step.

1. After you have logged in, click on **Home**.  Then, click on **Neo Trial**  
	![](images/12.png)

1. This will take you to the **Overview** page of the SAP Cloud Platform Cockpit for Neo stack  
	![](images/13.png)

1.	From SAP Cloud Platform Cockpit, click on Services. Ensure the following service is enabled	 
	- SAP Web IDE Full-Stack

	![](images/14.png)


## <a name="sign-up-cf"></a>Sign up for SAP Cloud Platform Cloud Foundry trial account
Sign up also for SAP Cloud Platform Cloud Foundry trial account.

1.	From SAP Cloud Platform Cockpit, click on Home.  Then, click on **Cloud Foundry Trial**. Select **Region** *Europe (Frankfurt)* and press **OK**  
	![](images/15.png)
1.	Select the Global account that matches your login. Next, select the trial sub-account  
	![](images/16.png)	 


## <a name="install-cf-cli"></a>Install Cloud Foundry CLI
Cloud Foundry CLI is the official command line client for Cloud Foundry. It provides a set of commands for managing your apps.  

1.	Cloud Foundry CLI can be downloaded here <https://github.com/cloudfoundry/cli#downloads>. Just select the installer which matches your Workstation's Operating System
	![](images/19.png)

1. Once the file has been downloaded, please extract it then install by double clicking on the extracted file.


## <a name="install-mta-cli"></a>Install MTA Plugin
The SAP Cloud Platform Cloud Foundry Plugins are used to extend the Cloud Foundry CLI with additional commands. The MTA Plugin performs operations on multi-target applications (MTAs) such as deploying, removing, viewing, etc.  

1.	The MTA Plugin can be downloaded here <https://tools.hana.ondemand.com/#cloud>. Scroll down to the **Plugins** section and download MTA plugin which matches your Workstation's Operating System

1. Once the file has been downloaded, please install by issuing the following command from a command prompt in the folder where you downloaded the file: **cf install-plugin -f \<downloaded-filename\>** where the name of the downloaded file replaces **\<downloaded-filename\>**.


## <a name="install-ml-cli"></a>Install Machine Learning Foundation CLI
SAP Leonardo Machine Learning foundation Command Line Interface (CLI) is a way of interacting with the foundation and using its services, e.g. to simplify data upload for Retraining and Bring your Own Model scenarios as described in the official documentation.

1.	Machine Learning Foundation CLI can be downloaded here <https://tools.hana.ondemand.com/#mlfoundation>. Just select the installer which matches your Workstation's Operating System
	![](images/19_02.png)

1. Once the file has been downloaded, please extract the file and install by issuing the following command from a command prompt in the folder where you extracted the file: **cf install-plugin -f \<extracted-filename\>** where the name of the extracted file replaces **\<extracted-filename\>**.


## <a name="install-minio-client"></a>Install Minio Client

1. Follow instructions on <https://docs.minio.io/docs/minio-client-quickstart-guide.html> to install the client for your operating system.


## <a name="install-java-jre"></a>Install Java JRE

1.	Download and install Java JRE from this link <https://www.java.com/en/>  
	![](images/05.png)

1.	Ensure you download and install the 64 bit version  
	![](images/05b.png)
	![](images/05c.png)


## <a name="install-paho-client"></a>Install Paho Client

1.	Download and install Paho Client from this link <https://help.sap.com/viewer/e9e5e6a2fa144c31b5b5d5c144047dec/Cloud/en-US>  
	![](images/01b.png)


## <a name="postman"></a> Install Chrome Postman application
For the workshop exercises you need to install the **Postman** application for Chrome. It will allow you to send REST requests to backend systems. Please pay attention that, this kind of application has been deprecated and removed from the Chrome web store, because it has been converted to a stand-alone application. However, for the scope of these exercises you will need to install it as a Chrome app. You can open the following link to install it:

<https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop>  
	![](images/25.png)


## <a name="postman-interceptor"></a> Install Chrome Postman Interceptor extension
Another required tool is the Postman Interceptor extension for Chrome. This can be found on the Chrome Web Store.

1. Navigate to <https://chrome.google.com/webstore/search/postman%20interceptor> and select the **Postman Interceptor** tool  
	![](images/26.png)

1. Click **Add to Chrome**  
	![](images/27.png)


## <a name="install-python"></a>Install Python

1.	Download and install Python from this link <https://www.python.org>  NB: this is not necessary for Mac users as Python should already be installed.
	![](images/30.png)

1.	Select downloads and download the windows installer file.
	![](images/31.png)

1.	Double click on the downloaded file. Be sure to check the **Add Python to PATH** option before commencing the installation.
	![](images/32.png)


## <a name="install-openssl"></a>Install OpenSSL

1.	Download and install OpenSSL from this link <http://gnuwin32.sourceforge.net/packages/openssl.htm>  NB: this is not necessary for Mac users as OpenSSL should already be installed.
	![](images/33.png)

1.	Download the **Complete package, except sources** then double click on the downloaded file.
	![](images/34.png)

1.	Note which folder OpenSSL will be installed into.
	![](images/35.png)

1.	Open **Advanced System Settings** for Windows
	![](images/36.png)

1.	Click on the **Environment Variables...** button
	![](images/37.png)

1.	Edit **PATH** in the System Variables area.
	![](images/38.png)

1.	Add a new value that corresponds to where OpenSSL has been installed (be sure to include \bin at the end).
	![](images/39.png)

1.  Save all changes.

## Summary
You have successfully completed the prerequisites installation.
