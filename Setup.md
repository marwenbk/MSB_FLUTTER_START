## Run System update

Let’s first run the system update command before installing Flutter, this will update all the already installed packages on our Debian Linux. In addition to refreshing the system repo cache.

```
sudo apt update
```

## Install Dependencies

There are few tools and libraries required to use Flutter on Linux such as Debian. Hence, before moving further use the below-given command to install them:

```
sudo apt install curl file git unzip xz-utils zip libglu1-mesa clang cmake ninja-build pkg-config libgtk-3-dev
```

## Download Latest Flutter SDK

Next, we need the Flutter SDK tarball file. That we can easily download from its official webpage. [Here is the link](https://docs.flutter.dev/development/tools/sdk/releases?tab=linux). Visit the page and select the latest version of Flutter to download.
![](https://i.imgur.com/hMKtElV.png)

## Install Flutter on Debian

Extract files:

```
cd ~
tar xvf ~/Downloads/flutter_linux_*-stable.tar.xz
```

## Add the flutter to the environment path

```
nano ~/.bashrc
export PATH="$PATH:~/flutter/bin"
```

![](https://i.imgur.com/fDNIIug.png)
Once you confirmed the folder where you have extracted Flutter is in the Environment path, let’s verify Flutter command-line tools are working perfectly:

```
flutter --version
```

![](https://i.imgur.com/Fs0W1WH.png)

## Check any missing dependency using- flutter doctor

Well, although we have completed the installation successfully along with the required dependencies. However, still in the case, something is missing to complete the setup, it can be pointed out using the Flutter’s doctor command:

```
flutter doctor
```

![](https://i.imgur.com/n0Q0yqV.png)

## Get Chrome browser

```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

## Install Android Studio on Debian

Open your browser and Download Android Studio for Linux. [Visit the official page](https://developer.android.com/studio#downloads) and then select the Tarball file.
![](https://i.imgur.com/dkwpGxi.png)

```
cd Downloads
tar xvf android-studio-*-linux.tar.gz
sudo mv android-studio /opt/
/opt/android-studio/bin/./studio.sh
```

![](https://i.imgur.com/ZWNLAGm.png)
![](https://i.imgur.com/omnHkHH.png)

To create Android Studio icon, please follow the steps here: [Link](https://gist.github.com/haunt99/15cc273f791f690e587681516d58170a)

## Install Android SDK Command-line Tools

On your Android Studio Project, click on the **File** and then **"Settings"**.
![](https://i.imgur.com/tfkOGwv.png)
Select **Appearance & Behavior > System Settings > Android SDK > SDK Tools**

Check the box given for **“Android SDK Command-line Tools (latest)”** and then press the **OK** button.
![](https://i.imgur.com/J84tYcz.png)

## Add command-line tools to your environment

```
nano ~/.bashrc
export PATH=$PATH:~/Android/Sdk/cmdline-tools/latest/bin
source ~/.bashrc
```

![](https://i.imgur.com/pOxTXlH.png)

## Agree to Android Licenses

To use Flutter, the user must agree to the licenses of the Android SDK platform. Here is the command for the same:

```
flutter doctor --android-licenses
```

![](https://i.imgur.com/BYTUhAQ.png)

## Check Again Flutter requirements

Let’s check again that Flutter dependencies are completed and the setup is successful.

```
flutter doctor
```

![](https://i.imgur.com/stwmUEh.png)

## Set up an editor

To set up the editor, go to Android Studio open any project, click on the **File**, and then select **Settings**. There select **“Plugins”** and select **Flutter** to Install it.
![](https://i.imgur.com/8G7KXsB.png)

## Create Flutter Project

Now, create a New Flutter Project…
![](https://i.imgur.com/ktCy00l.png)
Select Flutter and set the full path to its SDK. For that Just enter the path of the folder where you have extracted the Flutter.
![](https://i.imgur.com/5WgPCCK.png)
