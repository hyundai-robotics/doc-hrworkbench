# 5.3.1 What is scope log?

When a critical error or warning such as `E160 collision detection` occurs, the ${cont_model} controller stores data for required analysis such as position/speed/acceleration/status codes of each axis in a sampling period of 5ms, length of 30 seconds (25 seconds before occurrence + 5 seconds after occurrence). This is called scope log.
The scope log is stored in the `log/` folder of the controller as a pair of `.json` and `.bin` files. (Because of the large capacity, only a certain number is saved and the old data is deleted.)
The scope history stored in the remote robot controller and PC path is displayed in the `log/` folder of the explorer window, and the node name is the time of file storage in the form of YYYYMMDD_HHMMSS.

![](../../_assets/log/scopelog01.png)
