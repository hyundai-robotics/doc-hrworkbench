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
