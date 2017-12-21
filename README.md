# expdivision
Exponential long division/multiplication, upto 80x times faster logical long division(Algorithm)
x = log_a(b) ......(greatly reduced cycles)
![alt text](https://addzlabs.files.wordpress.com/2017/12/untitled.png)
single-pass exponential division drawback:
eg:  31/2  <-----this is okay since 16 falls near and less than or equal to whole number(n)                                    cycle (2^4) 
EXP DIVI ---> (2,4,8,16,32)---->32-2--->30  } about 5 cycles

NORMAL DIVI ----> (2,4,6,8,10......,30,32)----->32-2---->30 } about  16 cycles!

but now:

33/2 <-----this is going to be a problem :|

EXP DIVI ---> (2,4,8,16,32,64)---->(64,62.......,34,32)---->32  } about 22 cycles!

NORMAL DIVI ----> (2,4,6,8,10......,30,32,34)----->34-2---->32 } about  18 cycles

Now i did the obvious thing here :) to fix the problem, yes! subtract exponentially, it may sound a little confusing at first but its really simple if you look carefully, as the linear slope is replaced with an exponential slope the sequence will kind of oscillate back and forth damping exponentially :) and if you analyse this sequence you would get a beautifully damping sine wave pattern.
![alt text](https://addzlabs.files.wordpress.com/2017/12/desmos-graph.jpg)
Multi-pass exponential division vs Single-pass exponential division(worst case scenario)
Test case : 65537 / 2  <---- an extremely worst case
![alt text](https://addzlabs.files.wordpress.com/2017/12/untitled4.png)
