




Contents
Introduction:	3
Features:	4
Using ssWPI:	4
Loading Screen -	6
Mini installer	7
ssWPI’s Main Screen –	8
ssWPI Program Description - 	8
Category - 	10
Items - 	10
Title - 	10
Screenshot - 	10
Description - 	11
ssWPI Context Menu - 	11
Options Screen - 	15
Advanced Options Screen - 	17
Configuring ssWPI:	18
ssWPI_Options.ini -	18
Command Line Arguments -	19
Examples of Command Line options:	21
Quitting ssWPI:	22
Glossary of terms:	22


Introduction:

 
Figure 1

ssWPI v9 is a tool made by OS modders for OS modders, but is also simple enough for end users to use.  Its main function is to install a selection of applications and games silently.  ssWPI can categorize each item, display a screenshot and list a description making it easier to find the applications you want.  With the detailed information, you can see which applications and games you have available without needing to spend time looking over readme files or searching on the internet.

Optionally ssWPI can be used as a game launcher for any of your ppGames, while still retaining control so that you can quit a game at will, select a new game, and keep playing.  This is an especially convenient mode for children’s games, allowing them to easily switch to a new game.

The installation of applications from ssWPI is usually automated, and using SetupS technologies, ssWPI is able to sort your start menu, clean your desktop, tweak your settings and register your products.  With the ability to detect which OS you run it on, it will hide the applications that would not work if you tried to install them, including x86 and x64 detection.  It also checks to see which applications are already installed and hides them from the list of items you can install.  All these features are there to keep order on your PC, save you time, and make things easier to get your computer running the way you want, with the tools you need.

ssWPI can be used as either a Pre-Installer or a Post-Installer.  As a Pre-Installer, ssWPI can be run at the start of Windows XP/Vista /7 installs, allowing you to preselect the applications you want installed on the fresh OS before you actually begin the OS installation process.  By the time you get back from eating dinner your OS will be sitting on the desktop ready to go with all your choices installed and configured.  As a Post-Installer, it can be run from the DVD/USB anytime you need to install an application or game.
Features:

Load and Save Presets
Show a Screenshot of Applications and Games
Show Descriptions of Applications and Games
Hide Items detected as currently installed
Hide Items not intended for installing to the current OS
Countdown to Automatically load a default preset list of Items
Mini Installer to allow you to keep using your OS while installing
Color coded application types to quickly identify them
Quality Scaled Graphics for low or high screen resolution usage
Ability to specify additional stored application locations
Group all Items into self defined Categories
Theme-able Loader, Main screen, and Mini Installer
Auto Seek Items, scan all drives for Items to add
Create database of installable items for faster loading
Full Screen Mode or Windowed mode (F11 or Alt + Enter to switch between them)
Easy to integrate in unattended OS Mods


Using ssWPI:

ssWPI handles three basic types of applications, or items.  They are:

ssApps - Applications that install silently. i.e. no user interaction.
ppApps - permanent portable Applications.  Applications that are self contained.
ppGames - permanent portable Games.  Games that are self contained.

ssApps are pretty much what most people think of when they think of computer software applications.  They are installed on your HDD along with all the bells and whistles.  They tend to keep all their settings and preferences either in the system registry or some other system file so that once installed, they run only on that one machine until they are uninstalled and reinstalled on another machine.  The only difference in that and an ssApp, is that ssApps are designed to install silently.  Permanent portable Apps (ppApps), being portable, do not generally use the registry or system file locations, but rather keep all their personalization information in a file stored with the application itself.  This makes the application self contained and easy to move from one computer or OS to another.  They are best installed to a non-system partition/HDD allowing you to use them again even after a fresh OS installation.  Using SetupS technologies, ssWPI is able to create shortcuts and associate file types automatically even for these portable applications.  They are also designed to install silently.  Permanent portable Games (ppGames ) are games that are self contained in the same way as ppApps.  They do not require any other materials, such as a CD/DVD to be present in order to play the game.

ssWPI has default locations it searches for the various types of apps.  They are:

