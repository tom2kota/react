# react
Start React Project
---

[DeepSpaceHouse](https://youtu.be/P15NtXKEM-w?t=64)

[GitHub Pages](https://tom2kota.github.io/react/)


----------


# react native
Start React Native Project
---

[rn-casts](https://github.com/tom2kota/rn-casts)

[iOS Simulator](https://docs.expo.io/workflow/ios-simulator/)


[Android Studio Emulator](https://docs.expo.io/workflow/android-studio-emulator/)


----------

# macOS
# XCode iOS Simulator


Download the full version of Xcode from the App Store. This is a huge file at around 7GB, so it can take a LONG time to download and install. It might seem like it it is stuck and not installing, but it is probably not.

Launch XCode and agree to its terms. It will start installing more tools and software

Eventually, you will get a "Welcome to XCode" screen

In the top menu bar, click "XCode", then "Preferences" and then "Locations".

Make sure that the "Command Line Tools" are installed and selected.

In the top menu bar, click XCode, then "Open Developer Tool" then click "Simulator"

This will open an iPhone simulator on your machine. If everything is working well, it should load a generic screen with a few apps.

Go to your terminal and in your React Native project directory, run npm start

When the Metro Bundler opens up in your browser, click on the option in the left sidebar to “Run on iOS simulator”

If you navigate back to your iPhone simulator you should see an “Open In Expo” button. Click Open.

This will launch the Expo application in the simulated device and run your bundled code. Eventually, it should load the “Hi There!” screen.


----------


## Android Studio Simulator

[Install Android Studio](https://developer.android.com/studio)

After downloading, run the installer.

A dialog box should pop up. Do not Import Settings, Just Click "Ok"

Click “Next" to go thru the Wizard

Click “Next” to do a Standard install

Choose light or dark theme for your editor and click “Next”

Click “Finish”

You will likely get a dialog box pop and say “HAXM Installation wants to make changes”. Enter your password and click OK

If you get a “System Extension Blocked” error, follow the prompt to Open Security Preferences and click “Allow” for “Intel Corporation Apps”

Once the HAXM installer finished you should get a dialog box from Android Studio.

Click “AVD Manager”

Click “Create New Virtual Device”

Select a Device from the list and click “Next”

If the System Image for the most recent SDK is not installed, you will need to click the "Download" link next to the SDK version.

After the image has been downloaded, click “Next”

Preview the settings and then click “Finish”

You should see the newly created device in the “Your Virtual Device” screen.

Click the Play ▶️button all the way to the right in the "Actions" column.

This will open an Android simulator on your machine. If everything is working well, it should load a generic screen with a few apps.

Go to your terminal and in your React Native project directory, run npm start

When the Metro Bundler opens up in your browser, click on the option to “Run on Android simulator”

If you navigate back to your Android simulator you might see a “Permit Drawing Over Other Apps” message. Click the OK button and it should take you to the system settings screen to enable this. You will likely have to go back to the Metro Bundler and select “Run on Android simulator” again.

This will launch the Expo application in the simulated device and run your bundled code. Eventually, it should load the “Hi There!” screen.


----------

# Windows
# ios Simulator

Unfortunately, you cannot run iOS simulators on Windows. You can, however, use a physical iOS device running Expo with your Windows machine.


----------


## Android Studio Simulator

Make sure Virtualization is enabled in your BIOS. Also, note, your processor must support [HAXM](https://github.com/intel/haxm). If it does not (which is common with many AMD or non-Intel machines) you will likely not be able to run the simulators. HAXM will also conflict with the Hyper-V Manager if it is enabled.

[Install Android Studio](https://developer.android.com/studio)
After Downloading run the installer.

Click “Next" to go through the installer wizard.

Click “Next” on Choose Components screen

Click “Next” on the Configuration Settings screen

Click “Install”

After completion click “Next”

Click “Finish”

In the next dialog box that pops up, do not Import settings, Just Click "Ok"

Click “Next" to go thru the Wizard

Click “Next” to do a Standard install

Choose light or dark theme for your editor and click “Next”

Click “Finish”

Once the HAXM installer finishes you should get a dialog box from Android Studio.

Click “AVD Manager”

Click “Create New Virtual Device”

Select a Device from the list and click “Next”

If the System Image for the most recent SDK is not installed, you will need to click the "Download" link next to the SDK version.

After the image has been downloaded, click “Next”

Preview the settings and then click “Finish”

You should see the newly created device in the “Your Virtual Device” screen.

Click the Play ▶️button all the way to the right in the "Actions" column.

This will open an Android simulator on your machine. If everything is working well, it should load a generic screen with a few apps.

Go to your terminal and in your React Native project directory, run npm start

When the Metro Bundler opens up in your browser, click on the option to “Run on Android simulator”. If it does not open in your browser, you may need to go to localhost:19002 in your browser.

If you navigate back to your Android simulator you might see a “Permit Drawing Over Other Apps” message. Click the OK button and it should take you to the system settings screen to enable this. You will likely have to back to the Metro Bundler and select “Run on Android simulator” again.

This will launch the Expo application in the simulated device and run your bundled code. Eventually, it should load the “Hi There!” screen.


----------

# Expo Cli

## Windows

1. Try using a different terminal. There are few choices, CMD prompt, PowerShell, GitBash and CMDer.

2. Make sure you have installed Git as one of Expo's dependencies will need it:

[Git](https://git-scm.com/download/win)

3. Make sure that your project files are on the C drive rather than on some external or remote drive. This may be causing permissions errors or inconsistencies with the install.

If the installation seemed like it worked but you are getting errors starting expo, delete your package-lock.json file, node_modules directory and ``` run npm cache clean -f ```. Then run a new ``` npm install ``` as a regular user. Finally, run an ```npm start ``` again to install the ***Expo Cli tools***.

## macOS

1. Make sure your project is not on the Desktop as the file watchers will have some permissions issues with this location.

If you run into an endless loop:

You may have run into a loop where the terminal prompt keeps asking you to install the global cli tools. If this is the case, you'll need to install the tools manually.
```
npm install expo-cli --global
```

If this command fails due to permissions errors, please refer to the npm docs on avoiding the use of sudo:

On the command line, in your home directory, create a directory for global installations:
```
 mkdir ~/.npm-global
 
 ```
 
Configure npm to use the new directory path:
```
 npm config set prefix '~/.npm-global'
 ```
 
In your preferred text editor, open or create a ~/.profile file and add this line:
```
 export PATH=~/.npm-global/bin:$PATH
 ```
 
On the command line, update your system variables:
```
 source ~/.profile
 ```
 
To test your new configuration, install a package globally without using sudo:
```
npm install expo-cli --global
```

Then attempt to run an npm start again - you should not get prompted to install the tools this time and the ***Metro Bundler should start up***.

IMPORTANT - If you are using macOS Catalina, it is highly likely that your default shell is now zsh. If so, you will need to instead create a ``` ~/.zprofile ``` instead of a ``` ~/.profile ``` when following these instructions:

[docs](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)


