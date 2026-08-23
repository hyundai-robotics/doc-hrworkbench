# 6.2.1. Overview

For example, if you copy a specific `.json` setting file from Robot Controller A to Robot Controller B and then restart the power, the corresponding settings from Controller A can be applied identically to Controller B.

However, if you wish to apply only part of the settings (or global variables) from one controller to another, you must manually copy the relevant string portion from Controller A's `.json` file and overwrite the corresponding section in Controller B's `.json` file. Such manual work is cumbersome and carries the risk of damaging the `.json` format by mistake, which may result in the controller failing to boot or malfunctioning.
By using the porting function of HRWorkbench, these operations can be performed more easily and safely.

For instance, suppose there are four arc-welding cells, C1~C4, in a workshop. After completing the arc-welding setting and teaching on C1, if the welding conditions between `cnd_1000` and `cnd_1100` need to be horizontally deployed to C2~C4, you can simply export the relevant settings from C1 and import them into C2, C3, and C4. The following procedure explains the porting function using this example.

![](../../_assets/rc-setting/rcset-port-concept.png)
