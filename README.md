# 3d-elastic-kernel

This is the code I've done in SEP, and is the 3D elastic RTM kernel.

Unlike the 2D one that is the whole program from forward and backward, the 3D one only contains the backward with random 
input and output. 

The purpose of this code is to provide a 3D GPU interfaces for late usage. 




Performance 

Simply using L1, 200*200*200, ts = 1
CPU compiler: +opmp, +O3
<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>
CPU time for 1 steps:  10.03823566
Computing   Speedup: 89.90
Application Speedup: 11.78
<<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>



Simply using L1, 200*200*200, ts = 8
CPU compiler: +opmp, +O3
<<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>
CPU time for 8 steps:  85.90319824
Computing   Speedup: 95.60
Application Speedup: 52.67
<<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>



Using L1, Read-Only, 200*200*200, ts = 8
CPU compiler: +opmp, +O3
<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>
CPU time for 8 steps:  85.64048767
Computing   Speedup: 75.73
Application Speedup: 45.73
<<<<<<<<<<<<<<<<<PERFORMANCE PROFILING>>>>>>>>>>>>>>>>
