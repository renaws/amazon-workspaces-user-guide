# WorkSpaces Android client application<a name="amazon-workspaces-android-client"></a>

The following information will help you get started with the WorkSpaces Android client application\.

**Topics**
+ [Requirements](#android-requirements)
+ [Setup and installation](#android_setup)
+ [Connect to your WorkSpace](#android_connecting)
+ [Gestures](#android_gestures)
+ [Sidebar menu](#android_sidebar_menu)
+ [Keyboard](#android_keyboard)
+ [Trackpad mode](#android_trackpad_mode)
+ [Display support](#android_display_support)
+ [Disconnect](#android_disconnect)
+ [Clipboard support](#android_clipboard_support)
+ [Release notes](#android-release-notes)

## Requirements<a name="android-requirements"></a>

The Amazon WorkSpaces Android client application requires the following:
+ Amazon Kindle Fire tablets released after 2012 with Fire OS 4\.0 and later\.
+ Android tablets and phones with Android OS 4\.4 and later\. The client application works on most devices with Android version 4\.4 or later, but some devices might not be compatible\. If you have problems with a device, you can report the problem on the [WorkSpaces forum](https://forums.aws.amazon.com/forum.jspa?forumID=164)\.
**Note**  
Versions of the Android client application after 2\.4\.15 require devices with Android OS 9 and later\.
+ Chromebooks that support installing Android applications\. Chromebooks launched in 2019 or later support installing Android applications\. However, some Chromebooks launched before 2019 might not support installing Android applications\.

  We recommend using the Android client application if your Chromebook supports it\. To determine whether your Chromebook is compatible with the Amazon WorkSpaces Android client application or whether it requires the Amazon WorkSpaces Chromebook client application, see the [installation steps for Chromebooks launched before 2019](#chromebook_install_before_2019)\.
+ Devices that support running 64\-bit applications\.

**Note**  
The WorkSpaces Android client application is not available for the WorkSpaces Streaming Protocol \(WSP\)\.
If your WorkSpace is located in the Asia Pacific \(Mumbai\) Region, you must use version 2\.4\.19 or later of the Amazon WorkSpaces Android client application\.

## Setup and installation<a name="android_setup"></a>

To download and install the client application, complete the following procedure\.

**\(For devices other than Chromebooks launched before 2019\) To download and install the client application**

1. On your device, open [https://clients\.amazonworkspaces\.com/](https://clients.amazonworkspaces.com/) and choose the link for your device \(either **Android/Chromebook** or **Fire Tablet**\)\.

1. Download and install the application\.

1. Verify that the Amazon WorkSpaces client application icon appears on one of the device desktops\.

**\(For Chromebooks launched before 2019\) To download and install the client application**

1. Determine whether your Chromebook supports Android applications by checking its status on the list of [ Chrome OS Systems Supporting Android Apps](https://sites.google.com/a/chromium.org/dev/chromium-os/chrome-os-systems-supporting-android-apps)\.

1. Depending on your Chromebook's status, do one of the following:
   + If your Chromebook's status is marked as **Stable Channel**, do the following:

     1. Follow the instructions in [ Install Android apps on your Chromebook](https://support.google.com/chromebook/answer/7021273) to enable your Chromebook to install Android applications\. 
**Note**  
In some cases, your WorkSpaces administrator might need to enable your Chromebook to install Android applications\. If you are unable to install the Android client application on your Chromebook, contact your WorkSpaces administrator for assistance\.

     1. On your Chromebook, open [https://clients\.amazonworkspaces\.com/](https://clients.amazonworkspaces.com/) and choose **Android/Chromebook**\.

     1. Download and install the application\.

     1. Verify that the Amazon WorkSpaces client application icon appears on one of the device desktops\.
   + If your Chromebook's status is marked as **Planned** or if your Chromebook does not appear on the list, do the following:

     1. Determine whether your Chromebook meets the requirements of the Amazon WorkSpaces Chromebook client application:
        + The WorkSpaces Chromebook client application requires a Chromebook with Chrome OS version 45 or later\. The client application works on most Chromebooks with version 45 or later, but some devices might not be compatible\. If you have problems with a device, you can report the problem on the [WorkSpaces forum](https://forums.aws.amazon.com/forum.jspa?forumID=164)\.
        + To check the version of Chrome OS on your Chromebook, go to the status area, where your account picture appears\. Choose **Settings**, **About Chrome OS**\.

     1. If your Chromebook is running Chrome OS version 45 or later, open the link to the [ Amazon WorkSpaces Chromebook client application](https://chrome.google.com/webstore/detail/amazon-workspaces/ipaonomeflaallpcgnhcaoonfghaojha) on the Chrome Web Store\.

     1. Download and install the application\.

     1. Verify that the Amazon WorkSpaces client application icon appears in your Chromebook search\.

## Connect to your WorkSpace<a name="android_connecting"></a>

To connect to your WorkSpace, complete the following procedure\.

**To connect to your WorkSpace**

1. On your device, open the Amazon WorkSpaces client application\.

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. You can enter a different registration code by launching the client application and tapping **Enter new registration code** on the login screen\.

1. Enter your user name and password and tap **Sign In**\. If your WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your WorkSpaces administrator has not disabled the "Remember Me" feature, you are prompted to save your credentials securely so that you can connect to your WorkSpace easily in the future\. Your credentials will be securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

## Gestures<a name="android_gestures"></a>

The following gestures are supported for the WorkSpaces Android client application\.

Single tap  
Equivalent to a single click in Windows\.

Double tap  
Equivalent to a double\-click in Windows\.

Two finger single tap  
Equivalent to a right\-click in Windows\.

Two finger double tap  
Toggles the on\-screen keyboard display\. If a keyboard is attached to the device, a set of keyboard shortcuts is shown instead\.

Swipe from left  
Displays the sidebar menu\. For more information, see [Sidebar menu](#android_sidebar_menu)\.

Two finger scroll  
Scrolls vertically\.

Two finger pinch  
Zooms display in or out\.

Two finger pan  
Pans the desktop when zoomed in\.

## Sidebar menu<a name="android_sidebar_menu"></a>

The sidebar menu is displayed by swiping from the left side of the screen\.

![\[Android sidebar menu\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-menu.png)

The sidebar menu provides quick access to the following features:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-trackpad.png) **Trackpad Mode** – Turns the trackpad on or off\. For more information, see [Trackpad mode](#android_trackpad_mode)\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-keyboard.png) **Show Keyboard** – Toggles the display of the on\-screen keyboard\. If a keyboard is already attached, only a row of keyboard shortcuts is displayed\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-settings.png) **Settings** – Displays controls to change the screen resolution or the scroll direction\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-connection.png) **Connection Check** – Displays the connection status\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-windows.png) **Windows Menu** – Displays the Windows Start Menu\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/android-sidebar-disconnect.png) **Disconnect** – Disconnects the client application without logging off\.

## Keyboard<a name="android_keyboard"></a>

To toggle the display of the on\-screen keyboard, double\-tap with two fingers anywhere on the screen\. Special key combinations are displayed in the top row of the keyboard\.

## Trackpad mode<a name="android_trackpad_mode"></a>

The trackpad mode is set using the [sidebar menu](#android_sidebar_menu)\.

### Trackpad mode off<a name="android_trackpad_off"></a>

When trackpad mode is off, the mouse cursor is placed wherever you tap your finger\. In this mode, a single tap is equivalent to a left mouse button click and a two finger single tap is equivalent to a right mouse button click\.

### Trackpad mode on<a name="android_trackpad_on"></a>

When trackpad mode is on, the mouse cursor tracks the movement of your finger on the screen\. In this mode, simulate a left mouse button click by tapping the left mouse button icon\.

![\[Left mouse button icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/mouse-icon-left.png)

Simulate a right mouse button click by tapping the right mouse button icon\.

![\[Right mouse button icon\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/mouse-icon-right.png)

## Display support<a name="android_display_support"></a>

The Amazon WorkSpaces Android client application supports a single monitor\. Multiple monitors are not supported\.

The maximum supported screen resolution depends on your device's display\. Although specific screen resolution settings are offered in the **Settings** menu, if you choose **Default**, WorkSpaces matches the resolution that you've set on your device\. If your device supports a resolution higher than 2800x1752, choose **Default** if you want WorkSpaces to use a higher resolution\. 


| Resolution setting | When to use | 
| --- | --- | 
| 2800x1752, 2560x1440, 1920x1080, 1600x900, 1280x720, 960x540 | Choose one of these settings if you want your display to use this exact resolution\. | 
| Default | Choose this setting to match the resolution that you've set on your device, up to the maximum resolution that your device supports\. If you choose Default and you're using a high DPI display, the screen resolution is adjusted to a lower one so that text and icons are easier to read\.  | 
| High DPI Mode | Choose this setting for better maximum resolution of your WorkSpace on high DPI displays\. If you choose High DPI Mode and the text and icons on your WorkSpace are smaller than you'd prefer, either choose Default instead, or adjust the scaling settings on your WorkSpace\. For more information about high DPI mode and how to adjust the scaling settings on your WorkSpace, see [WorkSpaces high DPI display support](high_dpi_support.md)\. | 

## Disconnect<a name="android_disconnect"></a>

To disconnect the Android client, display the sidebar menu, tap the disconnect icon, and tap **Disconnect**\. You can also log off of the WorkSpace, which disconnects the client\.

## Clipboard support<a name="android_clipboard_support"></a>

The clipboard supports copy and paste of text and HTML content only\. The maximum uncompressed object size is 20 MB\. For more information, see [I'm having trouble copying and pasting](client_troubleshooting.md#copy_paste)\.

**Note**  
When copying from a Microsoft Office app, the clipboard only contains the last copied item, and the item is converted into standard format\. If you copy content larger than 890 KB from a Microsoft Office app, the app might become slow or unresponsive for up to 5 seconds\. 

## Release notes<a name="android-release-notes"></a>

### Android client application release notes<a name="android-client-release-notes"></a>

The following table describes the changes to each release of the Android client application\.


| Release | Date | Changes | 
| --- | --- | --- | 
| 3\.0\.2 | July 13, 2021 |  Minor enhancements and fixes  | 
| 3\.0\.1 | June 30, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
| 2\.4\.21 | May 20, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.20  | March 25, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.19  | February 22, 2021 |  Enhanced support for resolution 2560x1440  | 
|  2\.4\.18  | October 19, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.17  | February 24, 2020 |  Minor enhancements and fixes  | 
|  2\.4\.16  | January 30, 2020 |  Adds 64\-bit support for Android 9 and 10  | 
|  2\.4\.15  | June 24, 2019 |  Adds support for mouse cursor contextual shape changes  | 
|  2\.4\.14  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.13  |  |  Minor fixes  | 
|  2\.4\.12  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.11  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.10  |  |  Improves support for Japanese keyboard layouts  | 
|  2\.4\.9  |  |  Adds support for Samsung Galaxy Note 9  | 
|  2\.4\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.6  |  |  Adds support for uniform resource identifiers \(URIs\), which enable login orchestration  | 
|  2\.4\.5  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.4  |  | Minor improvements to session provision handling | 
|  2\.4\.2  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.3\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.3\.3  |  |  Localization enhancements  | 
|  2\.2\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.1\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.0\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.15  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.11  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.10  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0\.9  |  |  Improves the login experience  | 
|  1\.0  |  |  Initial release  | 

### Chromebook client application release notes<a name="android-chromebook-release-notes"></a>

The following table describes the changes to each release of the Chromebook client application\.

**Note**  
Version 2\.4\.13 is the final release of the Amazon WorkSpaces Chromebook client application\. Because [ Google is phasing out support for Chrome Apps](https://blog.chromium.org/2020/01/moving-forward-from-chrome-apps.html), there will be no further updates to the WorkSpaces Chromebook client application, and its use is unsupported\.


| Release | Date | Changes | 
| --- | --- | --- | 
|  2\.4\.13  | April 24, 2019 |  Fixed an issue that causes the app not to restore to full\-screen mode after a screen unlock  | 
|  2\.4\.12  |  |  Minor bug fixes  | 
|  2\.4\.11  |  |  Minor bug fixes  | 
|  2\.4\.10  |  |  Improves support for Japanese keyboard layouts  | 
|  2\.4\.8  |  |  Improves support for UK keyboards  | 
|  2\.4\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.6  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.5  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.4\.4  |  |  Minor improvements to session provision handling  | 
|  2\.4\.2  |  |  Resolves a bug with Caps Lock  | 
|  2\.4\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.2\.7  |  |  Resolves minor issues  | 
|  2\.2\.4  |  |  Localization enhancements  | 
|  2\.2\.1  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.1\.3  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  2\.0\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-android-client.html)  | 
|  1\.0  |  |  Initial release  | 