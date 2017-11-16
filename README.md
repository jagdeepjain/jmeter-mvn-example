# jmeter-mvn-example
Executing Jmeter tests using in memory jmeter.

## Command to execute
```
mvn test
```

## Results
```
D:\github\jmeter-mvn-example>mvn test
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building JMeter Maven Example 1.0-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO]
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ jmeter-mvn-example ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory D:\github\jmeter-mvn-example\src\main\resources
[INFO]
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ jmeter-mvn-example ---
[INFO] No sources to compile
[INFO]
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ jmeter-mvn-example ---
[WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory D:\github\jmeter-mvn-example\src\test\resources
[INFO]
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ jmeter-mvn-example ---
[INFO] No sources to compile
[INFO]
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ jmeter-mvn-example ---
[INFO] No tests to run.
[INFO]
[INFO] --- jmeter-maven-plugin:1.10.1:jmeter (jmeter-tests) @ jmeter-mvn-example ---
[INFO]
[INFO] -------------------------------------------------------
[INFO]  P E R F O R M A N C E    T E S T S
[INFO] -------------------------------------------------------
[INFO]
[INFO]
[info]
[debug] JMeter is called with the following command line arguments: -n -t D:\github\jmeter-mvn-example\src\test\jmeter\GoogleSearch.jmx -l D:\github\jmeter-mvn-example\target\jmeter\results\20171116-GoogleSearch.jtl -d D:\github\jmeter-mvn-example\target\jmeter -j D:\github\jmeter-mvn-example\target\jmeter\logs\GoogleSearch.jmx.log
[info] Executing test: GoogleSearch.jmx
[debug] Creating summariser <summary>
[debug] Created the tree successfully using D:\github\jmeter-mvn-example\src\test\jmeter\GoogleSearch.jmx
[debug] Starting the test @ Thu Nov 16 16:28:42 IST 2017 (1510829922189)
[debug] Waiting for possible shutdown message on port 4445
[debug] summary =      1 in     3s =    0.4/s Avg:  2238 Min:  2238 Max:  2238 Err:     0 (0.00%)
[debug] Tidying up ...    @ Thu Nov 16 16:28:45 IST 2017 (1510829925039)
[debug] ... end of run
[info] Completed Test: GoogleSearch.jmx
[info]
[debug] JMeter is called with the following command line arguments: -n -t D:\github\jmeter-mvn-example\src\test\jmeter\JDBCTestPlan.jmx -l D:\github\jmeter-mvn-example\target\jmeter\results\20171116-JDBCTestPlan.jtl -d D:\github\jmeter-mvn-example\target\jmeter -j D:\github\jmeter-mvn-example\target\jmeter\logs\JDBCTestPlan.jmx.log
[info] Executing test: JDBCTestPlan.jmx
[debug] Creating summariser <summary>
[debug] Created the tree successfully using D:\github\jmeter-mvn-example\src\test\jmeter\JDBCTestPlan.jmx
[debug] Starting the test @ Thu Nov 16 16:28:46 IST 2017 (1510829926071)
[debug] Waiting for possible shutdown message on port 4445
[debug] summary =      1 in   0.1s =    7.2/s Avg:    53 Min:    53 Max:    53 Err:     0 (0.00%)
[debug] Tidying up ...    @ Thu Nov 16 16:28:46 IST 2017 (1510829926411)
[debug] ... end of run
[info] Completed Test: JDBCTestPlan.jmx
[INFO]
[INFO] Test Results:
[INFO]
[INFO] Tests Run: 2, Failures: 0
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 10.627 s
[INFO] Finished at: 2017-11-16T16:28:46+05:30
[INFO] Final Memory: 17M/304M
[INFO] ------------------------------------------------------------------------

D:\github\jmeter-mvn-example>
```

## Logs

Check this line in the log to make sure that JDBC test actually ran properly. 

*2017/11/16 16:28:46 INFO  - jmeter.util.BeanShellTestElement: Number of users in the database # 1*.

