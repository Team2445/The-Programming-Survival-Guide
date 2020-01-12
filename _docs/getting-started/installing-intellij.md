---
title: Installing IntelliJ
category: Getting Started
order: 3
---
## Installation  
1. Double Click on the `ideaIC-2019.3.1.exe` file to begin the IntelliJ IDEA installation  
2. Go through the installer, accepting all defaults, 
3. Once the installation is complete, check the **Run IntelliJ Community Edition Box** and then click Finish  
4. You should see the following image once complete. If you made it this far, press **OK**  
![step 1](../../images/intellij/step1.PNG)
> Make sure it looks like the image.  

## IntelliJ First Run  
1. The JetBrains Privacy Policy Window will appear, read through the agreement and check the **I confirm that I have read and accept the terms of this User Agreement**  and then click Continue  
2. On the Data Sharing Window, Click **Don't Send**  
3. Select the Theme that you would like to use (Darcula prefered), click **Next: Default plugins**  
### Default Plugin Configuration  
  ![step 2](../../images/intellij/step2.PNG)  

1. Hit **Disable** on **Android**, **Swing**, and **Plugin Development**
2. Configure the plugins below. Once complete, click **Next: Featured Plugins**  

#### Version Controls  
1. Click on **Customize**  
2. Uncheck **Mercurial** and **Subversion**  
3. Click on **Save Changes and Go Back**  

![version control](../../images/intellij/version-control.PNG)  

#### Test Tools  
1. Click on **Customize**  
2. Uncheck **TestNG** and **Coverage**  
3. Click on **Save Changes and Go Back**  

![test](../../images/intellij/Testing.PNG)  

### Featured Plugins  
Do not install any plugins and click Start IntelliJ Idea  

## IntelliJ Configuration  
![plugins](../../images/intellij/Plugins.PNG)  
1. On the Welcome to IntelliJ IDEA page, click on the **Configure Gear**, and then select **Plugins**  
2. On the Plugins Window, Ensure Marketplace is selected, and type **FRC** into the Search bar  
3. Click the **Install** button next to the FRC Plugin  
4. On the Third-party Plugins Privacy Notice window, click **Accept**  
5. Once installed, do not click Restart  
6. Search for **Save Actions** and install the plugin  
7. Click **Ok** on the Plugins Window  

## Code Style Setup  
1. Download the 2445 Code Style XML file [**Right Click This Link**](https://gist.githubusercontent.com/lukemcd9/10fd4cd23724a5355fbfa8bfeff316bb/raw/f3c5767245463530177798871c4104df068ea1e2/frc-2445-code-style.xml) (right click link, Save As) to your desktop  
2. Click on the **Configure Gear**, then select **Settings**
3. On the left Window, Select **Editor**
4. In the Editor settings page, click on **Code Style**  

![code style](../../images/intellij/code-style.PNG)  
1. Next to the Scheme: Default IDE Dropdown, click on the **Gear** icon  
2. Hover over **Import Scheme** and click on **IntelliJ IDEA code style XML**  
![import](../../images/intellij/import.png)  
3. Navigate to the file that you just downloaded and click **OK**  
4. Click **OK** on the Import Scheme window  
5. Click **OK** on the settings window to close it  
6. Restart IntelliJ by closing the program and opening it back up again  

## FRC Plugin Setup  
1. Click on Configure FRC Team Number and put in our team number

## Save Actions Setup  
1. Open IntelliJ and Click On Settings  
2. On the left side of the Window, Select Save Actions  
3. Check the Activate save actions on shortcut  
3. Under the Formatting actions heading, check Optimize imports and Reformat only changed code  
5. On the left side of the Window, Select Keymap  
6. Click the right arrow next to Plug-ins  
7. Click the right arrow next to Save Actions  
8. Right click on Execute Save Actions on Shortcut and select remove Ctrl Shift S  
9. Right click on Execute Save Actions on Shortcut and select Add Keyboard Shortcut  
10. Change the keystroke to Ctrl S  
11. On the Warning box, select **Leave**  
12. Click OK  



