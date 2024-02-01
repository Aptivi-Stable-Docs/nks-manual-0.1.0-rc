---
description: How to install Nitrocid KS on Android
---

# 📱 Android

<figure><img src="../../.gitbook/assets/Screenshot_20231215_182920_Termux.png" alt=""><figcaption></figcaption></figure>

The tricky part is getting Nitrocid KS to run on Android phones and tablets, especially those that run the latest version of Android.

## Installation

To install Nitrocid KS on your phone or tablet, install the following dependencies:

* [Termux](https://termux.dev/en/)
* [Ubuntu PRoot](https://wiki.termux.com/wiki/PRoot#Installing\_Linux\_distributions)

Ensure that your Android version is compatible with Termux. You need at least 8 GB of free storage and Android 7.0 or higher.

{% hint style="info" %}
To get a better experience with Nitrocid KS on your phone or your tablet, it's advisable to get a phone or a tablet that supports desktop mode ([Samsung DeX](https://insights.samsung.com/2022/08/12/the-beginners-guide-to-samsung-dex-11/) for example) and a Bluetooth mouse and keyboard.
{% endhint %}

### Required packages

You can consult the required dependencies here:

{% content-ref url="../dependency-information.md" %}
[dependency-information.md](../dependency-information.md)
{% endcontent-ref %}

Once you're done, follow the steps:

1. Install Termux
2. Install proot-distro using the following command:
   * `pkg install proot-distro`
3. Install the Ubuntu proot
   * `proot-distro install ubuntu`
4. Log in to the Ubuntu proot
   * `proot-distro login ubuntu`
5. Ensure that you've updated the package cache
   * `apt update`
   * `apt dist-upgrade`
6. Install the .NET 8.0 runtime
   * `apt install dotnet-runtime-8.0`
7. Install wget to download the latest release from [this page](https://github.com/Aptivi/Kernel-Simulator/releases).
   * `apt install wget`
   * `wget https://github.com/Aptivi/Kernel-Simulator/releases/download/v0.x.x.x-beta/0.x.x.x-bin.zip`
8. Install unzip to extract the files
   * `apt install unzip`
   * `unzip 0.x.x.x-bin.zip`
9. Execute `dotnet Nitrocid.dll`

{% hint style="info" %}
For 0.0.24.x or older, files that end with the `-dotnet` prefix means that it's for .NET 6.0.
{% endhint %}

## Bleeding-edge

Bleeding-edge builds usually come from building the development branch of the kernel, and they usually contain bugs and other untested features.

If you're a tester to such software, please follow the steps on your Windows machine. Please be sure that you're signed in to your GitHub account.

1. Open [this page](https://github.com/Aptivi/Kernel-Simulator/actions/workflows/build-linux.yml)
2. Select the most recent build
3. Scroll down to Artifacts and click on the `ks-build` button to download the ZIP file on your device
4. Repeat steps 1-6 in the `Installation` section
5. Now, use the `termux-setup-storage` command. Follow the instructions [here](https://wiki.termux.com/wiki/Termux-setup-storage).
6. Copy the `ks-build.zip` file from `~/storage/downloads/ks-build.zip` to your home directory
   * `cp ~/storage/downloads/ks-build.zip ~/`
7. Still in the home directory, install unzip to extract the files
   * `apt install unzip`
   * `unzip ks-build.zip`
8. Execute `dotnet Nitrocid.dll`