ssApps - X:\ssAppsInstalls 
ppApps - X:\ppAppsInstalls
ppGames - X:\ppGamesInstalls

Where X: is any valid drive on your system.  ssWPI will search every drive on your system looking for those folders and any app they might contain.  As you become more familiar with ssWPI, you will learn how to specify other locations that you wish ssWPI to search for apps.

ssWPI requires that you have an identification file stored with each of your items, either applications or games, in order for them to be detected and added to the list of possible installable items.  That file’s name is dependent on the type of item.  Those file names are:

ssApps - ssApp.app
ppApps - ppApp.app
ppGames - ppGame.ppg

A companion program of ssWPI, SetupS, works alongside ssWPI to do the actual installation of the apps using the information in these files.  These .app and .ppg files are created by the SetupS Builder or can be written in notepad or any text editor if you are comfortable doing so.  They contain summary information for each app including Title, Version, Description, and Install Path, among other information. You are also able to include an optional screenshot for ssWPI to display and an icon for use during installation. Through SetupS, for an individual app installation, you’re also able to go into the ssAppsInstalls/ppAppsInstalls/ppGamesInstalls folders and by double clicking, run the .app or .ppg file to install and integrate the app automatically.  Another method for installing the app is to use the Send To menu in the Windows Context Menu by right clicking on the app and selecting “Send To – SetupS”.  No matter which of the methods you choose, ssWPI, double clicking, or Send To, SetupS uses the information in the .app or .ppg files to install the apps of your choosing, extracting them if necessary from a compressed format, creates their shortcuts, associates file types and anything else you may need to do to keep your important applications set up and ready to go.  Regenerator is another included tool made to create the shortcuts and associate the file types for all your installed ppApps.  If you had previously installed them to a non-system partition/HDD, then by simply running this on a fresh OS you can have them all reintegrated into your new OS without needing to reinstall or extract them from a DVD/USB device.  This reduces install time and allows you to keep things as you like it.

It is important to remember that in order for all the available features of ssWPI to function correctly, such as being able to hide items under certain conditions or group them together with similar items, the ssApp.app/ppApp.app/ppGame.ppg file needs to contain the correct settings.  More information on the features of SetupS and Regenerator, along with details on making your applications and games function with ssWPI, is available in the SetupS Builder's Help file and Manual.

The general usage of ssWPI is mouse driven, although you are also able to use the keyboard to navigate and select your items and options.  You are able to type the name of an app at any time to quickly jump to it, if it is somewhere in the currently displayed list of items.  The purpose of ssWPI's main screen is to find, review, and select/deselect the items you wish to install on your OS.  This involves switching between categories, clicking on the items of interest, seeing the screenshot and description and choosing to select it for installation.  Once you are happy with the selection of applications, simply click the Start button.  If you are preselecting items before an OS install using the Command Line “ssWPI.exe –NewSetup”, it will store the selection in a file on your computer.  Running “ssWPI.exe -Install” any time after this initial selection will install those preselected apps for you without any interaction.  If you’re using ssWPI after the OS installation, when you press the Start button it will open up a Mini Installer window showing the progress of the installation of your selections, as shown in Figure 3.



Loading Screen -
The loading screen, also known as a splash screen, shown in Figure 2, is included as an indication that your OS is busy looking for applications/games.  If you are using the auto start Command Line “ssWPI.exe -AutoStartTimer=18", then you will also see a countdown timer, shown in Figure 7.  Once the timer reaches 0, ssWPI will load in a Default Preset (selection of items), if those items are present on your system, and exit.  That selection of items can be installed later using the Command Line “ssWPI.exe -Install”.

 
Figure 2


Mini installer

 
Figure 3 
Figure 3 shows the Mini Installer screen displaying a list of selected applications and the progress of installation.


ssWPI’s Main Screen –

 
Figure 4

ssWPI Program Description - 
The items that are selected are silently installed.
To install select the Items to install by marking the selection boxes.
    
