# WinUI3Preview3_Problems_FileOpenPicker

This repository contains two solutions with sample code demonstrating the FileOpenPicker in both UWP and WinUI3 Preview3.

In the UWP sample solution, the FileOpenPicker works as expected for both single file selection (PickSingleFileAsync) and the multiple files selection (PickMultipleFilesAsync).

However, the WinUI3 Preview 3 Desktop sample solution breaks on the multiple files selection and open (PickMultipleFilesAsync).

----

**Describe the bug**

The FileOpenPicker in WinUI3 Preview3 Desktop sample solution break and close the application when trying to open multiple items.

**Steps to reproduce the bug**

1. Clone the [WinUI3 Preview3 Problems FilePicker repository](https://github.com/eleanorleffler/WinUI3Preview3_Problems_FileOpenPicker). 
2. Go to the FilePickerWinUIPreview3 folder.
3. Open the FilePickerWinUIPreview3 solution in Visual Studio 2019 Preview.
4. Build and run with Debug x64.
5. Click the second / bottom button "FileOpenPicker: Multiple Files". (The first button should work as expected.)
6. Select one or more files.
7. Click "Open". Crash should occur.

**Expected behavior**

We expect the application to display the path of the selected file(s) or folder.

We expect the FileOpenPicker to allow the user to select multiple files as it does in UWP.

**Screenshots**

Screenshot#1 - Current Behavior (Error Message)

Screenshot#2 - Expected Behavior (File paths of selected files)

**Version Info**

NuGet package version: 

[Microsoft.VCRTForwarders.140 1.0.6]
[Microsoft.WinUI 3.0.0-preview3.201113.0]

Targeting:
Target: Universal Windows
Target version: Windows 10, version 1809 (10.0; Build 17763)
Min version: Windows 10, version 1803 (10.0; Build 17134)

Windows app type:
| UWP              | Win32            |
| :--------------- | :--------------- |
| 		Yes 	   |  				  |

| Windows 10 version                  | Saw the problem? |
| :--------------------------------- | :-------------------- |
| Insider Build (xxxxx)              | 						 |
| May 2020 Update (19041)            | 						 |
| November 2019 Update (18363)       | 						 |
| May 2019 Update (18362)            | 						 |
| October 2018 Update (17763)        | 			Yes			 |
| April 2018 Update (17134)          | 						 |
| Fall Creators Update (16299)       | 						 |
| Creators Update (15063)            | 						 |

| Device form factor | Saw the problem? |
| :----------------- | :--------------- |
| Desktop            | 		Yes			|
| Xbox               | 					|
| Surface Hub        | 					|
| IoT                | 					|

**Additional context**

We are unable to replicate this issue with the example code from Microsoft/WinUI-3-Demos, because it does not allow multiple selection.
