# Xamarin Workshop Setup

## Introduction

Xamarin requires a few components to collaborate for a satisfying development experience. It is important that each participant to the workshop installs and tests the setup prior to the workshop day, so that we don’t lose any time and can jump into code as soon as possible 😊

## Configurations

You can develop for Xamarin using Windows or Mac. However if you use Windows and want to build Xamarin apps for iOS, you need a Mac computer too. This is because of Apple restrictions and cannot be avoided. During the workshop, we will support the following configurations:

__From a Windows PC:__

* Preferred: Develop for Android devices using a physical device connected through USB.
* Develop for Android devices using an emulator running on the PC directly.

__From a Mac:__

* Preferred: Develop for Android devices using a physical device connected through USB.
* Develop for iOS devices using a physical device connected through USB.
* Develop for Android devices using an emulator running on the Mac directly.
* Develop for iOS devices using a simulator running on the Mac directly.

__Keys to success:__

* Bring your own Windows PC and/or Mac PC to the workshop. Make sure to follow the instructions below for the Xamarin setup.
* If you have one, we recommend that you bring your own Android or iOS devices to the workshop. This is the easiest way to test your application

## Prerequisites on a Windows PC

You can see the requirements and follow the steps for Xamarin environment setup on Windows at: https://docs.microsoft.com/en-us/xamarin/cross-platform/get-started/installation/windows.

1. Install Visual Studio 2017 from https://www.visualstudio.com/vs. The free Community Edition is sufficient for this workshop.
2. Make sure to select the _"Mobile development with .NET"_ workload in the installer screen:
   ![The Xamarin workload selected in the installer](./Images/Setup/VS2017Workload.png)
3. You don’t need all options selected but you should choose the following:
   ![The required components in the installation](./Images/Setup/VS2017SelectedBits.png)

### Testing the setup

After the installation is complete, test the setup with the following steps:

1. In Visual Studio, select File, New, Project.
2. In the "New Project" dialog, select the Cross-Platform category.
3. Select "Mobile App (Xamarin.Forms)".
4. In the "New Cross Platform App" dialog, select "Blank App".
5. Under Platform, select "Windows (UWP)" and "Android". Deselect "iOS".
6. Under Code Sharing Strategy, select ".NET Standard".
   ![Creating a new Xamarin project](./Images/Setup/VS2017CreateNewProject.png)
7. Press OK.

With the application created in Visual Studio, we will now test on Windows and on the Android emulator. If this works fine, we will guide you during the workshop to deploy to your devices.

#### Running on Windows

Now we will try running the application in Windows and Android to see if everything works fine.

1. In the Solution Explorer, right click on the UWP version of the application and select "Set as Startup Project" from the context menu.
   ![Setting the UWP app as the startup app](./Images/Setup/VS2017SetUWPASStartup.png)
2. Select x86 Build Configuration
3. Select Debug Build Configuration
4. Click on the Start button with "Local Machine".
   ![Running the UWP app on the local machine](./Images/Setup/VS2017RunUWP.png)
5. After a short wait, you should see the UWP version of the application running.
   ![The UWP app running on the local machine](./Images/Setup/VS2017RunningUWP.png)

#### Running on Android

1. In the Solution Explorer, right click on the Android application and select "Set as Startup Project" from the context menu.
   ![Setting the Android app as the startup app](./Images/Setup/VS2017SetAndroidAsStartup.png)
2. In the Start button, the Android emulator should be selected as shown below:
   ![The Android emulator selected in the start button](./Images/Setup/VS2017RunningAndroid.png)
3. Click on the Start button to run the Android emulator.
   > You might have to select a video device when the emulator starts for the first time. You don’t have to select anything, you can just press OK. The emulator takes some time to boot, but once it is up and running, you don’t need to shut it down. It can just stay up.

   After the emulator runs, you should be able to see the application:
   ![The UWP app running on the emulator](./Images/Setup/VS2017RunningAndroidEmulator.png)

## Prerequisites on a Mac

You can see the requirements and follow the steps for Xamarin environment setup on Mac at: https://docs.microsoft.com/en-us/visualstudio/mac/installation.

1. Install Visual Studio for Mac from https://www.visualstudio.com/vs. The free Community Edition is sufficient for this workshop.
2. Open the App Store app on macOS, search for Xcode and install Xcode. Visual Studio requires Xcode to build the iOS applications as well as run them on the Simulator.
   > Important: After you finish installing Xcode, run it once to make sure that all the necessary component are up to date. Some components are only downloaded the first time that Xcode runs.

### Testing the setup

After the installation is complete, test the setup with the following steps:

1. In Visual Studio for Mac, select New Project.
   ![The New Project button in VS for Mac](./Images/Setup/VSMacNewProject.png)
2. In the "Choose a template…" dialog, select Multiplatform, App, Forms App, then press Next.
   ![The Forms template in the VS for Mac New Project dialog](./Images/Setup/VSMacNewFormsApp.png)
3. Enter a name for the application and your company name, then press Next.
   ![Configuring the new Forms App settings](./Images/Setup/VSMacConfigureApp.png)
4. Check the project location and details, and press Create.
   ![Configuring the new Forms project settings](./Images/Setup/VSMacConfigureProject.png)

With the application created in Visual Studio for Mac, we will now test on the Android emulator and the iOS simulator. If this works fine, we will guide you during the workshop to deploy to your devices.
> It is possible that Visual Studio requires you to install the Android SDK (or updates to it) when you create the new application. You should accept and wait until the SDK is installed.

#### Running on Android

1. In the Solution Explorer, right click on the Droid project and select Set as Startup Project from the context panel.
   ![Setting the Android app as the startup project in VS for Mac](./Images/Setup/VSMacSetDroidStartup.png)
2. In the top bar, make sure that the Android emulator is selected (for example "Android_Accelerated_Nougat (API 25)").
   ![Setting the Android emulator to use](./Images/Setup/VSMacSelectDroidEmulator.png)
3. Press the Run button (on the left with the triangle). This will build the application and start the Android emulator. After a short wait, you should see the application running on the emulator.
   ![The sample app running on Android](./Images/Setup/VSMacRunningDroid.png)

#### Running on iOS

1. Right click on the iOS project in the Solution Explorer and select Set As Startup Project from the context menu.
   ![Setting the iOS app as the startup project in VS for Mac](./Images/Setup/VSMacSetiOSStartup.png)
2. In the top bar, select the simulator that you want to test on (for example iPhone X iOS 11.3).
   ![Setting the iOS simulator to run on](./Images/Setup/VSMacSelectiOSSim.png)
3. Press the Run button (on the left with the triangle). This will build the iOS application and start the simulator. After a short wait you should be able to see the application in the simulator.
   ![The sample app running on iOS](./Images/Setup/VSMacRunningiOS.png)

## Enabling Developer Mode on a Physical Android Device

If you want to use a physical Android device then you will need to enable developer mode. This will ensure that you can load the applications to the device, debug on the device, etc. Please follow these steps:

1. Open the Settings app.
2. If you are on Android 8.0 or higher, select System.
3. Scroll to the bottom and select About phone.
4. Scroll to the bottom and tap Build number 7 times.
5. Return to the previous screen to find Developer options near the bottom.
6. Select Developer options, and then enable USB debugging.
7. Plug your device into your Mac or PC, set the Android app as the startup app, then select the device in the menu bar. A dialog will pop up on your Android device asking if you want to allow USB debugging from the connected Mac or PC.  Tap "Always allow", then tap "ok".
   ![Always allow USB debugging](./Images/Setup/AndroidAllowDebug.png)

You can find more information at https://developer.android.com/studio/run/device
