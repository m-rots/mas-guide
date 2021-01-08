+++
title = "Installing the MAS dependencies"
date = 2021-01-08
+++

For those having issues installing the project MAS dependencies, here is a little writeup guiding you through the installation process!

The instructions for MacOS and Windows are nearly the same but I will let you know when certain instructions are for Mac/Windows only. Let's get started!

## Removing old Java & Eclipse versions
GOAL has been updated in late December and is causing issues for the Assignment 0-instructions. Specifically, GOAL will not install with JDK-8u251 and Eclipse 2018-09.

Therefore, we want to update both of them. However, to do so we have to uninstall the old versions and then install the new versions.

### Uninstalling Eclipse 2018-09
Eclipse is not installed as a normal "app". Meaning: it's not in `~/Applications` on MacOS and not un-installable through `Programs & Features` on Windows. Instead, it's located in four directories:

- `~/.eclipse`
- `~/.p2`
- `~/eclipse`
- `~/eclipse-workspace`

The `~` indicates the user directory for both operating systems. \
Windows: `C:\Users\<username>\` \
Mac: `/Users/<username>/`

Not all directories might be visible from Windows Explorer / Finder. So make sure you make hidden files/folders visible. \
Windows: In the view options there should be an option to show hidden files. \
Mac: `cmd + shift + .` in Finder

Delete all four directories.

### Uninstalling Java
On Windows you should be able to uninstall Java (JRE and JDK) from `Programs and Features`.

For MacOS, please check [Oracle's article](https://docs.oracle.com/javase/10/install/installation-jdk-and-jre-macos.htm#JSJIG-GUID-F9183C70-2E96-40F4-9104-F3814A5A331F) on how to uninstall JDK8.

You might want to reboot afterwards just in case, though not required!

## Installing the latest JDK, Eclipse and GOAL
In this guide we will install JDK15 together with Eclipse 2020-12 and the latest GOAL version.

First, we are going to install JDK15. You can download the JDK installer on [Oracle's download page](https://www.oracle.com/nl/java/technologies/javase-jdk15-downloads.html). Make sure to download the installer instead of the compressed archive. Then, simply run the installer. To make sure it's installed, you can run `java -version` from a new cmd or terminal window.

Afterwards, simply download the installer for Eclipse IDE 2020-12 from [Eclipse's website](https://www.eclipse.org/downloads/). Then once you're in the installer, make sure to select `Eclipse IDE for Java Developers`.

With Eclipse installed, open Eclipse and click on `Help > Install new software`. Click on the `add` button in the pop-up window and use `GOAL` as name and use `https://dl.bintray.com/goalhub/GOAL` as location. Make sure `Group items by category` is enabled on the bottom of the pop-up window and then click on the checkmark next to `GOAL Agent Programming`. Click on next to start the installation process. In the middle of the installation process it will ask you whether you still want to install it. Make sure to click on `Install anyway`.

Once GOAL is installed it will ask you to restart Eclipse, please do so. To open the GOAL perspective, click on `Window > Perspective > Open Perspective > Other` and then click on GOAL.

Next, open your github repository in Eclipse and make sure to use the [new connector](/cbsr-eis-connector.jar)!