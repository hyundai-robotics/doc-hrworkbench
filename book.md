
[__SOURCE](README.md)
# ${cont_model} Controller Function Manual - HRWorkBench

[__SOURCE](0-about-this-manual/README.md)
# About the Manual

[__SOURCE](0-about-this-manual/precautions.md)
# Precautions

{% include file="en/precautions.md" %}

[__SOURCE](0-about-this-manual/safety-notice.md)
# Safety Cautions

{% include file="en/safety-notice.md" %}

{% hint style="danger" %}
During the execution of a user script, logic errors or unmet execution conditions may cause unexpected robot behavior, potentially resulting in serious injury or death.
{% endhint %}

[__SOURCE](1-preface/README.md)
# 1. Overview


[__SOURCE](1-preface/1-intro.md)
## 1.1 Introduction to HRWorkBench

HRWorkBench is a Windows PC software designed for supporting the teaching of the ${cont_model} controller of HD Hyundai Robotics.  HRWorkBench supports the following functions of the ${cont_model} controller when connected through Ethernet communication.
(This is the successor product of the HRView, HRHistoryViewer software used in the Hi5a controller.)

| Category | Description |
|---|---|
| Back up and restore files | You can back up the entire project folder and the entire log folder to the PC and restore it back to the controller. |
| Manage the job files | You can check the list of jobs in the controller and copy or delete some job files in both the PC and controller. |
|Edit the job files|You can open and edit a job file in the controller by double-clicking it. Syntax coloring and smart indent functions are supported for readable editing.|
|Check the syntax of job files|You can remotely carry out a basic syntax check of job files before executing them.|
|Monitor the  global variables, and edit their values|You can monitor the values of all global variables and modify the value of the targeted variables or delete targeted variables.|
|Execute the Robot Language|You can remotely execute an assignment statement of a job file. There is no support for the move statement or flow control statement.|
|Monitor, check logs in the controller|You can monitor the logs of errors, warnings, etc. that have occurred in the remote controller. And you can check the logs of the project you backed up to the PC.|
|Check the scope logs|Load and draw the data waveform of the scope log that generated on critical error as a robot collision. You can also export the data waveform to a .csv file.|
|Verify and Port Settings|You can apply some of a controller's settings or variables to another controller in the same way.|


{% hint style="warning" %}
This program allows you to remotely change the job program or variable value, so it may affect the robot's operation. You are required to read this manual and use the program carefully while paying sufficient attention!
{% endhint %}

