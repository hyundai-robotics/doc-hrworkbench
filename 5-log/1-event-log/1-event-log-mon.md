# 5.1.1 Event log monitoring window

At the bottom, you can see two tabs: `Event Log – RC` and `Event Log – PC`.

`Event Log – RC` is a window that monitors the event log in the controller and the newly occurring events in the ${cont_model}  controller connected via Ethernet.

`Event Log – PC` is a window that reads and displays event log files in the `log/` folder of the PC path. (Supported in ${cont_model} Controller V60.05-04 and later versions.)

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
  <td>Save the logs that have been accumulated in the controller’s memory as log files in the controller.</td>
</tr>
<tr>
  <td>Clear log files</td>
  <td>Clear all the logs both in the controller’s memory and in the log files.</td>
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

