# Install a R package

## Thought process

### Try a simple R package installation

```r
install.packages("energy")
```
Common issue: Dependencies are not always available at the given repo.

Solution to the issue: Download the source and install it manually.

Try a manual R package installation
Go to the R gsl package website and download the file locally:

```bash
wget https://cran.r-project.org/src/contrib/gsl_2.1-7.1.tar.gz
Then install the package in R:
```

```r
install.packages("gsl_2.1-7.1.tar.gz", type="source", repos=NULL)
```
Common issue: Dependent library is not always available on the system.

Solution to the issue: Let admin install the required library.

But it failed.

R gsl package needs systemwide gsl library. Google how to install gsl library in CentOS 7 (or a given Linux distro). Use the following command:

```r
sudo yum install -y gsl
```
Most cases are resolved at this point and we can revisit the installation process above.

Common issue: Dependent library is not always available in the repo.

Solution to the issue: Build the library from source.
```bash
R-gsl expects gsl library > 2.x
the gsl from the current repo is 1.15-13.el7
The gsl > 2.x will not be installed so we have to install gsl (system) library manually.

Install gsl library from source
```bash
wget https://mirror.ibcp.fr/pub/gnu/gsl/gsl-latest.tar.gz
tar xvfz gsl-latest.tar.gz
cd gsl-2.7.1
./configure
make
make install
```
This will install libgsl into /usr/local/lib. Though we have the required library, the installation may or may not be completed. This is an occasion where R is not aware of the library location. If it is the case, we have to declare the location of the library so that R will point out to the right place.

```bash
LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib/
export LD_LIBRARY_PATH
```
Then, try:

```r
install.packages("gsl")
install.packages("energy")
```

## Install multiple R versions in a server
Add EPEL repo
```bash
sudo yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
```

Specify R version
```bash
export R_VERSION=4.1.3
```
Download R precompiled binary
```bash
curl -O https://cdn.rstudio.com/r/centos-7/pkgs/R-${R_VERSION}-1-1.x86_64.rpm
```
Install the specified R
```bash
sudo yum install R-${R_VERSION}-1-1.x86_64.rpm
```
Verify the installed R
```bash
/opt/R/${R_VERSION}/bin/R --version
```
Optional - add R path to PATH variable
```bash
export PATH=/opt/R/${R_VERSION}/bin/:$PATH
```
