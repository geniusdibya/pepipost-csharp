# Step to use Pepipost C# .Net library with Visual Studio 2017

This SDK will help you in integrating Pepipost Web API v2

2.5.0 version provides full access to the functionality of web API v2 for Sending emails

The goal is to simplify the complexity of integration and make the library Community Driven. We require your help to make sure the libraries are built Properly.

## Prerequisites

   * [Microsoft visual Studio 2017](https://visualstudio.microsoft.com/downloads/)
   * [NETStandard.Library](https://www.nuget.org/packages/NETStandard.Library/)(>= 1.6.1)
   * [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/)
   * A free account on [Pepipost](https://app.pepipost.com/index.php/signup/registeruser).If you don't have a one, click here to sign-up and get 30,000 emails free every month.


## How to Build

 1. Download [Pepipost SDK](https://github.com/pepipost/pepipost-sdk-csharp/archive/master.zip)
   
    Unzip the SDK on any Location of your choice (we will unzipped in directory named testSDK)
            
    OR ```git clone https://github.com/pepipost/pepipost-sdk-csharp.git```
      
 2. For starting a new project, right click on the current solution from the *solution explorer* 
 
    choose  ``` Add -> New Project ```.

    ![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)

 3. Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name 
 
    click ``` OK ```.

    ![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)

 4. Set as startup project

    The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project.
    
    To do this, right-click on the  ``` TestConsoleProject ```
    
    choose  ``` Set as StartUp Project ``` form the context menu.

    ![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)

 5. Add reference of the library project

    In order to use the Pepipost C# library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. 
    
    First, right click on the ``` References ``` node in the *solution explorer*
    
    click ``` Add Reference... ```.

    ![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)

    Next, a window will be displayed where we must set the ``` checkbox ``` on ``` PepipostAPI.Standard ``` 
    
    click ``` OK ```. 
    
    By doing this, we have added a reference of the ```PepipostAPI.Standard``` project into the new ``` TestConsoleProject ```.

    ![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)
 
 6. Once all the packages are installed and **TestConsoleProject** is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method.
 
   This is the entry point for the execution of the entire solution.

   Here, you can add [simpleUsage.md code](https://github.com/hellovikram/pepipost-csharp/blob/master/simpleUsage.md) 

  ![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=Pepipost%20API-CSharp&workspaceName=PepipostAPI&projectName=PepipostAPI.Standard)

 7. Grab your **Api_key** and verified **Sending Domain**
   
       * apikey will be available under Login to Pepipost -> Settings -> Integration
       * Sending Domain will be available under Login to Pepiost -> Settings -> Sending Domains
      
 8. Change apikey and Sending Domain in script 
   
    ```string apiKey = "XXXXX-your-api-key-XXXX" ``` (near by line no 25 if your have copy the simpleUsage.md)
           
    ```body_personalizations_0.Recipient = "your recipient emailid here"``` (near by line no 31)
     
    ```body.From.FromEmail = "info@ your-verified-domain"``` (near by line no 37)
     
  9.  Building Project to Send Email
      
      Press **ctrl + shift + F5** 
      
      If your apikey and sending domain is proper response message will be success 
  
      ![s7](http://app1.falconide.com/integration_imgs/csharp-vs/screen-15.png)
