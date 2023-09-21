## Patch to previous release
This submission is a patch to fix a bug that broke some code in v0.2.0 release.


## Test environments
* local Ubuntu 20.04.1 LTS, R 4.0.3
* local Windows 10 x64, R 4.0.3
* Ubuntu 16.04.6 LTS (on travis-ci), R 4.0.2

## R CMD check results (Local Ubuntu 20.04.1)
There were no ERRORs or WARNINGs or NOTEs.

## R CMD check results (Local Windows 10x64)
There were no ERRORs or WARNINGs. 
  
## Existing CRAN checks issues:
There was a NOTE being raised at https://cran.rstudio.com//web/checks/check_results_sfcr.html:
checking LazyData ... NOTE
  'LazyData' is specified without a 'data' directory
  
I fixed this issue by removing the line `LazyData: true` from the DESCRIPTION file since the sfcr package has no data/ directory.
