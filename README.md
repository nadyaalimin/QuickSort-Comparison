# Quicksort-Comparison

Operation System  UPH 2017/1028 - Parallel vs Singular Quicksort Comparison

This repository is created to compare the time needed for sequential and parallel quicksort on Ubuntu, the quicksort file is build on C programming language and sample datas are provided in txt file format.

# Dependency
[GCC](https://linuxconfig.org/how-to-install-gcc-the-c-compiler-on-ubuntu-18-04-bionic-beaver-linux)

## Installation/running instruction
- Download the files on folder "Quicksort".
- Open terminal and get to the directory path (the place where you put the files).
- Type on "g++ quicksort.c -o quicksort -fopenmp" to compile the sequential quicksort. While "g++ quicksort_parallel.c -o quicksort_parallel -fopenmp -fpermissive" for parallel quicksort. Those command are written without quotations marks.
- After successfully compiling the file, execute it with the command "./quicksort (samplesize).txt" without quotes. (samplesize) will be changed with 10, 100, 1000, or 10000. Remember to delete the brackets.

## Sample Input and Time Data
The test is done by both sequential and parallel quicksort programs to find the average time taken to finish quicksorting with sample size txt file given (10, 100, 1000, 10000) and I take 4 times test taken.

### Sequential Quicksort

|Sample     |Test 1    |Test 2    |Test 3    |Test 4    |Average Time|
|-----------|----------|----------|----------|----------|------------|
|10         |0.000002 s|0.000002 s|0.000002 s|0.000002 s|0.00000200 s|
|100        |0.000024 s|0.000025 s|0.000025 s|0.000025 s|0.00002475 s|
|1000       |0.001172 s|0.001000 s|0.001000 s|0.001157 s|0.00108225 s|
|10000      |0.096854 s|0.096854 s|0.074262 s|0.075319 s|0.08582225 s|

### Parallel Quicksort

|Sample     |Test 1     |Test 2     |Test 3     |Test 4     |Average Time |
|-----------|-----------|-----------|-----------|-----------|-------------|
|10         |0.0031880 s|0.0032980 s|0.0026960 s|0.0039150 s|0.003274250 s|
|100        |0.0516770 s|0.0511020 s|0.0492840 s|0.0522280 s|0.051072750 s|
|1000       |1.1557710 s|1.0199490 s|1.0036200 s|0.9887030 s|1.040360750 s|
|10000      |7.1169880 s|17.218164 s|30.900057 s|5.8697420 s|15.27623775 s|

## Explanation and Comparison
The data above shows the time needed for quicksorting done with Sequential and Parallel Quicksort. The data compared can be seen below, with the orange line as parallel quicksort while blue line as sequential quicksort.

### Singular Quicksort vs Parallel Quicksort Time Comparison

|Sample     |Sequential  |Parallel     |
|-----------|------------|-------------|
|10         |0.00000200 s|0.003274250 s|
|100        |0.00002475 s|0.051072750 s|
|1000       |0.00108225 s|1.040360750 s|
|10000      |0.08582225 s|15.27623775 s|

![Quicksort Graph](https://github.com/nadyaalimin/QuickSort-Comparison/blob/master/chart.png)<br>

### Result analysis

From the result above, we can see that sequential quicksort is faster than parallel quicksort. The sample size and the test may affect the result. According to Tinku Singh and Durgesh Kumar Srivastava, When working with parallel quicksort there are some jobs that should be done such as parallelism job, spawning thread, synchronization time, etc. On the other hand, sequential sort is just doing the sort normally with algorithm given without any supplement on parallelism tasks.

## Authors

* **Nadya Natasha Alimin** - Informatics UPH 2017

## Acknowledgements
- [Quicksort Program](https://github.com/markwkm/quicksort)
- [Guidebook Quicksort Algorithm](https://pdfs.semanticscholar.org/cba9/770c4fad941fe5e501539525953a242a36f8.pdf)
