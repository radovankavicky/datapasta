## Test Environments

### r-hub
Debian Linux, R-devel, GCC (debian-gcc-devel)
Debian Linux, R-release, GCC (debian-gcc-release)
Ubuntu Linux 16.04 LTS, R-release, GCC (ubuntu-gcc-release)
Windows Server 2008 R2 SP1, R-release, 32/64 bit (windows-x86_64-release)
Windows Server 2008 R2 SP1, R-devel, 32/64 bit (windows-x86_64-devel)

### local installations
Mac OSX El Capitan 10.11.14, R-release 3.3.1
Microsoft Windows 7 Enterprise SP1, R-release 3.3.2 

## R CMD check results

0 errors | 2 warnings | 2 notes

NOTES:

* Packages in Depends field not imported from:
     ‘clipr’ ‘rstudioapi’

`Depends` in DESCRIPTION represents the nature of the relationship, however functions from these packages are called using namespace operator `::`.

* tribble_paste: no visible global function definition for
     '.rs.readUiPref'
   vector_paste_vertical: no visible global function definition for
     '.rs.readUiPref'
   Undefined global functions or variables:
     .rs.readUiPref
     
This function is in the global environment when running RStudio. RStudio addins in this package use this function.
    
WARNINGS:

* On Mac OSX only: "Warning: package ‘clipr’ was built under R version 3.3.2"

R-release 3.3.1 is the highest available for OSX El Capitan. Tests still passed without issue.

* On Windows 7 only: "Warning 'qpdf is needed for checks on size reduction of pdfs'"

I understand the absence of this binary means that this particular CMD check could not be performed on Windows 7. I do not believe it is hiding a package issues due to evidence from other platforms.

## Downstream dependencies

There are currently no downstream dependencies for this package