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
