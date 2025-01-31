# C# example

## Description

This repository contains a very simple .NET application that implements the Microsoft Graph SharePoint Pages API.

### Examples Provided

- GET all pages from a SharePoint site
- GET a specific page
- POST a new page
- PATCH an existing page
- DELETE a page
- POST to publish a page

## App Registration

To configure the sample, you'll need to register a new application in the Microsoft [Application Registration Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps).

Follow these steps to register a new application:

1. Sign in to the [Application Registration Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps) using either your personal or work or school account.

2. Choose **New registration**.

3. Enter an application name, and choose **Register**.

4. Next you'll see the overview page for your app. Copy and save the **Application Id** field. You will need it later to complete the configuration process.

5. Under **Certificates & secrets**, choose **New client secret** and add a quick description. A new secret will be displayed in the **Value** column. Copy this password. You will need it later to complete the configuration process and it will not be shown again.

6. Under **API permissions**, choose **Add a permission > Microsoft Graph**.

7. Under **Application Permissions**, add the permissions/scopes required for the sample. This sample requires **Sites.ReadWrite.All**. Grant admin consent to the application.

As the final step in configuring the script, modify the AccessToken.cs file in the root folder of your cloned repo.

```c#
static readonly string tenantId = "<enter your tenant Id here>";
static readonly string appId = "<enter your app Id here>";
static readonly string appSecret = "<enter your app secret here>";
```

Once changes are complete, save the file. After you've completed these steps and have received admin consent for your app, you'll be able to run the Main.cs sample as covered below.

### Notes:

- All code that interacts with the API is contained inside SitePagesController.cs

## Instructions

1) Clone this repository
2) Register an application using the steps above
3) Provide you application details in the AccessToken.cs file
4) Execute "dotnet run" to start the server

<img src="https://pnptelemetry.azurewebsites.net/sp-dev-solutions/solutions/PagesAPISolution/Csharp" />