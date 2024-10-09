---
{"dg-publish":true,"dg-path":"General/manually install R packages.md","permalink":"/general/manually-install-r-packages/","tags":["Reference"],"created":"2024-09-18","updated":"2024-09-18"}
---


- #### If installing via typical `install.packages()` function fail, you may install the packages manually by loading it from a local directory
	- This could either be due to certain packages URL being blocked, connection failed or a certain PC not open to internet
	- Sometimes the packages has dependencies, so you will need to ensure you download all the necessary packages
- #### Steps to install the packages manually
	- ##### Identify the required packages
		- Try installing the intended R package via `install.package()` function
		- There will be error message thrown. Identify the missing packages from the this messages
			- see below where installing `vctrs_0.6.5.zip` failed
				```R
				trying URL 'https://cloud.r-project.org/bin/windows/contrib/4.4/vctrs_0.6.5.zip'  
				Error in download.file(url, destfile, method, mode = "wb", ...) :  
				cannot open URL 'https://cloud.r-project.org/bin/windows/contrib/4.4/vctrs_0.6.5.zip'  
				In addition: Warning messages:  
				1: In download.file(url, destfile, method, mode = "wb", ...) :  
				downloaded length 0 != reported length 14513  
				2: In download.file(url, destfile, method, mode = "wb", ...) :  
				cannot open URL 'https://cloud.r-project.org/bin/windows/contrib/4.4/vctrs_0.6.5.zip': HTTP status was '403 Forbidden'  
				Warning in download.packages(pkgs, destdir = tmpd, available = available,  :  
				download of package 'vctrs' failed
				```
	- ##### Download the R package required from CRAN website
		- Go to CRAN package website i.e. `https://cran.r-project.org/web/packages/dplyr/index.html`
		- replace `dplyr` with the package name you want to download e.g. `tibble` or `rlang`
	- ##### Install the package manually via R console
		- Go to `Packages > Install package(s) from local files...`
		- Browse and select the downloaded packages from the step earlier

## References
- [CRAN: Package dplyr (r-project.org)](https://cran.r-project.org/web/packages/dplyr/index.html)