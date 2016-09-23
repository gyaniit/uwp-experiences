# Backdrop (music app)

![Imgur](http://imgur.com/CPWPlHE.png)

Backdrop is a sample music application that lets a group of friends collaborate on the music selection process and share their experience and music choices. A device is first chosen to be the host device where the music will be played. Then anyone is able to add and vote on tracks on their own device. Each friend can see the current playlist in real time and the progress of the current track on their own device. Each can vote on different tracks to set the order in which they will be played as well as suggest other tracks to be played. 

The application has been written for the Universal Windows Platform (UWP) and tvOS by using Xamarin to share the majority of business logic, view models, playlist management, cloud and device communication. The UI, in turn, is written using the native controls and affordances of each platform. Using the shared project, additional platforms such as Android and iOS can easily be added.

Read the [full blog post](https://blogs.windows.com/buildingapps/2016/09/23/background-audio-and-cross-platform-development-with-xamarin-app-dev-on-xbox-series) or visit the [App Dev on Xbox landing page](http://aka.ms/xboxappdev) for more videos and blogs.

### [Get the latest build of the app here](https://1drv.ms/f/s!AjZLNGpIZBbgruphmcOvpZogOprcdQ)

# Setup

## Keys.cs
To run the app yourself, you will need to populate the Music.PCL/Keys.cs file for the following services:

### 1. Azure App Service

The backend for Backdrop runs as a free App Service on Azure. If you don't have an Azure account, you can create a free account [here](https://azure.microsoft.com/free/).
To publish the App Service to your Azure account, right click on the **music_appService** project in Visual Studio and click on **Publish**. Follow the steps to create a new App Service or publish the project to an existing App Service. Use the url of the App Service as the **SERVICE_URL** in Keys.cs

### 2. Twitter

Twitter is used to authenticate a user to the Backdrop service and use their profile image. Backdrop uses the [UWP Community Toolkit](https://github.com/Microsoft/UWPCommunityToolkit) Twitter Service for authentication which requires a consumer key, consumer secret, and callback uri. Follow the steps [here](https://apps.twitter.com/app/new) to create a new Twitter app and paste the keys in Keys.cs once done. Visit the [UWP Community Toolkit documentation](https://developer.microsoft.com/en-us/windows/uwp-community-toolkit/services/twitter.htm) for more details.

### 3. Soundcloud

Backdrop uses Soundcloud for it's music service and the API requires a client id, client secret, and redirect url. [Register a new SoundCloud app](http://soundcloud.com/you/apps/new) and paste the required information in Keys.cs