Each Item that is checked will show its details in this description box.  ssApps, ppApps, and ppGames are determined by their Location and/or .app/.ppg file, and they are color-coded in the Items list.
White indicates an ssApps, yellow indicates a ppApps and green indicates a ppGames.
 
Figure 5
Right click the Items list for a menu that allows you to change Item selection and/or load/save a Preset.  Other options are available by clicking the Setup button.



The Hidden Items count includes Items that are not intended for the currently running Operating System.  ssWPI cannot detect all previously installed applications and therefore may not hide these applications from the Items list.

 
Figure 6
Category - 
This lists the Categories that are found inside the ssApp.app, ppApp.app and ppGame.ppg files.  Clicking them will only show items in that category.  The “All” category lists all available items depending on your options and current OS/Arch.  “Favorites” is a category available in the Game Launcher.  By right clicking a game you can toggle making it a favorite, which are shown in a different color than non favorites.  

Items - 
A list of available Items (applications or games) you can install, or play if you are in Game Launcher mode.  Clicking the name will show you the screenshot and description.  Clicking the Checkbox will select it for installation.  You are also able to use the arrow keys to navigate, and Space or Enter to select.

Title - 
This displays the title of the currently selected application.  It is displayed at the top right of the screen.  Clicking this will open the item’s URL in your browser if specified.

Screenshot - 
This is displayed in the right panel.  It is a graphic file of jpg format that is optionally included in each apps subfolder, alongside the ssApp.app/ppApp.app/ppGame.ppg.  There can also be another graphic file of png format that will display during installation of the app in the Mini Installer.

Description - 
Category: Example
Location: X:\ssAppsInstalls\SampleApp\ssApp.app (where x: is the drive of the installing application)
Install To: Destination Location.

The above is shown in the description box, followed by a description of the item as specified in the ssApp.app/ppApp.app/ppGame.ppg file.  This describes the application or game that is to be installed.

* Note:  Manually closing ssWPI’s Main Screen will cause ssWPI to close.  In other words, quit or abort.
ssWPI Context Menu - 
By right clicking on the left panel you are able to access the Context Menu as shown below:

 
Figure 7
 
Figure 8

Using the Context Menu (on the Item List) you are able to save or load a preset selection of Items, and pick from several hide/show options.  The context menu also has other tools to help with common tasks.

Select All	-Selects all the Items on the visible list.
Select None	-Un-Selects all the Items on the visible list.
Invert Selection 	-Un-Selects the Selected and Selects the Un-Selected Items on the visible list.

Select ssApps	 -Selects all the ssApps Items on the visible list.
Select ppApps	 -Selects all the ppApps Items on the visible list.
Select ppGames	-Selects all the ppGames Items on the visible list.

Un-Select ssApps	-Un-Selects all the ssApps Items on the visible list.
Un-Select ppApps	-Un-Selects all the ppApps Items on the visible list.
Un-Select ppGames	-Un-Selects all the ppGames Items on the visible list.

 
Figure 9

Hide ssApps	-Toggles hiding/showing ssApps Items on the visible list.
Hide ppApps 	-Toggles hiding/showing ppApps Items on the visible list.
Hide ppGames	-Toggles hiding/showing ppGames Items on the visible list.
Hide Local Items	-Toggles hiding/showing local Items on the visible list.
Hide Online items	-Toggles hiding/showing online Items on the visible list. 
Hide Installed	-Toggles hiding/showing Items that are already installed.
Hide Other OS	-Toggles hiding/showing Items that may not function with the current OS.
Hide OS-x86/x64	-Toggles hiding/showing Items that may not work on the current OS Platform.


 
Figure 10
Add items Location	-Browse for a location to scan extra Items.  Pick a folder that has ssApps, ppApps, or ppGames that you wish ssWPI to scan.
Sort List	-Toggles sorting the visible list alphabetically.
Load From Preset	-Browse for a Preset.ini file with a pre selected list of Items.
Save To Preset	-Save the current Item selections for later use.
Save Current List	-Generates a Text document with the Titles of visible Items.

(Re)Scan for Items	-ReScan all Item locations again.
Restart in Launcher	-Restart ssWPI in Game Launcher mode.
Mode