```
D:\github\jmeter-mvn-example>type D:\github\jmeter-mvn-example\target\jmeter\logs\JDBCTestPlan.jmx.log
2017/11/16 16:28:45 INFO  - jmeter.util.JMeterUtils: Setting Locale to en_IN
2017/11/16 16:28:45 INFO  - jmeter.JMeter: Loading user properties from: D:\github\jmeter-mvn-example\target\jmeter\bin\user.properties
2017/11/16 16:28:45 INFO  - jmeter.JMeter: Loading system properties from: D:\github\jmeter-mvn-example\target\jmeter\bin\system.properties
2017/11/16 16:28:45 INFO  - jmeter.JMeter: Copyright (c) 1998-2015 The Apache Software Foundation
2017/11/16 16:28:45 INFO  - jmeter.JMeter: Version 2.13 r1665067
2017/11/16 16:28:45 INFO  - jmeter.JMeter: java.version=1.8.0_131
2017/11/16 16:28:45 INFO  - jmeter.JMeter: java.vm.name=Java HotSpot(TM) 64-Bit Server VM
2017/11/16 16:28:45 INFO  - jmeter.JMeter: os.name=Windows 10
2017/11/16 16:28:45 INFO  - jmeter.JMeter: os.arch=amd64
2017/11/16 16:28:45 INFO  - jmeter.JMeter: os.version=10.0
2017/11/16 16:28:45 INFO  - jmeter.JMeter: file.encoding=Cp1252
2017/11/16 16:28:45 INFO  - jmeter.JMeter: Default Locale=English (India)
2017/11/16 16:28:45 INFO  - jmeter.JMeter: JMeter  Locale=English (India)
2017/11/16 16:28:45 INFO  - jmeter.JMeter: JMeterHome=D:\github\jmeter-mvn-example\target\jmeter
2017/11/16 16:28:45 INFO  - jmeter.JMeter: user.dir  =D:\github\jmeter-mvn-example\target\jmeter\bin
2017/11/16 16:28:45 INFO  - jmeter.JMeter: PWD       =D:\github\jmeter-mvn-example\target\jmeter\bin
2017/11/16 16:28:45 INFO  - jmeter.JMeter: IP: 10.8.42.29 Name: DESKTOP-U0HP063 FullName: 10.8.42.29
2017/11/16 16:28:45 INFO  - jmeter.services.FileServer: Default base='D:\github\jmeter-mvn-example\target\jmeter\bin'
2017/11/16 16:28:45 INFO  - jmeter.services.FileServer: Set new base='D:\github\jmeter-mvn-example\src\test\jmeter'
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: Testplan (JMX) version: 2.2. Testlog (JTL) version: 2.2
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: Using SaveService properties file encoding UTF-8
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: Using SaveService properties file version 1656252
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: Using SaveService properties version 2.8
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: All converter versions present and correct
2017/11/16 16:28:45 INFO  - jmeter.save.SaveService: Loading file: D:\github\jmeter-mvn-example\src\test\jmeter\JDBCTestPlan.jmx
2017/11/16 16:28:46 INFO  - jmeter.JMeter: Creating summariser <summary>
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Listeners will be started after enabling running version
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: To revert to the earlier behaviour, define jmeterengine.startlistenerslater=false
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Running the test!
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleEvent: List of sample_variables: []
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleEvent: List of sample_variables: []
2017/11/16 16:28:46 INFO  - jmeter.engine.util.CompoundVariable: Note: Function class names must contain the string: '.functions.'
2017/11/16 16:28:46 INFO  - jmeter.engine.util.CompoundVariable: Note: Function class names must not contain the string: '.gui.'
2017/11/16 16:28:46 INFO  - jmeter.JMeter: Running test (1510829926271)
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Starting ThreadGroup: 1 : Thread Group
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Starting 1 threads for group Thread Group.
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Thread will continue on error
2017/11/16 16:28:46 INFO  - jmeter.threads.ThreadGroup: Starting thread group number 1 threads 1 ramp-up 1 perThread 1000.0 delayedStart=false
2017/11/16 16:28:46 INFO  - jmeter.threads.JMeterThread: jmeterthread.startearlier=true (see jmeter.properties)
2017/11/16 16:28:46 INFO  - jmeter.threads.JMeterThread: Running PostProcessors in forward order
2017/11/16 16:28:46 INFO  - jmeter.threads.ThreadGroup: Started thread group number 1
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: All thread groups have been started
2017/11/16 16:28:46 INFO  - jmeter.threads.JMeterThread: Thread started: Thread Group 1-1
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleResult: Note: Sample TimeStamps are START times
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleResult: sampleresult.default.encoding is set to ISO-8859-1
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleResult: sampleresult.useNanoTime=true
2017/11/16 16:28:46 INFO  - jmeter.samplers.SampleResult: sampleresult.nanoThreadSleep=5000
2017/11/16 16:28:46 INFO  - jmeter.util.BeanShellTestElement: Number of users in the database # 1
2017/11/16 16:28:46 INFO  - jmeter.threads.JMeterThread: Thread is done: Thread Group 1-1
2017/11/16 16:28:46 INFO  - jmeter.threads.JMeterThread: Thread finished: Thread Group 1-1
2017/11/16 16:28:46 INFO  - jmeter.engine.StandardJMeterEngine: Notifying test listeners of end of test
2017/11/16 16:28:46 INFO  - jmeter.reporters.Summariser: summary =      1 in   0.1s =    7.2/s Avg:    53 Min:    53 Max:    53 Err:     0 (0.00%)

D:\github\jmeter-mvn-example>
```
