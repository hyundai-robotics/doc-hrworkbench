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
|Verify and Port Settings|You can apply some of a controller’s settings or variables to another controller in the same way.|


{% hint style="warn" %}
This program allows you to remotely change the job program or variable value, so it may affect the robot′s operation. You are required to read this manual and use the program carefully while paying sufficient attention!
{% endhint %}

* HRWorkBench can be downloaded from the `Download center` page under `Customer Support` on the HD Hyundai Robotics website(https://www.hd-hyundairobotics.com/en/main).
