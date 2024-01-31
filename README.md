# The Sillybugs homework

The program in this repository contains a number of severe performance bugs. First install the m4 macro preprocessor apt-get install m4, then clone the repository, then go to the folder codes/apps/raytrace and build the binary using make.

To run the program use this command line.

`./RAYTRACE -a1 inputs/teapot.env`

in the raytrace folder. It takes a few seconds to run, due to the bugs.

In addition to the source code, the git repository contains the binary RAYTRACE original. This is the original program, without the introduced performance bugs, com-
piled with the same Makefile. 

You will find that the original binary runs much
faster, and your job is to figure out why. TIP: you can use -a10 instead of -a1
to make the programs take longer to run, potentially giving you more detailed profiling data.

The introduced bugs are well hidden, and the program is relatively large, making it extremely difficult to debug its poor performance without tools. You’ll want to use the tools discussed in class, and any other profiling tools you like, to track down these bugs. 

Recommended tools include time, perf record, valgrind --tool=callgrind and strace. Since it is quite a bit of code, you may also want to use grep to search for keywords in text files.



