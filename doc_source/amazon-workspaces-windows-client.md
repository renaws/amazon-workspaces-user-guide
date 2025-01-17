# WorkSpaces Windows client application<a name="amazon-workspaces-windows-client"></a>

The following information will help you get started with the WorkSpaces Windows client application\.

**Topics**
+ [Requirements](#windows-requirements)
+ [Setup and installation](#windows_setup)
+ [Determine your client version](#determine-version-windows)
+ [Connect to your WorkSpace](#windows_connecting)
+ [Manage your login information \(3\.0\+ clients only\)](#manage-login-info-windows)
+ [Client views](#windows_views)
+ [Client language](#windows_client_lang)
+ [Display support](#windows-display-support)
+ [Proxy servers](#windows_proxy_server)
+ [Command shortcuts](#windows_shortcuts)
+ [Disconnect](#windows_disconnect)
+ [Clipboard support](#windows_clipboard_support)
+ [Manage hardware acceleration](#windows_hardware_acceleration)
+ [Release notes](#windows-release-notes)

## Requirements<a name="windows-requirements"></a>

The 4\.x client requires 64\-bit Microsoft Windows 8\.1 or Windows 10\.

The 3\.x client requires 32\-bit Microsoft Windows 7, Windows 8, or Windows 10\.

## Setup and installation<a name="windows_setup"></a>

Download and install the version of the client that you need as follows:


| To install\.\.\. | Do this | 
| --- | --- | 
| 4\.x client | Open [Amazon WorkSpaces Client Downloads](https://clients.amazonworkspaces.com/) and find the WorkSpaces Windows client\. Under Get the latest 64 bit client, choose the Download button\. | 
| 3\.x client | Open [Amazon WorkSpaces Client Downloads](https://clients.amazonworkspaces.com/) and find the WorkSpaces Windows client\. Under Get the latest 32\-bit client, choose the Download button\. | 
| 2\.5\.11 client | Open [Previous Versions](https://clients.amazonworkspaces.com/Versions.html)\. Find the WorkSpaces Windows client version and choose the Download button\. | 

You have two choices for how to install the Amazon WorkSpaces Windows client application: 
+ **Install just for you**\. If you choose this option and you share your local machine with other users, the WorkSpaces client application is available only to you\. If other users on the machine also want to use the WorkSpaces client application, they must install the application for their own use\. 
+ **Install for all users of this machine**\. If you choose this option, the WorkSpaces client application is available to anyone who logs on to the local machine, including those with Guest accounts\. 

Installing the WorkSpaces client application for all users requires you to have administrator privileges on your local machine\. Depending on how your local machine is configured, you might not have such privileges\. In that case, you can install the WorkSpaces client application just for yourself\. If you have questions about which option to choose, ask your WorkSpaces administrator for guidance\.

When installing the client 4\.0\+ version, you will have an option to install the USB redirection driver for features like USB mass storage device support\. Use the following procedure to install the USB redirection driver\.

**To install the USB redirection driver**

1. On the Amazon WorkSpaces Setup page, select **Install for all users of this machine**\. Choose **Next**\.  
![\[Selection of scope and folder\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/installation_1.png)

1. Select **Install driver for USB redirection** to enable the USB redirection features \(the default setting is not selected\)\. Choose **Install**\. You must have administrator privileges to install the driver\.  
![\[Selection of install driver for USB redirection\]](http://docs.aws.amazon.com/workspaces/latest/userguide/images/installer_string_draft2_box_checked.png)

1. To install the client with PCoIP USB redirection, enter and run the following command in an elevated command prompt\.

   ```
   msiexec.exe /i "[path to msi]" /qn INSTALL_USB="1" ALLUSERS="1"
   ```

   To install the client without PCoIP USB redirection, enter and run the following command in an elevated command prompt\.

   ```
   msiexec.exe /i "[path to msi]" /qn ALLUSERS="1"
   ```

If you're having trouble updating your WorkSpaces Windows client application to a newer version, use the following procedure to update your client application\.

**To update the WorkSpaces Windows client application to a newer version**

1. On your local machine, open the Windows search box and enter **registry editor** to open the Registry Editor \(regedit\.exe\)\.

1. When asked "Do you want to allow this app to make changes to your device?", choose **Yes**\.

1. In the Registry Editor, navigate to the following registry entry:

   **Computer\\HKEY\_CURRENT\_USER\\Software\\Amazon Web Services\. LLC\\Amazon WorkSpaces\\WinSparkle**

1. Delete the **SkipThisVersion** registry key\. When prompted to confirm the deletion, choose **Yes**, and then close the Registry Editor\.

1. If you have not already entered a registration code in the WorkSpaces Windows client application, do so, and then choose **Amazon WorkSpaces**, **Quit Amazon WorkSpaces** to close the client application\.

1. Restart the WorkSpaces Windows client application\. You should be prompted to update the client\. Accept the update\.

## Determine your client version<a name="determine-version-windows"></a>

To see which version of the WorkSpaces client you have, choose **Amazon WorkSpaces**, **About Amazon WorkSpaces**, or click the gear icon in the upper\-right corner and choose **About Amazon WorkSpaces**\.

## Connect to your WorkSpace<a name="windows_connecting"></a>

To connect to your WorkSpace, complete the following procedure\.

### To connect to your WorkSpace for 3\.0\+ clients<a name="windows_connecting-new-clients"></a>

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. To enter a different registration code, launch the client application, and then choose **Change Registration Code** at the bottom of the login page\.

1. Enter your user name and password in the login screen and choose **Sign In**\. If your WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your WorkSpaces administrator has not disabled the **Keep me logged in** feature, you can select the **Keep me logged in** check box at the bottom of the login screen to save your credentials securely so that you can connect to your WorkSpace easily while the client application remains running\. Your credentials are securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

### To connect to your WorkSpace for 1\.0\+ and 2\.0\+ clients<a name="windows_connecting-legacy-clients"></a>

1. The first time that you run the client application, you are prompted for your registration code, which is contained in your welcome email\. The WorkSpaces client application uses the registration code and user name to identify which WorkSpace to connect to\. When you launch the client application later, the same registration code is used\. To enter a different registration code, launch the client application, and then on the menu bar, choose **Options**, **Manage Registrations**\.

1. Enter your user name and password in the login screen and choose **Sign In**\. If your WorkSpaces administrator has enabled multi\-factor authentication for your organization's WorkSpaces, you are prompted for a passcode to complete your login\. Your WorkSpaces administrator will provide more information about how to obtain your passcode\.

1. If your WorkSpaces administrator has not disabled the "Remember Me" feature, you are prompted to save your credentials securely so that you can connect to your WorkSpace easily while the client application remains running\. Your credentials are securely cached up to the maximum lifetime of your Kerberos ticket\.

   After the client application connects to your WorkSpace, your WorkSpace desktop is displayed\.

An interruption of network connectivity causes an active session to be disconnected\. This can be caused by events such as closing the laptop lid, or the loss of your wireless network connection\. The WorkSpaces client application for Windows attempts to reconnect the session automatically if network connectivity is regained within a certain amount of time\. The default session resume timeout is 20 minutes, but this timeout can be modified by your network administrator\.

## Manage your login information \(3\.0\+ clients only\)<a name="manage-login-info-windows"></a>

You can view your registration code and what Region your WorkSpace is in\. You can specify whether you want the WorkSpaces client application to save your current registration code, and you can assign a name to your WorkSpace\. You can also specify if you want Amazon WorkSpaces to keep you logged in to a WorkSpace until you quit or your login period expires\.

**To manage your login information for a WorkSpace**

1. In the WorkSpaces client application, go to **Settings**, **Manage Login Information**\.

1. In the **Manage Login Information** dialog box, you can see the registration code and Region information for your WorkSpace\.

1. \(Optional\) If you want the WorkSpaces client to remember your current registration code, select the **Remember Registration Code** check box\.

1. Under **Saved registration codes**, select the WorkSpace that you want to name\.

1. In the **WorkSpace name** box, enter a name for the WorkSpace\.

1. \(Optional\) If you want WorkSpaces to keep you logged in until you quit or your login period expires, select the **Keep me logged in** check box\.

1. Choose **Save**\.

## Client views<a name="windows_views"></a>

You can switch to full screen mode by choosing **View**, **Enter Full Screen** \(3\.0\+ clients\) or **View**, **Show Fullscreen** \(1\.0\+ and 2\.0\+ clients\) in the client application menu\.

While in full screen mode, you can switch back to window mode by moving the pointer to the top of the screen\. The client application menu is displayed, and you can choose **View**, **Leave Full Screen** \(3\.0\+ clients\) or **View**, **Exit Fullscreen** \(1\.0\+ and 2\.0\+ clients\) in the client application menu\.

You can also toggle full screen mode by pressing Ctrl\+Alt\+Enter\.

## Client language<a name="windows_client_lang"></a>

You can select the language displayed by the client by performing the following steps\.

**Note**  
The WorkSpaces client applications support Japanese\. However, Japanese WorkSpaces are available only in the Asia Pacific \(Tokyo\) Region\.

**To select the client language**

1. Depending on which client you're using, do one of the following\.    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)

1. Enter your desired language in the **Select a language** list and choose **Save**\.

1. Restart the client\.

## Display support<a name="windows-display-support"></a>

WorkSpaces Value, Standard, Performance, Power, PowerPro, and GraphicsPro bundles support a maximum of four displays and a maximum resolution of 3840x2160 \(ultra\-high definition, or UHD\)\. The maximum supported resolution depends on the number of displays, as shown in the following table\.


| Displays | Resolution | 
| --- | --- | 
|  2  |  3840x2160  | 
|  4  |  1920x1200  | 

**Note**  
Graphics bundles support only a single monitor configuration with a maximum resolution of 2560x1600\.

The WorkSpaces client application extracts the Extended Display Information Data \(EDID\) of all attached displays and determines the best compatibility match before starting the session\. If you have a high pixel density \(high DPI\) display, the client application automatically scales the streaming window according to your local DPI settings\. For better maximum resolution with high DPI displays, see [WorkSpaces high DPI display support](high_dpi_support.md)\. 

**To use multiple monitors with WorkSpaces**
**Note**  
Multiple monitors aren't currently supported on Linux WorkSpaces using the WorkSpaces Streaming Protocol \(WSP\)\.

1. Configure your local machine to use multiple monitors\. For more information, see [ How to use multiple monitors in Windows 10](https://support.microsoft.com/windows/how-to-use-multiple-monitors-in-windows-10-329c6962-5a4d-b481-7baa-bec9671f728a) in the Microsoft documentation\. 

1. Start the WorkSpaces client application and log in to your WorkSpace\.

1. Depending on which client you're using, do one of the following:    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)

Your WorkSpace should now be extended across your displays\. Whichever display you have designated as your primary display is also the primary display in WorkSpaces when you enter full screen mode\.

**Note**  
Using full screen mode on only some of the displays in a multiple monitor setup isn't possible\. You can, however, press the Windows logo key \+ Up Arrow or use the maximize button in the upper\-right corner of the WorkSpaces window to maximize the WorkSpaces client window on a display without extending the WorkSpace to the other displays\.

## Proxy servers<a name="windows_proxy_server"></a>

If your network requires you to use a proxy server to access the internet, you can enable your WorkSpaces client application to use a proxy for HTTPS \(port 443\) traffic\. The WorkSpaces client applications use the HTTPS port for updates, registration, and authentication\. 

**Note**  
The desktop streaming connections to the WorkSpace require ports 4172 and 4195 to be enabled, and do not go through the proxy server\. 
Proxy servers that require authentication with a username and password are not supported\.

### To control the proxy server for 3\.0\+ clients<a name="windows_proxy_server-new-clients"></a>

By default, the 3\.0\+ Windows clients use the proxy server that's specified in the device operating system settings\. The first time the client is launched, the device operating system proxy server setting is used\. If you select another option for the proxy server, that setting is used for subsequent launches of the client\. If a proxy server is specified at both the operating system level and in the WorkSpaces client, the client setting is used\.

Starting with version 3\.0\.12 of the Windows client, you can also choose not to use a proxy server\.

**Note**  
In versions 3\.0\.0 through 3\.0\.11, if you specify a custom proxy server, a "No network" error might appear when you attempt to log in to your WorkSpace\. If you want to use a custom proxy server with the Windows client, we recommend upgrading to the latest version\.

1. In the WorkSpaces client application, go to **Settings**, **Manage Proxy Server**\.

1. In the **Set Proxy** dialog box, select the appropriate options, depending on which version of the 3\.0\+ client you have\.
   + **Windows client version 3\.1\.3 or later** — To disable usage of a proxy server, select **Don't use proxy server**\. If you select **Don't use proxy server**, no proxy server is used when you access the internet\.

     To use a proxy server, choose one of the following options, and then choose **Save**:
     + **Use your device operating system settings** — This option uses the proxy server settings for your operating system\.
     + **Customize proxy server for WorkSpaces** — Enter the URL or IP address and the port for your custom proxy server\.
   + **Windows client versions 3\.0\.12, 3\.1\.0, and 3\.1\.2** — To enable or disable usage of a proxy server, select or deselect **Use proxy server**\. If you deselect **Use proxy server**, no proxy server is used when you access the internet\.

     If you've selected **Use proxy server**, choose one of the following options, and then choose **Save**:
     + **Use your device operating system settings** — This option uses the proxy server settings for your operating system\.
     + **Customize proxy server for WorkSpaces** — Enter the URL or IP address and the port for your custom proxy server\.
   + **Windows client version 3\.0\.11 or earlier** — By default, these versions of the client use the proxy server specified in the device operating system settings\. To use a custom proxy server, choose **Use proxy server**, enter the URL or IP address and the port for the proxy server, and then choose **Save**\.

### To use a proxy server for 1\.0\+ and 2\.0\+ clients<a name="windows_proxy_server-legacy-clients"></a>

By default, the 1\.0\+ and 2\.0\+ Windows clients don't use a proxy server\. To specify a proxy server, use the following procedure\.

1. In the WorkSpaces client application, open the **Advanced Settings** dialog box\.

1. In the **Proxy Server Setting** area, select **Use Proxy Server**, enter the proxy server URL or IP address and the port, and choose **Save**\.

## Command shortcuts<a name="windows_shortcuts"></a>

The WorkSpaces Windows client supports the following command shortcuts:
+ Ctrl\+Alt\+Enter—Toggle full screen display
+ Ctrl\+Alt\+F12—Disconnect session

## Disconnect<a name="windows_disconnect"></a>

To disconnect the Windows client application, you have several options: 
+ In the Amazon WorkSpaces client application, go to **Amazon WorkSpaces**, and then choose **Disconnect WorkSpace**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.
+ In the Amazon WorkSpaces client application, go to **Amazon WorkSpaces**, and then choose **Quit Amazon WorkSpaces**\. Your WorkSpace session ends, and the client application closes\.
+ In the Amazon WorkSpaces client application, close the WorkSpaces client window by clicking the close \(X\) button in the upper\-right corner\. In the **End Session** dialog box, choose **Yes**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.
+ You can also log off of the WorkSpace\. In the Amazon WorkSpaces client application, go to **View**, and then choose **Send Ctrl\+Alt\+Delete**\. Choose **Sign Out**\. Your WorkSpace session ends, but the client application continues running in case you want to log in again\.

## Clipboard support<a name="windows_clipboard_support"></a>

The clipboard supports a maximum uncompressed object size of 20 MB\. For more information, see [I'm having trouble copying and pasting](client_troubleshooting.md#copy_paste)\.

**Note**  
When copying from a Microsoft Office app, the clipboard only contains the last copied item, and the item is converted into standard format\. If you copy content larger than 890 KB from a Microsoft Office app, the app might become slow or unresponsive for up to 5 seconds\. 

## Manage hardware acceleration<a name="windows_hardware_acceleration"></a>

Starting with version 3\.1\.4, hardware acceleration is disabled by default when you're using the Amazon WorkSpaces Windows client application\.

**Note**  
If you plan to upgrade to version 3\.1\.4, and if you've disabled hardware acceleration for version 3\.1\.3 or earlier by using the [procedure described later in this section](#hardware_acceleration_313), make sure that you re\-enable hardware acceleration in Windows by setting the **DisableHWAcceleration** registry key to **0**\. Then you can upgrade to version 3\.1\.4 or later of the WorkSpaces Windows client application\.

We recommend that you leave hardware acceleration disabled in the Windows client\. However, if you're experiencing high CPU usage or slower performance when using the client, you might want to enable hardware acceleration in the client\.

**Note**  
If you enable hardware acceleration in the Windows client, the following issues might occur with a few video driver versions:  
The screen might have flickering black boxes in some places\.
The screen might not properly update on the WorkSpaces login page, or it might not properly update after you log in to your WorkSpace\. You might see artifacts on the screen\.
Your mouse clicks might not be lined up with the cursor position on the screen\.

### To enable hardware acceleration in version 3\.1\.5 or later of the Windows client<a name="hardware_acceleration_315"></a>

1. Choose **Settings**, **Manage Hardware Acceleration**\.

1. In the **Manage Hardware Acceleration** dialog box, select **Enable Hardware Acceleration for Amazon WorkSpaces**, and then choose **Save**\. 

1. For this change to take effect, choose **Amazon WorkSpaces**, **Quit Amazon WorkSpaces** to close the Windows client application\.

1. Restart the WorkSpaces Windows client application\. Hardware acceleration should now be enabled\.

   After you've enabled hardware acceleration in the Windows client, if the screen and mouse issues described earlier occur, clear the **Enable Hardware Acceleration for Amazon WorkSpaces** check box to disable hardware acceleration, and then restart the Windows client application\.

WorkSpaces administrators can enable hardware acceleration in version 3\.1\.4 or later of the WorkSpaces Windows client by using the following commands in a Command Prompt or PowerShell window\.

1. Use the following command to check for the **EnableHwAcc** registry key\.

   ```
   reg query "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc
   ```

1. Use the following command to add the **EnableHwAcc** registry key\.

   ```
   reg add "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc
   ```

   This registry setting takes effect after the WorkSpaces Windows client is closed and restarted\.

If needed, use the following command to delete the **EnableHwAcc** registry key\.

```
reg delete "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc /f
```

This registry setting takes effect after the WorkSpaces Windows client is closed and restarted\. 

### To enable hardware acceleration in version 3\.1\.4 of the Windows client<a name="hardware_acceleration_314"></a>

1. On your Windows computer \(not your WorkSpace\), open the Windows search box, and enter **registry editor** to open the Registry Editor \(regedit\.exe\)\. Choose **Run as administrator**\. \(If you don't have permission to run the Registry Editor as an administrator, contact your system administrator for assistance\.\)

1. When asked "Do you want to allow this app to make changes to your device?", choose **Yes**\. 

1. In the Registry Editor, navigate to the following registry entry:

   **HKEY\_CURRENT\_USER\\SOFTWARE\\Amazon Web Services\. LLC\\Amazon WorkSpaces**

1. Select **Amazon WorkSpaces**, and then choose **Edit** > **New** > **String Value**\.

1. For the registry key name, enter **EnableHwAcc**\.

1. Close the Registry Editor\.

1. Close and restart the WorkSpaces client application\. 

   After you've enabled hardware acceleration in the Windows client, if the screen and mouse issues described earlier occur, delete the **EnableHwAcc** registry key to disable hardware acceleration, and then restart the Windows client application\.

WorkSpaces administrators can enable hardware acceleration in version 3\.1\.4 or later of the WorkSpaces Windows client by using the following commands in a Command Prompt or PowerShell window\.

1. Use the following command to check for the **EnableHwAcc** registry key\.

   ```
   reg query "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc
   ```

1. Use the following command to add the **EnableHwAcc** registry key\.

   ```
   reg add "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc
   ```

   This registry setting takes effect after the WorkSpaces Windows client is closed and restarted\.

If needed, use the following command to delete the **EnableHwAcc** registry key\.

```
reg delete "HKCU\SOFTWARE\Amazon Web Services. LLC\Amazon WorkSpaces" /v EnableHwAcc /f
```

This registry setting takes effect after the WorkSpaces Windows client is closed and restarted\. 

### To disable hardware acceleration in version 3\.1\.3 or earlier of the Windows client<a name="hardware_acceleration_313"></a>

If you need to use version 3\.1\.3 or earlier of the Windows client application, you can disable hardware acceleration in Windows through the Windows registry\. Disabling hardware acceleration in Windows might affect the performance of other Windows applications\.

1. On your Windows computer \(not your WorkSpace\), open the Windows search box, and enter **registry editor** to open the Registry Editor \(regedit\.exe\)\. Choose **Run as administrator**\. \(If you don't have permission to run the Registry Editor as an administrator, contact your system administrator for assistance\.\)

1. When asked "Do you want to allow this app to make changes to your device?", choose **Yes**\. 

1. In the Registry Editor, navigate to the following registry entry:

   **HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Avalon\.Graphics**

1. Do one of the following:
   + If the **DisableHWAcceleration** registry key exists, select it and choose **Edit** > **Modify**\. In the **Value data** box, enter **1** \(to disable hardware acceleration\), and then choose **OK**\. 
   + If the **DisableHWAcceleration** registry key doesn't exist, do the following:

     1. Select **Avalon\.Graphics**, and then choose **Edit** > **New** > **DWORD \(32\-bit\) Value**\.

     1. For the registry key name, enter **DisableHWAcceleration**\.

     1. Select the new **DisableHWAcceleration** key, and then choose **Edit** > **Modify**\. 

     1. In the **Value data** box, enter **1** \(to disable hardware acceleration\), set **Base** to **Hexadecimal**, and then choose **OK**\. 

1. Close the Registry Editor\.

1. Close and restart the WorkSpaces client application\. 

**Note**  
If you need to enable hardware acceleration to improve the performance of other Windows applications, set the **DisableHWAcceleration** key to **0**\.

## Release notes<a name="windows-release-notes"></a>

The following table describes the changes to each release of the Windows client application\.


| Release | Date | Changes | 
| --- | --- | --- | 
| 4\.0\.2 | September 1, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 4\.0\.1 | July 30, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 4\.0\.0 | June 30, 2021 | The first 64\-bit release of the Windows client application\. | 
| 3\.1\.10 | August 5, 2021 | Minor bug fixes and enhancements\. | 
| 3\.1\.9 | June 29, 2021 | Minor bug fixes and enhancements\. | 
| 3\.1\.8 | May 28, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.7 | April 29, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.6 | April 8, 2021 |  Fixes for disconnects and crashes resulting from WorkSpaces Streaming Protocol \(WSP\) audio traffic optimization  | 
| 3\.1\.5 | April 2, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.4 | March 16, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.3 | February 15, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.2 | January 8, 2021 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.1\.1 | December 1, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  Version 3\.1\.1 is available only in the AWS GovCloud \(US\-West\) Region\.   | 
| 3\.1\.0 | December 1, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.0\.12 | November 10, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.0\.11 | October 02, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.0\.10 | September 16, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
| 3\.0\.9 | August 14, 2020 |  Minor bug fixes and enhancements  | 
| 3\.0\.8 | July 30, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  3\.0\.7  | June 3, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  3\.0\.6  | April 28, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  3\.0\.5  | March 30, 2020 |  Resolves an issue with the user interface displaying a login prompt if single sign\-on \(SSO\) is enabled for Amazon WorkDocs  | 
|  3\.0\.4  | March 3, 2020 |  Minor bug fixes and enhancements  | 
|  3\.0\.2  | February 14, 2020 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  3\.0\.0  | November 25, 2019 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.11  | November 4, 2019 |  Minor bug fixes  | 
|  2\.5\.10  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.9  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.8  |  |  Resolves an intermittent crashing issue related to computer waking up when opening a laptop lid  | 
|  2\.5\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.6  |  |  Minor fixes  | 
|  2\.5\.5  |  |  Minor fixes  | 
|  2\.5\.2  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.1  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.5\.0  |  |  Adds support for user self\-service WorkSpace management capabilities  | 
|  2\.4\.10  |  |  Minor fixes  | 
|  2\.4\.9  |  |  Minor fixes  | 
|  2\.4\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.4\.7  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.4\.6  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.4\.5  |  |  Adds a check to ensure that certificates issued by Amazon Trust Services are trusted by Windows during installation\. By default, an up\-to\-date Windows local Root CA list includes Starfield Service Root Certificate Authority \- G2, and therefore trusts Amazon Trust Services certificates\. If the local Root CA list is outdated, the client installer installs the Starfield Service Root Certificate Authority \- G2 certificate to the system\. If you do not have administrator access to the client device, you'll be prompted to confirm the installation of the Root CA certificate\.  | 
|  2\.4\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.4\.2  |  |  Minor fixes  | 
|  2\.4\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.3\.7  |  |  Addresses a gray screen issue that occurs when displays are in different orientations  | 
|  2\.3\.6  |  |  Localization enhancements  | 
|  2\.3\.5  |  |  Minor improvements  | 
|  2\.3\.3  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.3\.2  |  |  Installer fixes  | 
|  2\.3\.1  |  |  Minor fixes  | 
|  2\.3\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.2\.3  |  |  Resolves minor bugs and improves stability  | 
|  2\.2\.1  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.1\.3  |  |  Closing the client expires the reconnect token\. You can easily reconnect to your WorkSpace as long as the client is running\.  | 
|  2\.1\.1  |  |  Minor improvement to protocol handling  | 
|  2\.1\.0  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.0\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  2\.0\.6  |  |  Resolves bugs and includes other improvements  | 
|  2\.0\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  1\.1\.80  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  1\.1\.6  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  1\.1\.4  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  1\.0\.8  |  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/workspaces/latest/userguide/amazon-workspaces-windows-client.html)  | 
|  1\.0  |  |  Initial release  | 