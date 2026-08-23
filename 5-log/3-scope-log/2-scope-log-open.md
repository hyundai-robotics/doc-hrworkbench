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