Update Current Options	-Save all Current ssWPI Options to ssWPI_Options.ini.
Generate Repository	-Scans all drives to create a list of all the applications and games.
Restart ssWPI	-Restarts ssWPI for all changes to settings to take effect.

 
Figure 11

Options Screen - 
The Options/Setup button opens up a window as shown in figure 11, with some important settings and options that you need to configure before selecting your applications.  The most important options are the ppGame Drive and ppApp Drive selection - where you wish to install your ppGames  and ppApps. (Default location for both is the system drive i.e. c:\ if none is selected.) and menu sorting method. The Drive selections only have to be done once per OS, as ssWPI will store the Drive information in the Windows folder.

Going from left to right:

ppGamesDrive	-Sets the Drive Location where ppGames will be installed.
ppAppsDrive	-Sets the Drive Location where ppApps will be installed.
Menu Sorting	-Choose between 3 sorting methods. (Kazz and LastOS and Windows Default)  

Group ppGames	-Combine all ppGames into one Games Category in addition to the assigned Category such as Puzzle or Arcade.
Hide Installed	-Toggles hiding/showing Items that are already installed.
Skip ssWPI path scan	-Make ssWPI NOT look in extra folders along ssWPI 's installation path for Items to list.
Show ppGames Parent	-Show the ppGames’ General Title for Multiple Game packs in Launcher mode.
Hide Other OS	-Toggles hiding/showing Items that may not function with the current OS.
Reboot PC	-Toggles Rebooting the PC after all applications are installed not advisable if installing Operating System.
Hide Splash	-Hide the Loading window while seeking Items.
Hide Local Items	-Hide the local Items.
Close On Complete	-Make ssWPI close after all selected Apps Items have been installed.
Hide Screenshot	-Toggles Displaying Screenshots as you click on a list item.
Hide Online	-Hide the online Items from the online repository.
Allow URL	-Allow Clicking the Title to open the URL of the Item in your Browser.
Use Remote DB	-Make ssWPI use a database file, ssWPI_Apps_DB.ini or ssWPI_Games_DB.ini, located with the Items on a remote or offline site.
Installer On Top	-Make the Mini installer the top most window during installation.
Full Screen	-Make ssWPI fill the entire screen (uncheck the box or press F11 or ALT + Enter to go back to window mode).
Hide OS-x86/x64	-Toggles hiding/showing Items that may not work on the current OS Platform.
Use Local DB	-Make ssWPI use a database file, ssWPI_Apps_DB.ini or ssWPI_Games_DB.ini, located with the Items, to store a summary of the scanned Items information to allow fast loading of ssWPI.
Sort Items	-Toggles sorting the visible list alphabetically.
Copy Apz to Repo	-Copy Apz to repository. 
Replace Existing 	-Replace Existing Apz/jpg from repository.
Apz/jpg
Download Items Only	- Download items from repository.
Launcher Starting	-Set the Starting Category for ssWPI Game Launcher to use.
Category
Load Preset	-Browse for a Preset.ini file with a pre selected list of Items.
Save Preset	-Save the current Item selections for later use.
Theme	-Choose a Theme for ssWPI.
 

Restart In Launcher 	-Restart ssWPI in Game Launcher mode.
Mode
Clear Added Locations	-Make ssWPI delete its list of Extra Locations and only look for Items in the "Standard" locations.  If there are currently no Extra Locations currently defined, then the button will be disabled.
Rescan Items	-Rescan all Item locations again.

Done	-Save Options to ssWPI_Options.ini and close the options window.  Any changes you make to the available options will be saved to ssWPI_Options.ini for future ssWPI sessions ONLY if “Done” is pressed.

Close Window 	-Option changes are instantly set for the current session, so closing the window will keep those choices.  However, future sessions of ssWPI will revert to the same settings that were used when the current session began.


 
Figure 12
Advanced Options Screen - 
If the ALT key is held while you push the Options/Setup button, the Advanced Options window is opened as shown in figure 11.  All the same options are available as before, but with the following additional options.

