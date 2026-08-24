# 4.1.3 Reloading after Converting Encoded Job Files

When a job file is opened, non-English characters (Korean, Chinese, etc.), comments, or strings may appear broken. The job file of the Hi6/Hi7 controller should be saved in utf-8 encoding, but the file will not be displayed properly in HRWorkBench and teach pendant if the file is saved with a different type of encoding (EUC-KR, GB2312). 

![](../../_assets/job-edit/encoding1.png) 


For example, if the job file is encoded in an extended complete type, select `Job - Encoding: Reload from - Korean` in the main menu. The job file will be converted to a utf-8 encoding and opened in the Edit window, and the text will now be displayed correctly. When saved in this state, the file will be saved as a utf-8 encoding file.
(The ascii file and utf-8 file are the same for a file only written in English, so this operation will not be necessary.)

![](../../_assets/job-edit/encoding2.png) 
