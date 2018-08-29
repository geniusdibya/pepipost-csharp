# Steps to install C# SDK with Mono-Develop IDE

  This SDK will help you in integrating Pepipost Web API v2

  2.5.0 version provides full access to the functionality of web API v2 for Sending emails

  The goal is to simplify the complexity of integration and make the library Community Driven. 
  We require your help to make sure the libraries are built Properly.
  
## Prerequisites
    
   * [dotnet SDK](https://www.microsoft.com/net/download/dotnet-core/2.0) (> 2.0)
   * [mono devel](https://www.mono-project.com/download/stable/)
   * [Mono-develop IDE](https://www.monodevelop.com/download/)
   * [NETStandard.Library](https://www.nuget.org/packages/NETStandard.Library/)(>= 1.6.1)
   * [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/)
   * A free account on [Pepipost](https://app.pepipost.com/index.php/signup/registeruser).If you don't have a one, click here to sign-up and get 30,000 emails free every month.

## How to Build

   1. Download [Pepipost SDK](https://github.com/pepipost/pepipost-sdk-csharp/archive/master.zip)
   
      Unzip the SDK on any Location of your choice (we will unzipped in directory named testSDK)
            
      OR ```git clone https://github.com/pepipost/pepipost-sdk-csharp.git```
      
      ![mygit](http://app1.falconide.com/integration_imgs/csharp-mono/1.png)
      
   2. Start Mono-Develop IDE
   
      Click **open**
      
      ![monoide](http://app1.falconide.com/integration_imgs/csharp-mono/2.png)
      
   3. Select **Pepipost.sln** from unzipped folder 
   
      **Open** the Solution once you have selected the sln file 
   
      ![mono](http://app1.falconide.com/integration_imgs/csharp-mono/3.png)
      
   4. Once you have Opened the Solution the few files will appear with respective SDK
   
      Add new project to the main directory as Shown below
      
      ![monoaddpro](http://app1.falconide.com/integration_imgs/csharp-mono/4.png)
      
   5. Choose Template for new project will be prompted
   
      Select **App -> Console Application -> next**
      
      ![appconsole](http://app1.falconide.com/integration_imgs/csharp-mono/5.png)
      
   6. Configure New project
   
      Give an Desired name to your project (testConsole recommended)
      
      ![makeconsole](http://app1.falconide.com/integration_imgs/csharp-mono/6.png)
      
   7. Resolving Dependencies
   
      a. Adding Reference 
      
      ![dep1](http://app1.falconide.com/integration_imgs/csharp-mono/7.png)
      
      Select **Edit Reference**
        
      ![dep2](http://app1.falconide.com/integration_imgs/csharp-mono/8.png)
        
      Select **Pepipost -> OK**
         
      ![dep3](http://app1.falconide.com/integration_imgs/csharp-mono/9.png)
         
       b. Adding packages
       
       ![dep4](http://app1.falconide.com/integration_imgs/csharp-mono/10.png)
          
       search **NewtonSoft.json -> Add packages**
          
       ![dep5](http://app1.falconide.com/integration_imgs/csharp-mono/11.png)
          
   8. Once all the packages are installed successfully 
   
      just copy and paste the [simpleUsage.md](https://github.com/hellovikram/pepipost-csharp/blob/master/simpleUsage.md) in your program.cs file present in your project.
      
      build the project shown below OR by clicking **F8**
      
      ![monol8](http://app1.falconide.com/integration_imgs/csharp-mono/l8.png)
        
   9.  Grab your **Api_key** and verified **Sending Domain**
   
       * apikey will be available under Login to Pepipost -> Settings -> Integration
       * Sending Domain will be available under Login to Pepiost -> Settings -> Sending Domains
      
   10. Change apikey and Sending Domain in script 
   
       ```string apiKey = "XXXXX-your-api-key-XXXX" ``` (near by line no 25 if your have copy the simpleUsage.md)
           
       ```body_personalizations_0.Recipient = "your recipient emailid here"``` (near by line no 31)
     
       ```body.From.FromEmail = "info@ your-verified-domain"``` (near by line no 37)
     
   11.  Building Project to Send Email
   
        Run the project Press **ctrl + F5**
      
        If your apikey and sending domain is proper response message will be success 
      
        ![monol9](http://app1.falconide.com/integration_imgs/csharp-mono/l9.png)
      
        If there is some problem related with config Error message will be Shown
      
        ![mono10](http://app1.falconide.com/integration_imgs/csharp-mono/l10.png)

      
