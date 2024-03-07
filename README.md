# covr-test
Testing an issue with running `covr::codecov` in package using `vetiver`

The following code runs with no issues using the basic package skeleton, but as 
soon as `vetiver` is added as a dependency the test fails with an error message,
 included below.

```
covr::codecov(
            quiet = FALSE,
            clean = FALSE
          )
```
The error message:

```
> # This file is part of the standard setup for testthat.
> # It is recommended that you do not modify it.
> #
> # Where should you do additional test configuration?
> # Learn more about the roles of various files in:
> # * https://r-pkgs.org/testing-design.html#sec-tests-files-overview
> # * https://testthat.r-lib.org/articles/special-files.html
> 
> library(testthat)
> library(covr.test)
Error in loadNamespace(x) : there is no package called 'covr'
> 
> test_check("covr.test")
Error in loadNamespace(x) : there is no package called 'withr'
Calls: test_check ... loadNamespace -> withRestarts -> withOneRestart -> doWithOneRestart
Execution halted
Error in loadNamespace(x) : there is no package called 'covr'
Calls: <Anonymous> ... loadNamespace -> withRestarts -> withOneRestart -> doWithOneRestart
```