Skip ppGames	-Make ssWPI NOT look in folders named ppGamesInstalls for Items to list.
Skip ppApps	-Make ssWPI NOT look in folders named ppAppsInstalls for Items to list.
Skip ssApps	-Make ssWPI NOT look in folders named ssAppsInstalls for Items to list.

Hide Advanced Menu	-Hide certain Advanced Right-Click Options.
Sort Previously	-Tell SetupS that after installation of the selected apps, to Resort Previously Installed	  Installed Apps using the same Menu Sorting style.
	
Extra Locations For	-Optional paths for ssWPI to use to look for Items.  Separate Paths with "|".
Items
SetupS Arguments	-The desired Arguments for SetupS.  See the SetupS Manual for available options.
Auto Start Timer 	- Set the length of countdown in seconds before loading Default Preset.  After ssWPI does this, it will exit.  Setting this to -1 means Off.
Configuring ssWPI:

As well as offering the options button for changing what you can access, you can also set up ssWPI to start with these options preconfigured, or even fully exclude items (to reduce loading times).  The two methods of preconfiguring ssWPI are with the ssWPI_Options.ini file in the ssWPI application path, or via the Command Line Arguments you send when starting ssWPI.exe.

ssWPI_Options.ini -
* Setting an item to = Yes enables it on startup of ssWPI, setting to = No disables it.  Default is No.

Option	Description
AllowURL = Yes	Allow (Yes) or not (No) Clicking the Title to open the URL of the Item in your Browser.
AutoStartTimer = -1	Set the length of countdown in seconds before loading Default Preset.  After ssWPI does this, it will exit.  Setting this to -1 means Off.  Default is -1.
ClearAdded = No	(Yes) Make ssWPI delete its list of Extra Locations and only look for Items in the "Standard" locations.
ExtraLoc = Path1|Path2|etc	Optional paths for ssWPI to use to look for Items.  Separate Paths with "|".  Default is blank – "".
FullScreen = No	(Yes) Make ssWPI fill the entire screen (press F11 or ALT + Enter to go back to window mode).
GroupppGames = Yes	(Yes) Combine all ppGames into one Games Category in addition to the assigned Category such as Puzzle or Arcade.
HideAdvancedContextMenu = No	Hide (Yes) or Show (No) certain Advanced Right-Click Options.
HideInstalled = No	Hide (Yes) or Show (No) Items that are already installed.
HideOtherArch = Yes	Hide (Yes) or Show (No) Items that may not work on the current OS Platform (x86|x64).
HideOtherOS = No  	Hide (Yes) or Show (No) Items that may not function with the current OS.
HideScreenShots = No	Hide (Yes) or Show (No) Screenshots as you click on a listed Item.
HideSplash = No	Hide (Yes) or Show (No) the Loading window while seeking Apps.
InstallerOnTop = No	(Yes) Make the Mini installer the top most window during installation.
Launcher = No	(Yes) Set ssWPI to run as a ppGames Launcher, pressing Start will play the ppGame selected.
LauncherStartIn = All	Set the Starting Category for ssWPI ppGames Launcher to use.  Default is "All".
RebootPC = No	(Yes) Set the PC to Reboot after the Items have been installed.
SetupSArgs = -silent	The desired Arguments for SetupS.  See the SetupS Manual for avaiable options.
ShowppGamesParent = No	Show (Yes) or Hide (No) the ppGames’ General Title for Multiple Game packs in Launcher mode.
SkipBranchScan = No	(Yes) Make ssWPI NOT look in extra folders along ssWPI 's installation path for Items to list.
SkipCloseOnComplete = No	(Yes) Make ssWPI NOT close after all selected Apps Items have been installed.
SkipppApps = No	(Yes) Make ssWPI NOT look in folders named ppAppsInstalls for Items to list.
SkipppGames = No	(Yes) Make ssWPI NOT look in folders named ppGamesInstalls for Items to list.
SkipssApps = No	(Yes) Make ssWPI NOT look in folders named ssAppsInstalls for Items to list.
SortItems = Yes	(Yes) Sort the Items List Alphabetically.
SortPreviouslyInstalled = No	(Yes) Tell SetupS that after installation of the selected Apps, to Resort Previously Installed Apps using the same Menu Sorting style.
UseDBLocal = Yes	(Yes) Make ssWPI use a database file, ssWPI_Apps_DB.ini or ssWPI_Games_DB.ini, located with the Items, to store a summary of the scanned Items information to allow fast loading of ssWPI.


