# Find unique coverage of two program runs
The purpose of this script is to compare code coverage of two program runs, stored in two folders. The two folders should contain the same source code, but the coverage data may be different in each. The difference in coverage can be due to running two different test suites.

The tool will use gcovr to collect coverage information. Then it will display the following:

* Total number of unique lines covered by each run
* Number of unique lines covered in each file source
* Line numbers in each file that are uniquely covered

## Prerequisites

* Python 3.8
* gcovr

## How to run

Before running, make sure the two source folders are present in the root directory, and contain the gcovr instrumented code and data.

Next, run the following command:
```
$ python3 unique_lines.py --source-1 run-1 --source-2 run-2 --summary
```

In the above example `run-1` stores the first target program run, and `run-2` stores the second target program run.

`--summary` is an optional argument. You can omit it if you want to get coverage line numbers.

The output is displayed in a json like format.

