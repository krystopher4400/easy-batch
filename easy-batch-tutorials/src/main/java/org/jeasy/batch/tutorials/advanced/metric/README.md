# Tutorial: Contributing custom metrics

## Description

The goal of this tutorial is to write a listener that contributes a custom metric to job report.
We would like to add a metric for the processing time average of all records.

We will write a class that implements:

* The `PipelineListener` to gather record processing time and calculate the average
* The `JobListener` to get access to the job report and add the custom metric

## Run the tutorial

First, make sure you have already downloaded the source code and built the tutorials
as described in the [quick start](https://github.com/j-easy/easy-batch/tree/master/easy-batch-tutorials#quick-start) section.

### From the command line

Open a terminal and run the following command:

```
$>mvn exec:java -PrunCustomMetricTutorial
```

### From Your IDE

* Navigate to the `org.jeasy.batch.tutorials.advanced.metric` package
* Run the `org.jeasy.batch.tutorials.advanced.metric.Launcher` class without any argument

## Sample output

Additional metrics are shown after core metrics in the job report. In this tutorial, it is the `Record processing time average` metric :

```
Job Report:
===========
Name: job
Status: COMPLETED
Parameters:
	Batch size = 1
	Error threshold = N/A
	Jmx monitoring = false
	Batch scanning = false
Metrics:
	Start time = 2020-02-02T18:20:08.113
	End time = 2020-02-02T18:20:09.916
	Duration = 1sec 803ms
	Read count = 2
	Write count = 2
	Filter count = 0
	Error count = 0
	Record processing time average (in ms) = 893.0
```