Command Line Arguments -
* Command Line options override ssWPI_Options.ini set options.  The options are not case sensitive.

Option 	Desciption
/?	Shows basic usage help.
-AllowURL	Allow Clicking the Title to open the URL of the Item in your Browser.
-DoNotAllowURL	Do Not Allow Clicking the Title to open the URL of the Item in your Browser.
-AutoStartTimer=	Set the length of countdown in seconds before loading Default Preset.  After ssWPI does this, it will exit.  Setting this to -1 means Off.
-ClearAdded	Make ssWPI delete its list of Extra Locations and only look for Items in the "Standard" locations.
-DoNotClearAdded	Leave any Extra Locations in place and look there for Items.
-ExtraLoc=	Optional paths for ssWPI to use to look for Items.  Separate Paths with "|".
-FullScreen	Make ssWPI fill the entire screen (press F11 or ALT + Enter to go back to window mode).
-NotFullScreen	Leave ssWPI in window mode.
-GroupppGames	Combine all ppGames into one Games Category in addition to the assigned Category such as Puzzle or Arcade.
-DoNotGroupppGames	Do not combine all ppGames into one Games Category, just leave them in their assigned Category such as Puzzle or Arcade.
-HideAdvancedContextMenu	Hide certain Advanced Right-Click Options.
-ShowAdvancedContextMenu	Show certain Advanced Right-Click Options.
-HideInstalled	Hide Items that are already installed.
-ShowInstalled	Show Items that are already installed.
-HideOtherArch	Hide Items that may not work on the current OS Platform (x86|x64).
-ShowOtherArch	Show Items that may not work on the current OS Platform (x86|x64).
-HideOtherOS	Hide Items that may not function with the current OS.
-ShowOtherOS	Show Items that may not function with the current OS.
-HideScreenShots	Hide Screenshots as you click on a listed Item.
-ShowScreenShots	Show Screenshots as you click on a listed Item.
-HideSplash	Hide the Loading window while seeking Items.
-ShowSplash	Show the Loading window while seeking Items.
-InstallerOnTop	Make the Mini installer the top most window during installation.
-NotInstallerOnTop	Do not force the Mini installer to be the top most window during installation.
-Launcher	Have ssWPI open set up to run as a ppGames Launcher, pressing Start will play the ppGame selected.
-NotLauncher	Set ssWPI to open in Installer mode.
-LauncherStartIn=	Set the Starting Category for ssWPI Game Launcher to use.
-RebootPC	Set the PC to Reboot after the Items have been installed.
-DoNotRebootPC	Do not set the PC to Reboot after the Items have been installed.
-SetupSArgs=	The desired Arguments for SetupS.  See the SetupS Manual for available options.
-ShowppGamesParent	Show the ppGames' General Title for Multiple Game packs in Launcher mode.
-HideppGamesParent	Hide the ppGames' General Title for Multiple Game packs in Launcher mode.
-SkipBranchScan	Make ssWPI NOT look in extra folders along ssWPI's installation path for Items to list.
-BranchScan	Make ssWPI look in extra folders along ssWPI's installation path for Items to list.
-SkipCloseOnComplete	Make ssWPI NOT close after all selected Apps Items have been installed.
-CloseOnComplete	Make ssWPI close after all selected Apps Items have been installed.
-SkipppApps	Make ssWPI NOT look in folders named ppAppsInstalls for Items to list.
-ppApps	Make ssWPI look in folders named ppAppsInstalls for Items to list.
 -SkipppGames	Make ssWPI NOT look in folders named ppGamesInstalls for Items to list.
