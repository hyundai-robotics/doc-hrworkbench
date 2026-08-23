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
