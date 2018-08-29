![pepipostlogo](https://pepipost.com/assets/img/pepipost-footLogo.png)

[![NuGet](https://img.shields.io/nuget/v/Pepipost.svg)](https://www.nuget.org/packages/Pepipost)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE.txt)
[![Twitter Follow](https://img.shields.io/twitter/follow/pepi_post.svg?style=social&label=Follow)](https://twitter.com/pepi_post)


# Official C# Code library for [Pepipost](http://www.pepipost.com/?utm_campaign=GitHubSDK&utm_medium=GithubSDK&utm_source=GithubSDK)

## Overview

  This library allows you to fasten up your integration with Pepipost web API v2
  
  2.5.0 version of this library provides full access of functionality with respect to send email using v2 API
  
  The goal is to simplify the complexity and minimize the requirements of integration for making the library Community Driven. To help us in building the right things in proper order we would request you to help us by sharing valuable comments, creating new [issues]() and [pull requests]()

  For any update of this library check [Releases]().

# Table of Content
  
* [Installation](#installation)
* [Quick Start](#quick-start)
* [Usage](#usage)
* [Announcements](#announcements)
* [Roadmap](#roadmap)
* [How to Contribute](#contribute)
* [Troubleshooting](#troubleshooting)
* [About](#about)
* [License](#license)

<a name="installation"></a>
# Installation

## Prerequisites

   * [Microsoft visual Studio 2017](https://visualstudio.microsoft.com/downloads/)
   * [NETStandard.Library](https://www.nuget.org/packages/NETStandard.Library/)(>= 1.6.1)
   * [Pepipost](https://www.nuget.org/packages/Pepipost/)
   * A free account on [Pepipost](https://app.pepipost.com/index.php/signup/registeruser). If you don't have a one, click here to sign-up and get 30,000 emails free every month.
   
## IDE Specific installation

  In order to use Pepipost C# library you can either directly download [Pepipost C# .NET library from our Git Repo]() OR if your have Nuget Package manager installed, you can search and download from the Package manager
  
  Pepipost C# .NET library is compatible with Windows Forms, Windows RT, Windows Phone 8, Silverlight 5, Xamarin iOS, Xamarin Android and Mono.
  
  We have demonstrated the installation with two IDEs which consists of Mono-Develop and Visual Studio 2017
  
  * Installation with Mono-Develop
  
    * [Using Nuget package manager](). 
  
    * [Using Github Repository]()
    
  * Installation with Microsoft Visual Studio
  
    * [using Nuget Package manager]()
    
    * [using Github Reposistory]()
    

# Quick Start

## How to Build

  1. Download File from [Github](https://github.com/pepipost/pepipost-sdk-csharp/archive/master.zip) unzipped file to your desired location.
  
  2. Start Visual Studio 2017
  
    ![]

## Initialization

### 

API client can be initialized as following.

```csharp

PepipostAPIClient client = new PepipostAPIClient();
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [EmailController](#email_controller)

## <a name="email_controller"></a>![Class: ](https://apidocs.io/img/class.png "PepipostAPI.Standard.Controllers.EmailController") EmailController

### Get singleton instance

The singleton instance of the ``` EmailController ``` class can be accessed from the API Client.

```csharp
EmailController email = client.Email;
```

### <a name="create_send_email"></a>![Method: ](https://apidocs.io/img/method.png "PepipostAPI.Standard.Controllers.EmailController.CreateSendEmail") CreateSendEmail

> *Tags:*  ``` Skips Authentication ``` 

> This Endpoint sends emails with the credentials passed.


```csharp
Task<Models.SendEmailResponse> CreateSendEmail(string apiKey = null, Models.EmailBody body = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| apiKey |  ``` Optional ```  | Generated header parameter. Example value ='5ce7096ed4bf2b39dfa932ff5fa84ed9ed8' |
| body |  ``` Optional ```  | The body passed will be json format. |


#### Example Usage

```csharp
string apiKey = "api_key";
var body = new Models.EmailBody();

Models.SendEmailResponse result = await email.CreateSendEmail(apiKey, body);

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 405 | Method not allowed |


[Back to List of Controllers](#list_of_controllers)



