# 3.1 Back Up and Restore Files

You can back up or restore the files in the Hi6/Hi7 controller.
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
When performing the restore, the Hi6/Hi7 controller must be in the motor-off state. When performed in the motor-on state, a 'impossible' message is output
{% endhint %}