* HRWorkBench can be downloaded from the `Download center` page under `Customer Support` on the HD Hyundai Robotics website(https://www.hd-hyundairobotics.com/en/main).

[__SOURCE](1-preface/2-install-exec.md)
## 1.2 Install and Execute HRWorkBench

Run the installer.

![](../_assets/preface/installer1.png)


Proceed with selecting the installation details, such as the installation location, etc., and click Next. Finally, click the Install button when you agree to the license.

![](../_assets/preface/installer2.png)
![](../_assets/preface/installer3.png)

Click the Finish button to end the installer once the installation is completed.

![](../_assets/preface/installer4.png)


Execute the application by clicking the Windows `Start` button and then select HRWorkBench from the `Recently Added App` or the `HHI Robotics Group`.

![](../_assets/preface/exec-icon.png)

[__SOURCE](1-preface/3-ui.md)
## 1.3 Configuration of the User Interface for HRWorkBench

The figure below shows the names of the user interface elements of the HRWorkBench.
Each function will be described in the order according to the operation sequence.

![](../_assets/preface/ui1.png)


The elements of the user interface can be rearranged into a layout convenient for the work.
Dragging the toolbar's left edge or dragging the title bar of each window will allow you to detach the toolbar or a window while it is in docking state or attach it back into the docking state. When in the docking state, the windows can be arranged side by side, or they can be stacked into a page from which you can select one using a tab.


<div style="display: flex; gap: 20px;">
  <img src="../_assets/preface/ui2.png" width="20%">
  <img src="../_assets/preface/ui3.png" width="80%">
</div>

You can change the user interface language by selecting 'Help - Change Language'. After select the language, restart the HRWorkBench application.

![](../_assets/preface/ui4.png)

[__SOURCE](2-setting/README.md)
# 2. Basic Settings


[__SOURCE](2-setting/1-ethernet.md)
# 2.1 Connect to Ethernet

HRWorkBench and the ${cont_model} robot controller should be connected to the same Ethernet network.
Suppose there are two ${cont_model} controllers that need to be connected, and let us assume that their individual IP addresses are 192.168.1.150 and 192.168.1.151. Moreover, the IP address of the PC is 192.168.1.100. (The devices connected to each other through a hub should all be in the same subnetwork, 192.168.1.XXX.)

The IP Address Manager dialog box will be opened, as shown below, when you select `Comm - Address Manager` in the main menu of HRWorkBench or click the tool   button.
A new input line will be added each time you click the `Append` button. After adding two lines, you need to input the name and IP address, as shown in the figure below.
You can also adjust the order of the current lines by moving them up and down using the `Up` and `Down` buttons.

![](../_assets/setting/addrmng.png)


Now, when you open the IP address combo box in the Comm. window, you can select the two IP addresses that are already inputted.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/comm/cb-ipaddr.png" width="30%" height="30%">
  <img src="../_assets/comm//bt-connect.png" width="50%">
</div>

When you press the `Connect` button, and the button turns yellow, you are now connected.
If you are successfully connected, the Robot Controller node will appear in the Explore window on the left. Right-click the node and then click Display RC Info. in the pop-up menu. The software version of the ${cont_model} controller will be received and displayed, as shown below.



<div style="display: flex; gap: 20px;">
  <img src="../_assets/explorer/pmenu-rc-info.png" width="55%" height="55%">
  <img src="../_assets/explorer/dlg-rc-info.png" width="30%">
</div>

[__SOURCE](2-setting/2-pc-path.md)
# 2.2 Select the PC Path

When backing up or editing the files of the robot controller, you need to copy the files to the PC. To do this, you should designate the path of the folder on the PC side. This path is called the `current PC home path` or `PC path` when shortened. The PC path can be specified in the following ways;

### Way 1

In Windows Explorer, drag the icon in the folder with the left mouse button and drop it over the communication window.

![](../_assets/pcpath/pcpath1.png)
![](../_assets/pcpath/pcpath2.png)


The designated PC path will be displayed in the Comm. window. Then, the files copied to the PC will be saved in this folder.
 
![](../_assets/pcpath/pcpath3.png)

When you manage multiple robot controllers in different PC folders, you can perform tasks by changing between folders and dragging and dropping them.
If you click the <img src="../_assets/pcpath/bt-folder.png"> button on the right side of the displayed path, the path will be opened in Windows Explorer.


### Way 2

Clicking the <img src="../_assets/pcpath/bt-dot3.png"> button on the right opens the Select Folder dialog. After selecting a folder, click the `[Select Folder]` button to enter the path.

![](../_assets/pcpath/pcpath3.png)


### Way 3

Right-click the PC node in the explorer pane to open the pop-up menu and select `Set PC Backup path`, and a dialog box opens. Type the path in the dialog box or copy/paste the path in Windows Explorer, and click the `OK` button.

![](../_assets/pcpath/pcpath4.png)
![](../_assets/pcpath/pcpath5.png)


The folders in the PC path is structured, as shown in the figure below.
Jobs that have been backed up before in the PC path will be displayed under the PC node of the Explore window, as shown in the figure below.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/pcpath/pcpath10.png" width="55%" height="55%">
  <img src="../_assets/pcpath/pcpath11.png" width="40%">
</div>

[__SOURCE](2-setting/3-hrwb-file.md)
# 2.3 Save and Load WorkBench Files

You can save and load working environment settings as a WorkBench file with the extension `.hrwb`.
The following items will be saved.

*	List created in the IP address manager
*	PC path setting


Let us save a WorkBench file. After performing the basic settings, select `File - Save Workbench` in the main menu. Select the desired path, input the file name, and then click the Save button.

![](../_assets/file/wbfile-save.png)


Let us load a WorkBench file. Exit the HRWorkBench application and execute it again. Select `File - Open WorkBench` in the main menu. If you select the saved file, you can see that the existing settings are restored.

![](../_assets/file/wbfile-open.png)


The recently loaded paths and file names will be listed in File in the main menu, so you can quickly open a file by clicking it.

![](../_assets/file/wbfile-list.png)

Another way to load WorkBench files is by opening an `.hrwb` file by dragging and dropping its icon from Windows Explorer.

![](../_assets/file/drag-drop-hrwb.png)

[__SOURCE](3-backup-restore/README.md)
# 3. Backup and Restore


[__SOURCE](3-backup-restore/1-backup-restore.md)
# 3.1 Back Up and Restore Files

You can back up or restore the files in the ${cont_model} controller.
First, press the `Connect` button to remotely connect to the controller. In the Explore window, open a pop-up menu for the `Robot Controller` node by right-clicking it, and then select `Backup all to PC`. The `Backup` dialog box will appear.


<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/backup1.png" width="40%" height="40%">
  <img src="../_assets/backup/backup2.png" width="50%">
</div>

Press the `Start` button after checking the target that needs to be backed up. The files in the controller will be backed up to the PC path. The Completed dialog box will be displayed once the backup is finished, and the file list under the PC node in the Explore window will be updated.
 
![](../_assets/backup/backup3.png)


The method for restoration is similar to this.
In the Explore window, open a pop-up menu for the `Robot Controller` node by right-clicking it, and then select `Restore all to Robot Controller.` The Restore dialog box will appear.


<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/restore1.png" width="40%" height="40%">
  <img src="../_assets/backup/restore2.png" width="50%">
</div>


Press the `Start` button after checking the target that needs to be restored. The files in the controller will be restored to the PC path, and the Completed dialog box will be displayed.

{% hint style="warning" %}
When performing the restore, the ${cont_model} controller must be in the motor-off state. When performed in the motor-on state, a 'impossible' message is output
{% endhint %}

[__SOURCE](3-backup-restore/2-job-copy-del.md)
# 3.2 Copy and Delete Job Files

You can only copy some of the controller's job files.
When copying job files from the robot controller to the PC, click and select the targeted job files under the `Robot Controller/jobs/` path in the Explore window.
To select multiple files, you use the following methods.


<table>
<tr>
  <td><img src="../_assets/backup/job1.png"/></td>
  <td>Drag and select multiple files while pressing the left button.</td>
</tr>
<tr>
  <td><img src="../_assets/backup/job2.png"/></td>
  <td>Select one file, hold the Shift key, then click another file to select files in between.</td>
</tr>
<tr>
  <td><img src="../_assets/backup/job3.png"/></td>
  <td>Select multiple files individually while pressing the ctrl key.</td>
</tr>
</table>

Right-click the selected job files and then select `Backup to PC` in the pop-up menu. The copy result will be displayed in the Log window, and the names of copied files will be displayed on the `PC/jobs` node.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/job4.png" width="40%">
  <img src="../_assets/backup/job5.png" width="30%" height="30%">
</div>

The method is similar when copying files from the PC to the robot controller.
Click and select the desired job files under the `PC/jobs/` path in the Explore window.
Right-click the selected job files and select `Restore to Robot Controller` in the pop-up menu.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/job10.png" width="40%">
  <img src="../_assets/backup/job11.png" width="30%" height="30%">
</div>

<br/>

You can delete job files in the robot controller or the job files in the PC using the `Delete` pop-up menu.

![](../_assets/backup/job-del.png)

[__SOURCE](4-job-var/README.md)
# 4. Editing Jobs and Variables


[__SOURCE](4-job-var/1-job-edit/README.md)
# 4.1 Edit Job Files

You can edit the job files copied to the PC with your preferred text editor, but HRWorkBench also provides an editor.

[__SOURCE](4-job-var/1-job-edit/1-job-edit-wnd.md)
# 4.1.1 Open and Arrange Edit Windows

Double-click the desired PC-side job file in the Explore pane to open the editor. Let's open four job files in sequence: 0001.job, 0005.job, 0006.job, and 0007.job. As shown below, the editor window for the last opened file, 0007.job, fills the area, with the file names displayed on the tabs.
 
![](../../_assets/job-edit/job-tab01.png)


You can select a tab to edit the desired job. To compare two files, you can split the area into up to two panes using the `Window - Split Area` menu or tool button. Clicking it once more will merge the areas back together.
  
![](../../_assets/job-edit/job-tab02.png)
![](../../_assets/job-edit/job-tab03.png)

You can reorder tabs by dragging them with the left mouse button. Alternatively, you can move a tab to another area using the `Window - Move Tab to Other Area` menu or the tool button.
Selecting `Tile` or `Cascade` from the `Window` main menu or the toolbar allows you to arrange multiple job editor windows side by side within an area.

![](../../_assets/job-edit/job-tab04.png)
![](../../_assets/job-edit/job-tab05.png)

You can minimize the Edit window with the <img src="../../_assets/job-edit/job-min.png"> button and maximize it with the <img src="../../_assets/job-edit/job-max.png"> button. Clicking the <img src="../../_assets/job-edit/job-close.png"> button or pressing `ctrl+F4` will close the Edit window.

[__SOURCE](4-job-var/1-job-edit/2-encoding.md)
# 4.1.2 Reloading after Converting Encoded Job Files

When a job file is opened, non-English characters (Korean, Chinese, etc.), comments, or strings may appear broken. The job file of the ${cont_model} controller should be saved in utf-8 encoding, but the file will not be displayed properly in HRWorkBench and teach pendant if the file is saved with a different type of encoding (EUC-KR, GB2312). 

![](../../_assets/job-edit/encoding1.png) 


For example, if the job file is encoded in an extended complete type, select `Job - Encoding: Reload from - Korean` in the main menu. The job file will be converted to a utf-8 encoding and opened in the Edit window, and the text will now be displayed correctly. When saved in this state, the file will be saved as a utf-8 encoding file.
(The ascii file and utf-8 file are the same for a file only written in English, so this operation will not be necessary.)

![](../../_assets/job-edit/encoding2.png) 

[__SOURCE](4-job-var/1-job-edit/3-syntax-coloring.md)
# 4.1.3 Syntax Coloring and Automatic Multi Stage Indentation (Smart Indent)

The Edit window provides basic syntax coloring for readability, where main commands and strings, hidden poses, comments, and job headers are displayed in unique colors.

![](../../_assets/job-edit/syntax-color.png)


An automatic multi stage indentation function (smart indent) is also used for a more easy-to-read structure of the flow control statement. All of the current job programs in the Edit window will be automatically indented if you click `Smart Indent` under the Job main menu or toolbar.


<div style="display: flex; gap: 20px;">
  <img src="../../_assets/job-edit/smart-indent1.png" width="20%" height="20%">
  <img src="../../_assets/job-edit/smart-indent2.png" width="50%">
</div>

[__SOURCE](4-job-var/1-job-edit/4-undo-redo.md)
# 4.1.4 Undo, Redo, and Save

The Edit window provides Undo and Redo functions with the shortcut keys `Ctrl+Z` and `Ctrl+Y`.

An asterisk (*) mark in the file name in the title bar, as shown below, means that some edited content have not been saved.
You can save the edited contents to a file by selecting `File - Save` or `File - Save As` in the main menu. You can also use the shortcut `Ctrl+S` or click the <img src="../../_assets/tool-btn/tb-save.png"> button in the toolbar.

![](../../_assets/job-edit/title-star.png)


The file will be saved and copied to and immediately reflected in the robot controller if you select `Job - Save & Copy to RC` in the main menu or click the <img src="../../_assets/tool-btn/tb-upload2rc.png"> button on the toolbar.

[__SOURCE](4-job-var/1-job-edit/5-find-replace.md)
# 4.1.5 Find, Replace, and Go To Lines

You can open the Find/Replace dialog box by selecting `Edit - Find and Replace` in the main menu or by pressing the shortcut key `Ctrl+F` or `Ctlr+F3.` If a specific text has been selected, the text will be automatically inputted into `Find`. 
 
![](../../_assets/find-replace/find01.png)

The functions of the individual options in the dialog box are shown below.

<table>
<tr>
  <th>이름</th>
  <th colspan=2>기능</th>
</tr>
<tr>
  <td rowspan=2>Look In</td>
  <td>Current Document</td>
  <td>The function will be performed within the currently selected window. </td>
</tr>
<tr>
  <td>Current Project</td>
  <td>The function will be performed for all jobs under the PC node of a project.</td>
</tr>
<tr>
  <td>Case Sensitive</td>
  <td colspan=2>Selecting this function makes it possible to distinguish between upper and lower cases.</td>
</tr>
<tr>
  <td>Whole Word</td>
  <td colspan=2>Selecting this makes it possible to perform searches only for a complete word.</td>
</tr>
</table>


Clicking the `Find prev.` or `Find next` button allows the cursor to move to the prev. or next matching string. Clicking the `Replace` button allows the currently selected string to be replaced with the string inputted under Replace with and then allows the cursor to move to the next matching string.
Clicking the `Find all` button searches for the entire range designated under `Look In`, and lists the searched items in the `Find Results` window at the bottom in the form of its path file name (line number): string. When you double-click on a specific item, the relevant file will be opened, and the cursor will move to the matching position.
(Even when the `Find/Replace` dialog box is closed, you can use the shortcut keys `Shift+F3 (Find Previous)` and `F3 (Find Next)`.)

![](../../_assets/find-replace/find02.png)


Clicking the `Replace all` button searches the entire range designated in `Look In` and replaces the matching string with the string inputted in `Replace with`. Moreover, this function will list the searched items in the `Find Results` window at the bottom. 
You can select `Job - Go To` in the main menu or press the shortcut key `Ctrl+G` to open the Go To Line dialogue box. When you input a line number, the cursor will move to the line number. 

![](../../_assets/find-replace/dlg-goto.png)

[__SOURCE](4-job-var/1-job-edit/6-etc.md)
# 4.1.6 Other functions

*	Font Size Adjustment: `Ctrl+mouse wheel` to change the font size in the job editor.

[__SOURCE](4-job-var/2-syntax-check.md)
# 4.2 Check the Robot Language Syntax

You can remotely carry out a basic syntax check on the job file currently being edited. 

While the job file to be checked is open, as shown below, click `Syntax Check` on the main menu or on the toolbar.

![](../_assets/job-edit/syntax-check1.png)
 
![](../_assets/job-edit/syntax-check2.png)

The path file name and line number, where there is a syntax error, and the relevant error message will be displayed on the `Syntax Check` window.

Double-clicking an error will move the cursor to the corresponding position.
 
![](../_assets/job-edit/syntax-check3.png)

Because this syntax check is executed without the actual execution of a job, it cannot detect all errors that may occur when a job is executed. In the job file shown in the figure above, it was detected that `var` was incorrectly marked as `val` and that the `move` statement accuracy exceeded the range of 0-7. However, it could not detect that the I/O variable do31 of the `wait` statement was incorrectly marked as `DO31` and that `tno=2` was incorrectly marked as `tn=2.` They are not considered errors because the variables `DO31` and `tn` may possibly have been created during execution.

[__SOURCE](4-job-var/3-exec-roblang.md)
# 4.3 Execute Robot Language Statements

You can remotely execute robot language statements in job files. A move statement or flow control statement is not supported. It only supports some commands can be executed individually, such as assignment statements.

The global variables window in the teach pendant of the connected ${cont_model} controller should be left open to check the result.

The following program was created as a demonstration in the Job Edit window.

![](../_assets/job-edit/exec-roblang01.png)


Place the cursor on global msg="Hello," and click on Job in the main menu, or `Run Current Line` in the toolbar.
 
![](../_assets/job-edit/exec-roblang02.png)

A success message will be displayed in the Log window if the remote execution is successful. In the global variables of the teach pendant, you can also see that the `msg` variable has been created.
     
![](../_assets/job-edit/exec-roblang03.png)
![](../_assets/job-edit/exec-roblang04.png)

 
Clicking on `Job` in the main menu or `Run Job` in the toolbar will execute all of the currently selected jobs, including the `print` statement.

![](../_assets/job-edit/exec-roblang05.png)
![](../_assets/job-edit/exec-roblang06.png)

[__SOURCE](4-job-var/4-gvar-mon.md)
# 4.4 Monitor Global Variables and Set Their Values

When the connect button is pressed online, the Global Variables window displays the current global variable values. The functionality of the Global Variables window is almost identical to that of the ${cont_model} Teach Pendant (TP630). 

See the link below for instructions.

https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/3-job/3-global-variable/README?cont_model=Hi7


![](../_assets/var-edit/gvar01.png)


*	The common things: Finding variables, changing variable type/name/value, creating/deleting variables, creating arrays, checking/changing array element values, and checking/changing object property values are all the same.

*	The differences: The properties window for Pose/Shift values is not supported, and expands the same as any other object type.

![](../_assets/var-edit/gvar02.png)


*	Use the <img src="../_assets/var-edit/gvar03.png"> buttons to navigate back, forward, or up to the parent folder.

[__SOURCE](4-job-var/5-gvar-copy-del.md)
# 4.5 Copying and deleting global variable files

{% hint style="info" %}
The global variable export function prior to v1.4.2 is superseded by this function.
{% endhint %}

The Variables window allows you to monitor global variables and set values, but has limitations in editing large lists of variables.
Global variables are stored in `var.json` files within the ${cont_model} controller, of which predefined-variables are stored in `.csv` files. These are all text files, so you can easily edit them if you copy them to your PC.

The method of backing up and restoring variable files is similar to job files. Select the `vars/` folder of the robot controller, or some files, and then right-click to open the pop-up menu. When the `Backup to PC` menu is selected, the Log panel displays the copy results, and the copied file names are displayed in the `PC/vars` node.

![](../_assets/var-edit/var-backup1.png)
![](../_assets/var-edit/var-backup2.png)
![](../_assets/var-edit/var-backup3.png)

Next, let's copy from the PC to the robot controller. The methods are similar.

Click to select the desired variable files under `PC/vars/` path in the Explorer panel.
Click the right button on the selected variable files and select the `Restore to Robot Controller` pop-up menu.

![](../_assets/var-edit/var-restore1.png)
![](../_assets/var-edit/var-restore2.png)


Variable files on the robot controller or PC can be deleted using the `Delete` pop-up menu. Deleting a variable file on the robot controller also deletes that variable.

![](../_assets/var-edit/var-del.png)

{% hint style="warning" %}
When restoring or deleting variables, the ${cont_model} controller must be in the Motor-Off state. When carried out in the Motor-On state, the message is displayed that it is not possible.
{% endhint %}

Double-click a variable file on your PC to open a text edit window. If you double-click the variable file on the robot controller, once it backs up it to `PC/vars/` and open the file on the PC side.

![](../_assets/var-edit/csv-edit.png)

[__SOURCE](5-log/README.md)
# 5. Check Robot Controller's Log


[__SOURCE](5-log/1-event-log/README.md)
# 5.1 Monitor Event Logs in the Controller


[__SOURCE](5-log/1-event-log/1-event-log-mon.md)
# 5.1.1 Event log monitoring window

At the bottom, you can see two tabs: `Event Log - RC` and `Event Log - PC`.

`Event Log - RC` is a window that monitors the event log in the controller and the newly occurring events in the ${cont_model}  controller connected via Ethernet.

`Event Log - PC` is a window that reads and displays event log files in the `log/` folder of the PC path. (Supported in ${cont_model} Controller V60.05-04 and later versions.)

This window provides the similar functions as those of the U/I provided by ${cont_model}'s teach pendant. New events will be highlighted in yellow.

![](../../_assets/log/evlog01.png)


At the top of the window are event type filter buttons, displaying only the pressed type of events. For example, only the types of errors (E), warnings (W), and alerts (N) are displayed in the figure above.  (After adjusting the filter buttons, click the Update button (<img src="../../_assets/log/evlog-bt-update.png">) to the right of the filters to refresh the screen.)

<table>
<tr>
  <th>Category</th>
  <th>U/I</th>
  <th>Description</th>
</tr>
<tr>
	<td rowspan=9>Filter</td>
  <td>All</td>
  <td>Turn (toggle) on or off all types of logs.</td>
</tr>
<tr>
  <td>E (Error)</td>
  <td>Display the error log.</td>
</tr>
<tr>
  <td>W (Warning)</td>
  <td>Display the warning log.</td>
</tr>
<tr>
  <td>N (Notice)</td>
  <td>Display the notice log.</td>
</tr>
<tr>
  <td>ST (Start/Stop)</td>
  <td>Display the start/stop logs.</td>
</tr>
<tr>
  <td>P (Periodic)</td>
  <td>Display the periodic state log.</td>
</tr>
<tr>
  <td>OP (Operation)</td>
  <td>Display the operation log.</td>
</tr>
<tr>
  <td>IO (I/O)</td>
  <td>Display the I/O logs.</td>
</tr>
<tr>
  <td>H (History)</td>
  <td>Display the execution history.</td>
</tr>
<tr>
  <td>Update</td>
  <td><img src="../../_assets/log/evlog-bt-update.png"></td>
  <td>Apply the selected filters</td>
</tr>
<tr>
  <td></td>
  <td><img src="../../_assets/log/evlog-cb-cnt.png"></td>
  <td>Select the number of logs to be displayed on the window and refresh the screen.</td>
</tr>
<tr>
  <td>Reload & update</td>
  <td><img src="../../_assets/log/evlog-bt-update.png"></td>
  <td>Reload events from the controller or files, and display on the table.</td>
</tr>
<tr>
  <td rowspan=2><img src="../../_assets/log/bt-dot3.png"><br>(Pop-up menu)</td>
  <td>Save to log files</td>
  <td>Save the logs that have been accumulated in the controller's memory as log files in the controller.</td>
</tr>
<tr>
  <td>Clear log files</td>
  <td>Clear all the logs both in the controller's memory and in the log files.</td>
</tr>
<tr>
  <td rowspan=2></td>
  <td><img src="../../_assets/log/bt-lock.png"></td>
  <td>Stop monitoring a new log.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-trash.png"></td>
  <td>Clear the items in the Event Log window.</td>
</tr>
<tr>
  <td rowspan=2></td>
  <td><img src="../../_assets/log/bt-aux.png"></td>
  <td>Open auxiliary data window.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope.png"></td>
  <td>Open scope.</td>
</tr>

</table>


[__SOURCE](5-log/1-event-log/2-event-find.md)
# 5.1.2 Finding an event

In the Event History pane, select the `Edit - Find and Replace...` menu, or press `Ctrl+F` to open the Find event dialog box.
In `Find:`, enter the code, message, date time, or prog.cnt to find, and click `Find next` or `Find prev` to search from the currently selected row and select the next or previous row containing the string.

![](../../_assets/log/evlog-find.png) 


The functionality of each option in the dialog box is as follows.

<table>
<tr>
  <th>Name</th>
  <th>Function</th>
</tr>
<tr>
  <td>Look in</td>
  <td>
    It displays the name of history window in which it performs the search, among Event Log-RC and Event Log-PC.
    (The Find event dialog boxes exist separately for the Event History-RC window and the Event History-PC window. Open the dialog box in the corresponding history window and then perform Find.)
  </td>
</tr>
<tr>
  <td>Case Sensitive</td>
  <td>Selecting this function makes it possible to distinguish between upper and lower cases.</td>
</tr>
<tr>
  <td>Whole Word</td>
  <td>Selecting this makes it possible to perform searches only for a complete word.</td>
</tr>
</table>


[__SOURCE](5-log/1-event-log/3-event-text-copy.md)
# 5.1.3 Copy event text

Right-clicking the selected event history opens a pop-up menu.

![](../../_assets/log/evlog-text-copy.png) 

*	Copy Cell Text: Copies the text from the selected row and column to the clipboard.
*	Copy Row Text: Copies the text from all columns in the selected row to the clipboard. The text from each column is separated by the `|` character.

[__SOURCE](5-log/2-aux-data/README.md)
# 5.2 Auxiliary Data

If you click the <img src="../../_assets/log/bt-aux.png"> button, five event aux. data windows will be open.

![](../../_assets/log/evlog-aux-panel.png) 

<table>
<tr>
  <th>panel name</th>
  <th>contents</th>
  <th>supported event type</th>
</tr>
<tr>
  <td>aux.pose</td>
  <td>program counter and pose data</td>
  <td>error/warning/start/stop</td>
</tr>
<tr>
  <td>aux.sin</td>
  <td>system input</td>
  <td>error/warning/start/stop</td>
</tr>
<tr>
  <td>aux.sout</td>
  <td>system output</td>
  <td>error/warning/start/stop</td>
</tr>
<tr>
  <td>aux.din</td>
  <td>general input</td>
  <td>periodic state/IO</td>
</tr>
<tr>
  <td>aux.dout</td>
  <td>general output</td>
  <td>periodic state/IO</td>
</tr>
</table>

[__SOURCE](5-log/2-aux-data/1-aux-pose.md)
# 5.2.1. Pose Data (aux.pose)

When you click the Error/Warning/Start/Stop event row, the program counter at the time of the event and the value of each axis (mm|deg) are displayed.

Because program counters and pose auxiliary data are recorded only on error and warning events, when you click on rows of different types of events, the data are dimly displayed. This indicates that it is the data of error/warning/start/stop event recorded just before that event, and may not be accurate.


![](../../_assets/log/evlog-aux-pose1.png)
![](../../_assets/log/evlog-aux-pose2.png)

[__SOURCE](5-log/2-aux-data/2-aux-sio.md)
# 5.2.2 System input/output (aux.sin/sout)

When you click the Error/Warning/Start/Stop event row, the system input and output at the time the event are displayed.

Because system I/O auxiliary information is recorded only for error and warning events, when you click on rows of different types of events, the data are dimly displayed. This indicates that it is the data of error/warning/start/stop event recorded just before that event, and may not be accurate.


![](../../_assets/log/evlog-aux-sin.png)

[__SOURCE](5-log/2-aux-data/3-aux-dio.md)
# 5.2.3 General input/output (aux.din/dout)

When you click the Periodic State/IO event row, the general input and output are displayed.

![](../../_assets/log/evlog-aux-dout.png)


Using the combo box at the top, you can select the signal groups `fb0 to fb9` to be displayed. IO events occur only with the differential information when any `dio` value changes. In addition, the periodic state event occurs with only one `fb` group's full `dio` information per minute in the ${cont_model} controller. HRWorkBench accumulates this information to show all the `dio` information in all `fb` groups in the general input/output window for each event row.

Therefore, if you click on a row of older events where the `dio` information is not accumulated enough, the data is not displayed and but just `?` symbol, as below.

![](../../_assets/log/evlog-aux-dout2.png)

[__SOURCE](5-log/3-scope-log/README.md)
# 5.3 Scope log

(Supported in ${cont_model} Controller V60.05-04 and later versions.)

[__SOURCE](5-log/3-scope-log/1-scope-log-intro.md)
# 5.3.1 What is scope log?

When a critical error or warning such as `E160 collision detection` occurs, the ${cont_model} controller stores data for required analysis such as position/speed/acceleration/status codes of each axis in a sampling period of 5ms, length of 30 seconds (25 seconds before occurrence + 5 seconds after occurrence). This is called scope log.
The scope log is stored in the `log/` folder of the controller as a pair of `.json` and `.bin` files. (Because of the large capacity, only a certain number is saved and the old data is deleted.)
The scope history stored in the remote robot controller and PC path is displayed in the `log/` folder of the explorer window, and the node name is the time of file storage in the form of YYYYMMDD_HHMMSS.

![](../../_assets/log/scopelog01.png)

[__SOURCE](5-log/3-scope-log/2-scope-log-open.md)
# 5.3.2 Open scope

![](../../_assets/log/scopelog02.png)

Select a row of critical errors or warning events and click the <img src="../../_assets/log/bt-scope.png"> button at the top right to open the scope window.

(If you do not have a scope log file at the time of the event, it will not open.)

(You can also double-click the scope log item in the `log/` folder in the explorer window.)

![](../../_assets/log/scopelog03.png)

Click the <img src="../../_assets/log/bt-scopelog-field.png"> button in the upper left corner to open a field (item) selection window.

![](../../_assets/log/scopelog04.png)

Each item in the field selection window displays its name, unit, and description.


<table>
<tr>
  <th>Button</th>
  <th>Function</th>
  <th>Misc.</th>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-trash.png"></td>
  <td>Uncheck all.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-check.png"></td>
  <td>Check all selected rows.<br>
    (You can select several rows by dragging with mouse left button, or click with ctrl+left / shift+left button.)
	</td>
  <td><img src="../../_assets/log/scopelog07.png"></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-uncheck.png"></td>
  <td>Uncheck all selected rows.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-csv.png"></td>
  <td>Export to .csv file.</td>
  <td>To use in external software.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-ok.png"></td>
  <td>Close the field selection window and display the graph of the checked items.</td>
  <td></td>
</tr>
</table>

For example, qr[0]~qr[5]'s unit is mm or rad, and they are the `joint position` data on 1 to 6 axes.

Check qr[0]~qr[2] and click the `OK` button if you want to check the data on the 1st to 3rd axes at the time of robot-collision.

![](../../_assets/log/scopelog05.png)


After a few seconds, the graph opens.

![](../../_assets/log/scopelog06.png)

[__SOURCE](5-log/3-scope-log/3-graph.md)
# 5.3.3 Graph Operation

<table>
<tr>
  <th>Button</th>
  <th>Function</th>
  <th>Operation on Graph</th>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-adddel.png"></td>
  <td>Add a graph or remove selected graph.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-field.png"></td>
  <td>Open Select Fields window.</td>
  <td><img src="../../_assets/log/scopelog07.png"></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-arrow.png"></td>
  <td>Select Normal Cursor mode.<br>(For moving markers)
</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-t.png"></td>
  <td>Select the area on the T(time) axis to zoom in.</td>
  <td>Press the mouse left button, and drag to select the area to zoom-in.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-yt.png"></td>
  <td>Select the area on the Y(vertical), T(time) axes to zoom in.</td>
  <td>Press the mouse left button, and drag to select the area to zoom-in.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-out.png"></td>
  <td>Zoom out to the state one step before zoom-in.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-pan-t.png"></td>
  <td>In the zoomed-in state, pan to the T(time) axis.</td>
  <td>Press the mouse left button, and drag left and right.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-pan-yt.png"></td>
  <td>In the zoomed-in state, pan to the Y(vertical), T(time) axes.</td>
  <td>Press the mouse left button, and drag up, down, left and right.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-marker.png"></td>
  <td>Open and close the marker table. (toggle)</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-csv2.png"></td>
  <td>Export to .csv file.</td>
  <td></td>
</tr>
</table>

------------------

Let's add another graph at the bottom.

If you click the <img src="../../_assets/log/bt-scopelog-add.png"> button, another graph is added at the bottom. The green border on the bottom graph means that the graph is currently selected (you can select it by left-clicking on the surface of the graph with the normal cursor)


![](../../_assets/log/scopelog11.png)

Click the <img src="../../_assets/log/bt-scopelog-field.png"> button and check dqm[0]~dqm[2] to display a velocity graph of 1~3 axes together.


![](../../_assets/log/scopelog12.png)

Click <img src="../../_assets/log/bt-scopelog-zoom-yt.png"> and drag some area on the graph to zoom in.

![](../../_assets/log/scopelog13.png)
![](../../_assets/log/scopelog14.png)


Click <img src="../../_assets/log/bt-scopelog-pan-yt.png"> and drag it to the graph with the left mouse button to pan the Y and T axes. The two graphs are always moved in synchronization with the T (time) axis.

[__SOURCE](5-log/3-scope-log/4-marker.md)
# 5.3.4 Marker

When you click <img src="../../_assets/log/bt-scopelog-marker.png"> button, marker table opens. (Click once more to close.)

Clicking the <img src="../../_assets/log/bt-marker-add.png"> button on the left adds a marker row M0 to the table, displaying the M0 marker line (vertical dotted line) on the graph.

(Not visible if it is outside the zoomed area. Try zoom-out to find it.)
 
 ![](../../_assets/log/scopelog21.png)

You can move the marker line by dragging it with the left mouse button. The time point at which the marker line is located and the absolute time (HH:MM:SS.usec), and the values for each field at that time are displayed in the table.

Whenever you click <img src="../../_assets/log/bt-marker-add.png"> button, a marker line and a table row is added. (M1, M2,...)

Whenever you click <img src="../../_assets/log/bt-marker-del.png"> button, the marker of selected table row is removed.

[__SOURCE](5-log/3-scope-log/5-export2csv.md)
# 5.3.5 Export to .csv file

If you want to analyze scope log data with other software, such as _Microsoft Excel_ or _MATLAB_, you can save it as a `.csv (comma-separated values)` standard format file.

After selecting a graph, click the <img src="../../_assets/log/bt-scope-csv.png"> button to open the `Save File` dialog box. Specify the path file name and click the `Save` button.

![](../../_assets/log/scopelog31.png)
<br><br>
![](../../_assets/log/scopelog32.png)


The below figure shows an example of visualizing a saved file in _Excel_ with the chart tool.

![](../../_assets/log/scopelog33.png)

[__SOURCE](6-rc-setting/README.md)
# 6. Checking and Porting Controller Settings


[__SOURCE](6-rc-setting/1-rc-set-view.md)
# 6.1 Checking Controller Setting

You can check the contents of the setting files copied to the PC.

In the explorer window, under the `PC/project/` folder, you will find .json files containing the settings.
To view a specific `.json` file, right-click on it and select `Treeview` from the context menu. This will open the `Treeview of json` dialog.

![](../_assets/rc-setting/rcset-01.png)
![](../_assets/rc-setting/rcset-02.png)


You can check the hierarchical property structure and setting values, but they cannot be edited.

To search for a property name or value, press `Ctrl+F` to open the Find dialog and perform a search."

![](../_assets/rc-setting/rcset-find.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/README.md)
# 6.2 Porting Controller Settings


[__SOURCE](6-rc-setting/2-rc-set-porting/1-intro.md)
# 6.2.1 Overview

For example, if you copy a specific `.json` setting file from Robot Controller A to Robot Controller B and then restart the power, the corresponding settings from Controller A can be applied identically to Controller B.

However, if you wish to apply only part of the settings (or global variables) from one controller to another, you must manually copy the relevant string portion from Controller A's `.json` file and overwrite the corresponding section in Controller B's `.json` file. Such manual work is cumbersome and carries the risk of damaging the `.json` format by mistake, which may result in the controller failing to boot or malfunctioning.
By using the porting function of HRWorkbench, these operations can be performed more easily and safely.

For instance, suppose there are four arc-welding cells, C1~C4, in a workshop. After completing the arc-welding setting and teaching on C1, if the welding conditions between `cnd_1000` and `cnd_1100` need to be horizontally deployed to C2~C4, you can simply export the relevant settings from C1 and import them into C2, C3, and C4. The following procedure explains the porting function using this example.

![](../../_assets/rc-setting/rcset-port-concept.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/2-export-import.md)
# 6.2.2 Export and Import

We will begin the practice assuming that each controller (C1~C4) has its own backup folder on the PC and that a full backup of each controller has already been created.

![](../../_assets/rc-setting/rcset-port-01.png)

First, select the PC path for controller C1.
 
![](../../_assets/rc-setting/rcset-port-02.png)

Open the Tree View for the `PC/project/arc_weld.json` file, and select cnd_1001 through cnd_1092. (Multiple items can be selected using the SHIFT and Ctrl key combinations.)

![](../../_assets/rc-setting/rcset-port-03.png)
![](../../_assets/rc-setting/rcset-port-04.png)

Right-click on the selected items to open the context menu, and choose `Export`.
 
![](../../_assets/rc-setting/rcset-port-05.png)

Enter an appropriate JSON file name and click `Save`. (For partial JSON files, use the `.part.json` extension.)
 
 ![](../../_assets/rc-setting/rcset-port-06.png)

You will now see the file `cnd_1000.part.json` saved under `PC/project/` in the explorer. (This file can also be opened in Treeview for inspection.) Copy the generated file using the context menu.

![](../../_assets/rc-setting/rcset-port-07.png)

Select the PC path of Controller C2, and paste the file into `PC/project/`.

(Instead of using HRWorkbench, you may also copy the file with Windows Explorer or other tools.)

 
![](../../_assets/rc-setting/rcset-port-08.png)

Open the Treeview of the pasted file `cnd_1000.part.json`.

![](../../_assets/rc-setting/rcset-port-09.png)

After reviewing the Treeview contents, right-click on the top-level node `cnd_1000.part.json` and execute `Import - arc_weld.json`.
 
![](../../_assets/rc-setting/rcset-port-10.png)
![](../../_assets/rc-setting/rcset-port-11.png)

Repeat the same procedure for Controllers C3 and C4.

(The `cnd_1000.part.json` file in each folder may be deleted after the import is completed.)

Note: Global variables can also be exported and imported in the same way as the settings.


![](../../_assets/rc-setting/rcset-port-12.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/3-export-freq-path.md)
# 6.2.3 Exporting Often Used Paths

If you often need to repeatedly export settings for multiple paths, manually selecting the paths each time can be cumbersome.

To simplify this, you can predefine a list of frequently used paths in a file and apply it in the Treeview to quickly and easily select them.

As a simple example, let's select 4 items under `arc_conds/` and 4 items under `lvs_tracking/` in `arc_weld.json` using this method.

![](../../_assets/rc-setting/rcset-freq-1.png)
![](../../_assets/rc-setting/rcset-freq-2.png)

Using a text editor, create a `.json` file in any folder on the PC as shown below.

The file must follow JSON syntax (https://www.json.org/json-en.html), but the file name itself is not important.


- often_used_path.json
	```json
	{
		"lvs gains": [
			"lvs_tracking.d_gain_0",
			"lvs_tracking.d_gain_1",
			"lvs_tracking.p_gain_0",
			"lvs_tracking.p_gain_1"
		],
		"arc.cond 1001~1004" : [
			"arc_conds.cnd_1001",
			"arc_conds.cnd_1002",
			"arc_conds.cnd_1003",
			"arc_conds.cnd_1004"
		]
	}
	```

In the example above, `lvs gains` and `arc.cond 1001-1004` are the group names that will appear in the combo-box.

The values for each group should be written as an array of path strings, i.e., listed within `[ ]`.

(To check the path for a specific item, select the item and refer to the combo-box at the top of the Tree View dialog, as shown in the figure below.)

![](../../_assets/rc-setting/rcset-freq-3.png)

Drag the created `.json` file in Windows Explorer and drop it onto the combo-box at the top of the Treeview.
 
![](../../_assets/rc-setting/rcset-freq-4.png)


When you open the combo-box, you will see the group names you defined. For example, selecting `lvs gains` will automatically select the corresponding paths.
 
![](../../_assets/rc-setting/rcset-freq-5.png)


Click the `Export`(<img src="../../_assets/rc-setting/bt-export.png">) button at the top left to export the items in the selected group.

![](../../_assets/rc-setting/rcset-freq-6.png)
