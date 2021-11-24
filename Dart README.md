# React Native Documintaion

## Install for Windows
##### You will need Node, Python2, JDK and Android Studio.

##### 1. Node and Python2
in cmd:

```
choco install -y nodejs.install python2 jdk8
```


##### 2. JDK [Download](https://download.oracle.com/java/17/latest/jdk-17_windows-x64_bin.exe)
##### 3. Android Studio [Download](https://redirector.gvt1.com/edgedl/android/studio/install/2020.3.1.25/android-studio-2020.3.1.25-windows.exe)

###### 1. Install Android Studio

make sure all of the following boxes are checked:
- [x] Android SDK
- [x] Android SDK Platform
- [x] Android Virtual Device

Then, click `Next` to install all of these components.

###### If the checkboxes are grayed out, you will have a chance to install these components later on.

###### 2. Install the Android SDK
 Android Studio installs the latest Android SDK by default.

 however,Additional Android SDKs can be installed through the SDK Manager in Android Studio.

To do that, open Android Studio, click on "Configure" button and select "SDK Manager".


![AndroidStudio](https://user-images.githubusercontent.com/92295682/143215962-a2a44407-603d-47a7-be57-61f3713e8c5b.png)

- Select the "SDK Platforms" tab from within the SDK Manager
- check the box next to "Show Package Details"
- make sure the following items are checked:
 - [x] Android SDK Platform 29
 - [x] Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image
- select the "SDK Tools"
- check the box next to "Show Package Details"
- Look for and expand the "Android SDK Build-Tools"
- then make sure that 29.0.2 is selected.

##### Finally, click "Apply" to download and install the Android SDK and related build tools.

###### 3. Configure the ANDROID_HOME environment variable
- Open the Windows Control Panel.
- Click on User Accounts, then click User Accounts again
- Click on Change my environment variables
- Click on New... to create a new ANDROID_HOME user variable that points to the path to your Android SDK:

![تنزيل](https://user-images.githubusercontent.com/92295682/143204267-d9285f79-0861-4060-a985-b6a6832bd88e.png)

You can find the actual location of the SDK in the Android Studio "Settings" dialog, under Appearance & Behavior → System Settings → Android SDK.

Open a new Command Prompt window:
- Open powershell
- Copy and paste Get-ChildItem -Path Env:\ into powershell
- Verify ANDROID_HOME has been added

###### 4. Add platform-tools to Path
- Open the Windows Control Panel.
- Click on User Accounts, then click User Accounts again
- Click on Change my environment variables
- Select the Path variable.
- Click Edit.
- Click New and add the path to platform-tools to the list.

The default location for this folder is:

`%LOCALAPPDATA%\Android\Sdk\platform-tools`

#### React Native Command Line Interface
we recommend you access the current version at runtime using npx

`npx react-native`

### Creating a new application
React Native has a built-in command line interface, which you can use to generate a new project. You can access it without installing anything globally using npx, which ships with Node.js. Let's create a new React Native project called "AwesomeProject":

```
npx react-native init AwesomeProject
```
### [Optional] Using a specific version or template
If you want to start a new project with a specific React Native version
```
npx react-native init AwesomeProject --version X.XX.X
```

You can also start a project with a custom React Native template
```
npx react-native init AwesomeTSProject --template react-native-template-typescript
```

### Running your React Native application
#### Step 1: Start Metro
inside your React Native project folder:
```
npx react-native start
```
#### Step 2: Start your application
Open a new terminal inside your React Native project folder. Run the following:
```
npx react-native run-android
```
If everything is set up correctly, you should see your new app running in your Android emulator shortly.
