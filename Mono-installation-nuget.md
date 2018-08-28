# Step to install C# Library using Mono-Develop IDE

This library will help you to speed up the integration with Pepipost API v2 

2.5.0 version provides full access to the functionality of web API v2 for Sending emails

The goal is to simplify the complexity of integration and make the library Community Driven. We require your help to make sure the libraries are built in proper order.
we would want you to create issues and pull requests or simply upvote or comment on existing issues or pull requests.

For any update of this library check Releases.

## Prerequisites

   * [dotnet SDK](https://www.microsoft.com/net/download/dotnet-core/2.0) (> 2.0)
   * [mono devel](https://www.mono-project.com/download/stable/)
   * [Mono-develop IDE](https://www.monodevelop.com/download/)
   * [NETStandard.Library](https://www.nuget.org/packages/NETStandard.Library/)(>= 1.6.1)
   * [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json/)(>= 11.0.2)
   * [Pepipost](https://www.nuget.org/packages/Pepipost/)
   * A free account on [Pepipost](https://app.pepipost.com/index.php/signup/registeruser). If you don't have a one, click here to sign-up and get 30,000 emails free every month.
 
## How to build

   1. Start mono-develop IDE 
      
      ![Monol1](http://app1.falconide.com/integration_imgs/csharp-mono/l1.png)
   
   2. Select **File -> New Solution** Or Simply **Ctrl+shift+N**
   
      Template for new project prompt will appear **App -> console application -> Next**
      
      ![monol2](http://app1.falconide.com/integration_imgs/csharp-mono/l2.png)
      
   3. Give name to your Project 
   
      ```testConsole```
      
      Once you have named your project simply click create
      
      ![monol3](http://app1.falconide.com/integration_imgs/csharp-mono/l3.png)
      
   4. After Project is successfully created 
   
      ![monol4](http://app1.falconide.com/integration_imgs/csharp-mono/l4.png)

   5. Let's add Nuget package dependencies as described earlier
   
      ![mono15](http://app1.falconide.com/integration_imgs/csharp-mono/l5.png)
      
      **Newtonsoft.Json**
      
      ![monol6](http://app1.falconide.com/integration_imgs/csharp-mono/l6.png)
      
      Select **official C# library Pepipost**
      
      ![monol7](https://app1.falconide.com/integration_imgs/csharp-mono/l7.png)
     
   6. Once all the packages are installed successfully 
   
      just copy and paste the [simpleUsage.md]() in your program.cs file present in your project.
      
      build the project shown below OR by clicking **F8**
      
      ![monol8](http://app1.falconide.com/integration_imgs/csharp-mono/l8.png)
      
   7. Grab your **Api_key** and verified **Sending Domain**
   
      * apikey will be available under Login to Pepipost -> Settings -> Integration
      * Sending Domain will be available under Login to Pepiost -> Settings -> Sending Domains
      
   8. Change apikey and Sending Domain in script 
   
      ```string apiKey = "XXXXX-your-api-key-XXXX" ``` (near by line no 25 if your have copy the simpleUsage.md)
           
      ```body_personalizations_0.Recipient = "your recipient emailid here"``` (near by line no 31)
     
      ```body.From.FromEmail = "info@ your-verified-domain"``` (near by line no 37)
     
   9. Building Project to Send Email
   
      Run the project Press **ctrl + F5**
      
      If your apikey and sending domain is proper response message will be success 
      
      ![monol9](http://app1.falconide.com/integration_imgs/csharp-mono/l9.png)
      
      If there is some problem related with config Error message will be Shown
      
      ![mono10](http://app1.falconide.com/integration_imgs/csharp-mono/l10.png)
     
   
      
      

      
      
