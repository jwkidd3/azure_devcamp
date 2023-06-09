# Developer Environment (Java)

## Overview
In this lab, you will set up an Office365 trial subscription, an Azure trial subscription, configure your Azure subscription for the DevCamp, and provision a virtual machine in the subscription to use for development of further labs.

## Objectives
In this hands-on lab, you will set up an Office365 developer subscription, and Azure trial subscription, and an Azure-based virtual machine for the development environment for subsequent labs in the DevCamp.  To expedite the process, we've prepared a Windows image that you will copy into your own environment, start the virtual machine and connect to it.  You will then configure the components for Azure development.
* Set up an Office365 trial subscription.
* Set up an Azure trial subscription.
* Configure your Azure subscription for DevCamp.
* Create an Azure Virtual Machine for remote development.
* Connect to the Azure Virtual Machine and configure it for development.
* Review the features of the Azure Portal.

## Prerequisites

You will need a cell phone and credit card for identity verification.

The credit card ***will not*** be charged unless you remove the spending limit on the subscription you will create.

## Exercises
This hands-on-lab has the following exercises:
* [Exercise 1: Set up Office 365 trial subscription](#ex1)
* [Exercise 2: Set up Azure trial subscription](#ex2)
* [Exercise 3: Start your VSTS trial subscription](#ex3)
* [Exercise 4: Configure your Azure subscription for DevCamp](#ex4)
* [Exercise 5: Use an Azure Virtual Machine for remote development](#ex5)
* [Exercise 6: Deploy Shared API application](#ex6)
* [Exercise 7: Azure Portal walkthrough](#ex7)
* [Exercise 8: View the resources you created](#ex8)

---
## Exercise 1: Set up Office 365 trial subscription<a name="ex1"></a>

> If you already have an Office 365 subscription, please use an alternate browser or use private mode. This will help avoid any issues with conflicting accounts.

1. In your browser, go to [https://products.office.com/en-us/business/office-365-enterprise-e3-business-software](https://products.office.com/en-us/business/office-365-enterprise-e3-business-software) 
and click the link that says `Free Trial`. 

    ![image](./media/2017-03-14_08_28_44.png)

    This will navigate you to this page:

    ![image](./media/2017-03-14_08_38_22.png)

1. Enter the information requested, and click **Next** which will take you to the following page:
    
    ![image](./media/2016-10-14_19-06-31.gif)

1. Choose a `user id` and a `tenant name` for your trial.  In this case I chose `devcampross`, but you can choose anything you'd like, as long as it is unique.  You'll also have to choose a password, and click `Create my account`.
    
1. Next you will see this page, which asks for phone verification:

    ![image](./media/2016-10-14_19-07-30.gif)

1. After this process is complete, your O365 trial will be set up, and you'll see this page:
    
    ![image](./media/2016-10-18_12-39-13.gif)

    > Make note of your user id, which will be used to sign onto the Azure portal later.

1. Click `You're ready to go`, which will take you to the following screen:

    ![image](./media/2017-03-14_08_49_17.png)

1. Click on the `Admin` app icon, which will open the Office365 admin center page in your browser. It will look like this:

    ![image](./media/2017-06-15_10_19_00.png)

     If you'd like to see the welcome tour click `Next`, or simply close the dialog box.   
    
Stay on this page until the next exercise.

---
## Exercise 2: Set up Azure trial subscription<a name="ex2"></a>

Next, we want to set up an Azure subscription, which can be accessed via the Azure Active Directory link.  On the bottom, left-hand side of the screen, click `Admin centers`, and then click `Azure AD`. 

![image](./media/2017-06-15_10_23_00.png)    

This will open up a new browser tab showing this page:

![image](./media/2017-06-15_10_27_00.png)

Click the hyperlink **Azure Subscription** to begin the Azure Trial signup process.

> BEGIN Steps for Azure Pass redemption - Follow this step if you are using an Azure Pass. If you are not using an Azure Pass, please skip ahead to **END Steps for Azure Pass redemption**

1. Navigate to [http://www.microsoftazurepass.com/]().

    ![image](./media/2017-06-15_10_39_00.png)

1. Enter the code that is provided by your facilitator into the text box, then click `Submit`.

> END Steps for Azure Pass redemption

1. After clicking on the `Azure Subscription` link you will be taken to the page for creating a new trial subscription:

    ![image](./media/2016-10-18_12-48-52.gif)

1. Enter the requested information and click `Next`.

1. Enter the information about you, and verify your identity by phone.  

1. Next, you will need to verify via credit card.  Your credit card ***will not*** be charged unless you remove the spending cap from your subscription. Supported cards must be either a Credit or Debit card, from vendors Visa, Mastercard, American Express, or Discover.
    
    ![image](./media/2016-10-14_21-42-46.gif)

1. Finally after the verification process, you'll have to agree to the terms of the trial subscription and click the `Sign up` button.

    ![image](./media/2017-03-14_09_12_14.png)

1. It will take a few moments to set up your Azure subscription.  

    ![image](./media/2016-10-14_21-45-32.gif)

1. When the subscription set up process is complete, click on `Get started with your Azure subscription` button:

    ![image](./media/2017-03-14_09_15_01.png)

You should now be taken to the [Azure Portal](http://portal.azure.com) where you can explore your new Azure Trial Subscription.

![image](./media/2017-06-15_10_44_00.png)

---
## Exercise 3: Start your VSTS trial subscription<a name="ex3"></a>

In a future lab we will use [Visual Studio Team Services](https://www.visualstudio.com/team-services/), or "VSTS" for short. In this exercise we will enable a free trial subscription.

1. In your browser, go to [http://www.visualstudio.com/team-services](http://www.visualstudio.com/team-services) and click on `Sign in` in the upper right corner.  

    ![image](./media/2017-03-14_09_21_21.png)

    Complete the sign in process if needed, and you should be taken to a screen that looks like this:

    ![image](./media/2017-03-14_09_25_15.png)

    Add your name and email address (if not already populated) and click `Continue`.

1. On the My Benefits screen, click `Use your benefits` under the heading **Visual Studio Dev Essentials**.

    ![image](./media/2016-10-18_17-30-18.gif)

1. Click the `Accept` button to access your Visual Studio Dev Essentials benefits

    ![image](./media/2016-10-18_17-42-01.gif)

    Click `Confirm` in the modal dialogue.

    ![image](./media/2017-06-15_10_47_00.png)

You have now activated a Visual Studio Team Services Trial Subscription, which will be used in a future lab.

---
## Exercise 4: Configure your Azure subscription for DevCamp<a name="ex4"></a>

1. We have created an Azure Resource Group template that will configure the resources you need in Azure for the DevCamp.  To deploy these resources in your Azure subscription, `control + click` on the blue ***Deploy to Azure*** button below (on a MAC, use `Apple Key + click`):

    :point_right:    <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzureCAT-GSI%2FDevCamp%2Fmaster%2FShared%2FARMTemplate%2FAzureDeploy.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>    :point_left:

1. You should see a new tab open in your browser and open the Azure portal, with a blade that looks like this:

    ![image](./media/2017-06-15_10_51_00.png)

1.  Name your resource group `DevCamp`, and choose a location for your deployment. 

    > Please **do not** choose the region West India for your deployment. It is missing a resource that is needed for the labs

1. Check the box that indicates you agree to the terms and conditions, and click the `Purchase` button.

    The Resource Group template will start deploying, and the portal may pin a tile to the dashboard showing the status:

    ![image](./media/2017-06-15_10_56_00.png)

    It will also be visible in the **Notifications** dropdown:

    ![image](./media/2017-03-14_09_43_44.png)

1. This will take approximately 20-30 minutes to complete. Please do not continue on until the template has completed.

    In a later session, we will take a look at Azure Resource Group templates, and how to manage your infrastructure the same way     you manage your code.  As a short introduction, a template is a JSON file that contains definitions for the resources you want in your    resource group.  When you apply the resource group template, Azure will apply the template to your Azure resource group, and create     the resources you have specified in the template.  This makes it easy to maintain the infrastructure definition in the JSON text file.
    
    In the resource group template we have created for DevCamp, there are several types of resources including Web Apps and a Virtual Machine. The     complete list of resources deployed is detailed in Exercise 8 of this Hands-On-Lab.  Resource Group Templates are usually fairly quick to    apply - the reason this one takes so long is that we are creating a Windows Virtual machine and installing all the tools you will    need for the DevCamp including Visual Studio, the Java development kit, and other software resources.

1. You will know when the Resource Group finishes provisioning either by the Notification dropdown, or by navigation on the lefthand bar to **Resource Groups** -> **DevCamp** and check the "Deployments" status for **Succeeded**.

    ![image](./media/2017-06-15_11_41_00.png)

    Once the Resource Group creation is done, you can visit the resource group by clicking `Resource Groups` on the left navigation pane:

    ![image](./media/2016-10-18_13-36-29.gif) 

1. Then click on your Resource group to open it:

    ![image](./media/2016-10-18_13-39-10.gif)

---
## Exercise 5: Use an Azure Virtual Machine for remote development<a name="ex5"></a>

1. The Azure resource group template will have created a virtual machine that can be used for remote development on Windows. Exercise 5 describes the configuration for the Windows virtual machine, which would be appropriate for any of the languages.

1. In the DevCamp resource group, select the DevCamp DevTest Lab.

    ![image](./media/image-007.gif)

1. Find the Windows virtual machine in your DevTest lab. The name will start with the prefix `windev`:

    ![image](./media/2017-06-15_11_47_00.png)

1. Select the machine name and open the virtual machine blade  then click `Connect` to connect to the machine using Remote Desktop:

    ![image](./media/2017-06-15_11_52_00.png)

    This will download a remote desktop connection file, and when you open it, remote desktop on your local machine will attempt to attach to your virtual machine.

    ![image](./media/2017-06-15_11_57_30.png)

    When the windows security dialog pops up, the user name `l-admin` should be pre-selected. If not click on the `More choices` link, then choose `Use a different account`.
    
    ![image](./media/2017-06-15_12_02_00.png)

1. Use the following credentials to log on to the machine:
    
    > User Name = `\l-admin`
    >
    > Password = `Devc@mp2016!` 
 
    ![image](./media/2017-06-15_11_57_00.png)

    > It would be wise to change the password in the virtual machine.

1. When remote desktop is connected, you will see server manager initially.  We will want to turn of IE enhanced security, to make accessing the web within the virtual machine easier.  First click `local server`.

    ![image](./media/2016-10-18_16-46-33.gif)

1. Then click the `On` next to **IE Enhanced Security Configuration**.

    ![image](./media/2016-10-18_16-50-50.gif)

    A dialog box pops up - choose to turn enhanced security off for administrators.

1. We are going to use git to clone the DevCamp github repository to this development machine. Click on the Start menu, and type `cmd`.

    > NOTE: On some high resolution monitors (HIGH DPI), you will notice that the icons and command line windows appear small. If this is an issue, you can download [Remote Desktop Connection Manager 2.7](https://www.microsoft.com/en-us/download/details.aspx?id=44989).

1. Change directory to the root using `cd c:\ `.

1. Type `git clone https://github.com/AzureCAT-GSI/DevCamp.git`:

    ![image](./media/2016-10-18_17-03-51.gif)

    All of the content for this DevCamp will now be located in `c:\DevCamp`.

1. Inside your development Virtual Machine, open a *NEW* terminal window and execute this command to verify that the node version is v6 or greater:

    ```CMD
    node -v
    ```

1. If the Node version on your machine is less than v6, we will need to update the version. In a browser window open a browser window and go to `http://nodejs.org`, and click on the `Other Downloads` link under the current version LTS:

    ![image](./media/2017-06-19_08_48_00.png)

    In the next page, click on `32-bit` next to `Windows Installer (.msi)`, download the MSI and run the installation.

    ![image](./media/2017-06-19_08_51_00.png)

    > Please do not skip this step, because we will need node.js to install the Azure cross platform command line interface in the next step.

1. We will use the [Microsoft Azure Cross Platform Command Line](https://github.com/Azure/azure-xplat-cli) to interact with our subscription.

    > *There is a new python-based command line interface in preview - we are not going to use that one. Please follow these instructions to install the node-based command line interface.* 
    
    Then install the Microsoft Azure Cross Platform Command Line by executing:

    ```CMD
    npm install azure-cli -g
    ```

1. If you are not developing in Java for the DevCamp, you can skip this step. We have already installed the Java JDK, but we will install gradle and Eclipse. We will be using the gradle build manager - to install that using the [chocolatey package manager](http://www.chocolatey.org), open a command window as administrator and type:

    ```CMD
    choco install -y gradle
    ```

    Also install maven with:

    ```CMD
    choco install -y maven
    ```

    Go to the root directory using `cd \ `, and perform these commands in sequence:

    ```CMD
    refreshenv
    git clone https://github.com/swagger-api/swagger-codegen.git
    cd swagger-codegen
    mvn clean package
    ```

    Also Eclipse Mars is installed in `C:\Program Files\Eclipse Foundation\4.5.1\eclipse`.
    
    If you would like to download a newer version (e.g. [Neon](https://www.eclipse.org/downloads/packages/eclipse-ide-java-ee-developers/neon3) - be careful to not upgrade to versions newer than Neon since they no longer support gradle), Eclipse is available here:

    [http://www.eclipse.org/downloads/]()

    and Spring Tool Suite is available here:

    [http://spring.io/tools/sts]()

    For example, after downloading the Eclipse install, run it and you'll get this screen:

    ![image](./media/2017-06-19_09_10_00.png)

    choose `Eclipse IDE for Java EE developers`.  In the next screen, leave the defaults and choose `INSTALL`:

    ![image](./media/2017-06-19_09_11_00.png)

    When that is done, click `LAUNCH` to start the IDE and choose a directory for your workspace. You will end up with the initial Eclipse screen:

    ![image](./media/2016-10-19_10-53-32.gif)

    Click `Help` in the menu bar, and choose `Install New Software...`:

    ![image](./media/2016-10-19_10-55-30.gif)

    In the window that pops up, choose `All Available Sites` for the `Work with` dropdown, type `gradle` in the search box, and when the search is complete (which sometimes takes a minute or two), choose `Buildshop: Eclipse Plug-ins for Gradle`:

    ![image](./media/2017-06-19_09_22_00.png)
    
    Click through the dialog, install the package and let Eclipse restart.
    
    Again select `Help` -> `Install New Software...`, and click the `Add..` button next to the `Work with` dropdown.  In the `Add Repository` dialog box, give the repository a name, and type `http://dl.microsoft.com/eclipse` for the Location, and click `OK`:

    ![image](./media/2016-10-19_11-26-29.gif)

    This will load a list of available packages. Choose the `Azure Toolkit for Java` package and the `Team Explorer Everywhere` package in the list, and complete the package installation as before:

    ![image](./media/2017-06-19_09_29_00.png)

    Also, install the `Spring Tool Suite (STS) for Eclipse` package by using the menu item `Help` -> `Eclipse Marketplace...`, type `spring` in the `Find:` box and choose `Go`. In the list of packages, scroll down to `Spring Tool Suite (STS) for Eclipse X.X.X.RELEASE` and click `Install`.

    ![image](./media/2017-06-19_09_34_00.png)

---
## Exercise 6: Deploy shared API application<a name="ex6"></a>

1. The API application has been prepared for you to be available as a communication partner during different exercises and just needs to be deployed once. It will be first used in the second hands on lab.

1. Open a browser and navigate to [https://portal.azure.com](https://portal.azure.com). Locate the app service named `incidentapi...` in the resource group blade:
    
    ![image](./media/2017-06-15_13_05_00.png)

1. Click on the app service, which will bring up the app service blade. Click on `Browse` at the top:

    ![image](./media/2017-06-15_13_08_00.png)

    A new browser tab will open.

    > If the page looks like the image displayed below, this means the API was automatically deployed from GitHub, and you can skip the rest of this exercise.
    
    ![image](./media/2016-11-14_12-10-59.gif)

    > If the page looks like the image below, continue with this exercise
         
    ![image](./media/2016-11-14_12-03-50.gif)

1. In the Azure portal, select the API Application (noted with the ![image](./media/image-024.gif) icon).
    
    ![image](./media/image-019.gif)

1. On the details blade select `Deployment options`.
 
    ![image](./media/image-020.gif)

1. If the app deployment is connected, click `Disconnect` on the menu bar.
 
    ![image](./media/2017-06-15_15_47_00.png)

1. Then select `Setup` on the menu bar.
 
    ![image](./media/image-022.gif)

1. Select `External repository`. 

1. Paste the following in the Repository URL field `https://github.com/AzureCAT-GSI/DevCamp.git`.

    ![image](./media/image-023.gif)

1. Select `OK`.

---
## Exercise 7: Azure Portal walkthrough<a name="ex7"></a>

1. On your local machine or the virtual machine in Azure, open a browser window and go to the main Azure portal page, [http://portal.azure.com](https://portal.azure.com).  Log in with the credentials you supplied in the subscription signup exercise.  You should see the Azure portal, similar to this:

    ![image](./media/2017-06-15_16_21_00.png)

    There is a lot to notice on this screen.  At the upper left corner, the icon under the `Microsoft Azure` banner allows you to shrink and expand the left bar:

    ![image](./media/2016-10-19_15-15-50.gif)

    Under that, clicking on the `+ New` item will allow you to create new deployments, virtual machines, databases, etc:

    ![image](./media/2017-06-15_16_29_00.png)
    
1. On the left you will see a list of the Azure services that you can use on the left hand side.  Notice that this list will scroll up and down to reveal more services, and finally an item that says `More Services >`:

    ![image](./media/2017-06-15_16_25_00.png)

    You can click on any of these and see what items are deployed, and easily create new deployments.

1. At the top of the window you have a search box where you can search for any resources:

    ![image](./media/2016-10-19_15-22-14.gif)

1. The bell icon is for notifications, and in this screenshot, it indicates that there are two notifications pending: 

    ![image](./media/2016-10-19_15-22-14a.gif)

    Clicking on the bell will show you the notifications:

    ![image](./media/2017-06-15_16_37_00.png)

    If you click on one of the notifications, you can go to the details blade that matches the content of the notification, e.g. the details blade of the starting virtual machine.

1. The `>_` icon opens the Azure Cloud Shell which gives you authenticated shell access to Azure within the browser. It opens at the bottom of the window.
 
    ![image](./media/2017-06-15_16_46_00.png)

1. The gear at the top of the screen lets you set the color palate for the portal, whether or not there will be animations, and other options for the portal itself:

    ![image](./media/2016-10-19_15-22-14b.gif)

1. The "smiley face" button allows you to send feedback to Microsoft:

    ![image](./media/2016-10-19_15-22-14c.gif)

    Clicking on the icon will give you a form to let us know about your experience:

    ![image](./media/2017-06-15_16_48_00.png)

1. The Question icon will give you the ability to enter a support case, manage support requests, or get further information on Azure.
    
    ![image](./media/2016-10-19_15-22-14d.gif)

1. Your login name and company name on the upper left hand corner has two functions: 

    ![image](./media/2016-10-19_15-22-14e.gif)
    
    If you hover the mouse over your name, you'll get information about your login, the directory and subscription:

    ![image](./media/2016-10-19_16-25-54.gif)

    If you click on your name, you can sign out, change your password, view your permissions, and view your bill:

    ![image](./media/2017-06-15_16_51_00.png)

1. Next we will look at the resource group we set up with the template.  Click on `Resource Groups` on the left hand side:

    ![image](./media/2016-10-19_16-30-19.gif)

1. Click on the resource group that you created:

    ![image](./media/2017-06-16_08_38_00.png)

    A new blade will open with the overview of all of the contents of the resource group listed:

    ![image](./media/2017-06-16_08_42_00.png)

    You can click on any of the items on the left hand side which will view or manipulate settings for the resource group as a whole.  If you click on any of the individual resources in the center, you will get more information on that resource.

1. Azure automatically logs changes to resource group and who made those changes.  Clicking `Activity log` on the left of the blade will allow you to query the log, and clicking on any logged items will give you additional information on that entry:

    ![image](./media/2017-06-16_08_51_00.png)

1. Clicking on `Automation script` will allow you to view, edit or download the resource group template that would create this resource group.

    ![image](./media/2017-06-16_08_53_00.png)

1. The Windows VM is managed by an [Azure DevTest lab](https://azure.microsoft.com/en-us/services/devtest-lab/) named `DevCamp` which handles the startup and shutdown of the machine. To change the start up schedule, click on the DevTest Lab icon and select `Configuration and policies` under the `Settings` headline. 

    ![image](./media/2017-06-16_09_04_00.png)

1. Select `Auto-shutdown`.

    ![image](./media/2017-06-16_09_06_00.png)

1. Modify the Auto-shutdown schedule based on your time zone.

    ![image](./media/2017-06-16_09_08_00.png)

1. The machine does not automatically turn on. To enable this, in the Policy Settings blade, select `Auto-Start`.

    ![image](./media/2017-06-16_09_14_00.png)

1. Change the schedule based on your time zone.

    ![image](./media/2017-06-16_09_14_30.png)

> It is particularly useful to create resources in the Azure portal, then save or edit the resource group template.
> Resource group templates will be explained further in a later lab.

---
## Exercise 8: View the resources you created<a name="ex8"></a>

Going back to the list of resources in the resource group `DevCamp`, we'll go through the list of each resource, with a description.  Feel free to click on the resource and view its detail blade.

![image](./media/2017-06-16_09_18_00.png)

Also, our resource group template has added a random string to the end of many of the resources.  In this description, we have replaced that string with `...`:

* `adevcamp...` - Storage account for storing artifacts for the DevTest labs.

* `DevCamp` - This is the DevTest lab that is used to manage the VM images and artifacts.

* `DevCamp...` - This is the Azure Key Vault that is used to manage secure credentials.

* `DevCampVnet` - This is an Azure Virtual Network, which will allow components of the resource group to communicate as if they were on the same physical network.

* `dotnetapp...` - App service for running the .NET application when deployed to the cloud.  If you are not using .NET in the labs, you can safely delete this.

* `incidentapi...` - App service for running the API service that provides a REST API to the web applications.

* `incidentappplan...` - App Service Plan, which defines how the app services in the resource group will be configured.

* `incidentblobstg...` - Storage account for storing the uploaded images and the Azure Queue, from the modern-cloud-apps hands on lab.

* `incidentcache...` - This is the Redis cache that we use from the application to make data access faster.  The modern-cloud-apps hands on lab adds support to the application to be able to leverage the cache.

* `incidentdb...` - This is the documentDB database that will hold the JSON incident documents stored by the application.

* `incidentdiagstg...` - Storage account for storing diagnostics from the services in the resource group.

* `javaapp...` - App service for running the Java application when deployed to the cloud.  If you are not using Java in the labs, you can safely delete this.

* `nodejsapp...` - App service for running the Node.js application when deployed to the cloud.  If you are not using Node.js in the labs, you can safely delete this.

In the second resource group `DevCamp-WinDev-...`, additional resources were created.

   ![image](./media/2017-06-16_09_55_00.png)

They are all called `WinDev-...` but are of different types:

* `Public IP address` - This is a public IP that will allow the Windows development virtual machine to communicate with the Internet (e.g. via Remote Desktop).  If you delete the Windows virtual machine, you can safely delete this.

* `Virtual machine` - This is the Windows server virtual machine that we are using as a development machine for these hands-on-labs. You can delete this machine after the developer-environment lab if you are using an on-premises/local machine for development. 

* `Network interface` - This is a public network interface that will allow the Windows development virtual machine to communicate on the network.  If you delete the Windows virtual machine, you can safely delete this.

* `Disk` - Storage account for storing for VHDs for the machines DevTest labs.

---
## Clean Up

**&#x1F53A; Please refer back to this section after the DevCamp concludes! This is instructional only! Do NOT clean up until the DevCamp is done! &#x1F53A;**

To clean up a Resource Group, we typically simply delete the Resource Group. However, since we are using an Azure DevTest Lab to manage our Virtual Machine, we have an additional step.

Azure DevTest Labs create a series of [Resource Locks](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-lock-resources) that prevent accidental deletion of resources. Locks allow us to safeguard against accidental deletion of critical resources, and to delete the Resource Group we first need to delete the locks.

Open your DevCamp Resource Group, and in the navigation pane select **Locks**. You should see the 3 locks created by the DevTest Lab. To delete, select the three dots to the right of the Notes column, and select **Delete**.

![image](./media/2017-06-16_10_13_00.png)

After all 3 locks have been deleted you are able to delete the resource group. Navigate to the **Overview** tab and select **Delete**. The Resource Group will take several minutes to remove, but when finished all resources will no longer accrue charges in your subscription.

![image](./media/2017-06-16_10_25_00.png)

---
## Summary

In this hands-on lab, you learned how to:
* Set up an Office365 developer subscription.
* Set up an Azure trial subscription allowing you to complete this course free of charge.
* Configure your Azure subscription for DevCamp.
* Create an Azure Virtual Machine for development where you can carry out the following hands on labs.
* Connect to the Azure Virtual Machine and configure it for development.
* Use the Azure portal to view the resources that you created giving you a first overview of the management of Azure resources.

After completing this module, you can continue on to Module 2: Building modern cloud apps.

### View Module 2 instructions for [Java](../02-modern-cloud-apps).

---
Copyright 2016 Microsoft Corporation. All rights reserved. Except where otherwise noted, these materials are licensed under the terms of the MIT License. You may use them according to the license as is most appropriate for your project. The terms of this license can be found at https://opensource.org/licenses/MIT.