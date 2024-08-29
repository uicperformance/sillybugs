# The Sillybugs homework

The program in this repository contains a number of severe performance bugs. Clone the repository, then go to the folder `codes/apps/raytrace` and build the binary using `make`. You'll want to run this program on nodes.

To run the program use the following command in the `raytrace` directory:
```bash
./RAYTRACE -a1 inputs/teapot.env
```

It takes a few seconds to run due to all the bugs.

In addition to the source code, the git repository contains the original `RAYTRACE` binary (named `RAYTRACE_orig`). This is the original program, without the introduced performance bugs, com-
piled with *the same* Makefile.

You will find that the original binary runs much faster, and your job is to figure out why.
TIP: you can use `-a10` instead of `-a1` to make the programs take longer to run, potentially giving you more detailed profiling data.

The introduced bugs are well hidden, and the program is relatively large, making it extremely difficult to debug its poor performance without tools. You’ll want to use the tools discussed in class, and any other profiling tools you like, to track down these bugs. 

Recommended tools include `time`, `perf record`, `valgrind --tool=callgrind` and `strace`.
Since it is quite a bit of code, you may also want to use `grep` to search for keywords in text files.

### Performance Hints
Ideally, you want to get your `RAYTRACE` to perform close to as fast as `RAYTRACE_orig` (around 0.07 seconds). I'd say you've found almost all of the bugs if your program runs in under 0.085 seconds.

There are three main categories of bug(s), with the following runtime reductions to be gained from fixing each one:


| Category of Fix | Number of Bugs | Seconds Faster Fixed (than having nothing fixed) |
| --------------- | -------------- | ------------------------------------------------ |
| Unnamed #1      | 1              | 4.04s                                            |
| Unnamed #2      | 2              | 3.336s                                           |
| Unnamed #3      | 1              | 6.366s                                           |


