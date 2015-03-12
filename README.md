# TravisTests

Tests related to the proposed GSOC project "Test timings on Travis"

# Test 1 (Easy)
download <a href = https://github.com/tdhock/testthatQuantity>testthatQuantity</a> and run the <a href = https://github.com/tdhock/testthatQuantity/blob/master/R/testthatQuantity.R#L99-L126>example code</a> 
on one test file of a package of your choice.
<br>
<b>Approach</b>: Modified the (<a href="https://github.com/da-ta-vinci21/TravisTests/blob/master/test1.R#L99-L126">code-test1.R</a>) to run testthatQuantity's example code on package stringr's test-detect.R test file.
Obtained the plot given below, <br>
![stringr-detect-tests.png](string-detect-tests.png)
As can be seen, the recent commit has seen a slight increase in the runtime of test "special cases are correct" among other things. 

# Test 2 (Medium)
edit the test.file function so that it records the pass/fail status of each test. 
Hint: look at testthat::get_reporter().
<br>
<b>Approach</b>: <a href = "https://github.com/da-ta-vinci21/TravisTests/blob/master/test2.R#L151-L154">The relevant code (151-154, 195-199)</a>. 
Given the nature of the default reporter (StopReporter), the test will come to a halt whenever
an error takes place, thus if it progresses to completion that will be an indicator of the fact that no error
occured. Thus, in this case the status is update as "passed", otherwise the status would be set as "fail".