-ppGames	Make ssWPI look in folders named ppGamesInstalls for Items to list.
-SkipssApps	Make ssWPI NOT look in folders named ssAppsInstalls for Items to list.
-ssApps	Make ssWPI look in folders named ssAppsInstalls for Items to list.
-SortItems	Sort the Items List Alphabetically.
-DoNotSortItems	Do not sort the Items List Alphabetically.
-SortPreviouslyInstalled	Tell SetupS that after installation of the selected apps, to Resort Previously Installed Apps using the same Menu Sorting style.
-DoNotSortPreviouslyInstalled	Tell SetupS that after installation of the selected apps, to NOT Resort Previously Installed Apps using the same Menu Sorting style.
-UseDBLocal	Make ssWPI use a database file, ssWPI_Apps_DB.ini or ssWPI_Games_DB.ini, located with the Items, to store a summary of the scanned Items information to allow fast loading of ssWPI.
-DoNotUseDBLocal	Do not use a database file, but only scan.
-x64	Makes ssWPI show the items made to run on an x64 OS.
-x86	Makes ssWPI show the items made to run on an x86 OS
-XP	Makes ssWPI show the items made for use on a Windows XP Machine.
-7	Makes ssWPI show the items made for use on a Windows 7 Machine.
-Vista	Makes ssWPI show the items made for use on a Windows Vista Machine.
-Install	Scans for applications, loads in Pre selected apps list and Installs them (uses Mini Installer screen).
-NewSetup	Allows manual selection of Pre Selected items for auto install after OS install completes (install with ssWPI.exe -Install).
-MenuSort=	Specifies your preferred menu sorting style.  Options are Kazz, LastOS, and Default – ie normal Windows.
Examples of Command Line options:
Example 1:
If the value stored in ssWPI_Options.ini file is:  AutoStartTimer=18, then:
When ssWPI is run it will start a countdown, as determined by the value of AutoStartTimer stored in the ssWPI_Options.ini file, then load in a Default Preset, compare that list with the files available on your system, store the list of valid files back out to “ssWPI.ini”, and exit ssWPI.  (Install with ssWPI.exe -Install)

In this case ssWPI will begin the process described above after 18 seconds as shown in Figure 7.
 
 
Figure 7
Example 2:
ssWPI  -AutoStartTimer=25

In this case ssWPI will begin the Auto Start process after 25 seconds since the command line argument will override what is set in ssWPI_Options.ini.

Example 3:

Before OS installation:
This should be placed in a startup sequence that is executed prior to installing an OS:

ssWPI -NewSetup

This will allow the selection of applications prior to the OS being installed but not install them until after the OS is installed when ssWPI -Install triggers the start.


After OS installation:
This should be placed in the scripts that are executed after the OS has finished installing:

ssWPI -Install

This will then install the preselected applications that were chosen prior to installation.
Quitting ssWPI:

If, while you are using ssWPI, you decide you need to just stop what you are doing and quit ssWPI, simply close the Main screen.  If you prefer, the ESC key will also cause ssWPI to close.




Glossary of terms:
Term	Definition
ssWPI	An application for doing silent installs and Launching ppGames.
x86	32 bit Architecture.
x64	64 bit Architecture.
Kazz	Kazz is a format for the start menu.
LastOS	LastOS is a format for the start menu.
SetupS	Setup Silent Applications.  An application to install the applications silently.
SetupS Builder	SetupS Builder is a separate application for the creation of SetupS applications for use with ssWPI.
ssApps	SetupS applications.  Applications that install silently. i.e. no user interaction.
ppApps	permanent portable Applications.  Applications that are self contained.
ppGames	permanent portable Games.  Games that are self contained.
Apps	An abbreviation for the word Applications.
OS	An abbreviation for Operating System.
Regenerator	permanent portable Applications Generator that will search your hard drives for ppApps and update the start menu with shortcuts and associate file types to the app.
Mods	Modified Windows Operating Systems that have customized themes and unattended installation of the OS.

