# TravisTests

Tests related to the proposed GSOC project "Test timings on Travis"

# Test 1 (Easy)
<i>download <a href = https://github.com/tdhock/testthatQuantity>testthatQuantity</a> and run the <a href = https://github.com/tdhock/testthatQuantity/blob/master/R/testthatQuantity.R#L99-L126>example code</a> 
on one test file of a package of your choice.</i>
<br>
<b>Approach</b>: Modified the code (<a href="https://github.com/da-ta-vinci21/TravisTests/blob/master/test1.R#L99-L126">(test1.R)</a>) to run testthatQuantity's example code on package stringr's test-detect.R test file.
Obtained the plot given below, <br>
<img src = "https://raw.githubusercontent.com/da-ta-vinci21/TravisTests/master/stringr-detect-tests.png"/ alt = "strinr-detect-tests.png">
<br>
As can be seen, the recent commit has seen a slight increase in the runtime of test "special cases are correct" among other things. 

# Test 2 (Medium)
<i>edit the test.file function so that it records the pass/fail status of each test.
Hint: look at testthat::get_reporter().</i>
<br>
<b>Approach</b>: <a href = "https://github.com/da-ta-vinci21/TravisTests/blob/master/test2.R#L151-L154">The relevant code (151-154, 195-199)</a>. 
Given the nature of the default reporter (StopReporter), the test will come to a halt whenever
an error takes place, thus if it progresses to completion that will be an indicator of the fact that no error
occured. Thus, in this case the status is update as "passed", otherwise the status would be set as "fail".

# Test 3 (Hard)
<i>the current code in test.file and test.commit assumes that the tests specified in tfile do not change across different git commits, which may or may not be true. Implement a test.commits(tfile, SHA1.vec) function which saves the tests in tfile and runs them against all commits specified in the SHA1.vec character vector.</i>
<br>
<b>Approach</b>: <a href = "https://github.com/da-ta-vinci21/TravisTests/blob/master/test3.R#L201-L228">The relevant code (201-228)</a>.
Saved current version of test code from the given tfile before checking it against the package versions specified by the SHA1 vector. Plotted the graph same similarly as done in the previous version.
