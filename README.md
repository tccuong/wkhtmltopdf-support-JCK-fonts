# wkhtmltopdf-support-CJK-fonts
By default package wkhtmltopdf not support CJK (Asian fonts). This document to help you can add the Asian fonts for wkhtmltopdf.
## System requirements:
- EC2 2018.03 release
## Install wkhtmltopdf
```
$ cd ~
$ wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.3/wkhtmltox-0.12.3_linux-generic-amd64.tar.xz
tar vxf wkhtmltox-0.12.3_linux-generic-amd64.tar.xz
$ cp wkhtmltox/bin/wk* /usr/local/bin/
```
Check version wkhtmltopdf
```
$ wkhtmltopdf --version
wkhtmltopdf 0.12.3 (with patched qt)
```
Generate sample pdf 
```
$ wkhtmltopdf https://majestic.cloud majestic.pdf
```
If has error missing libpng-1.5.15, to do below commands
```
$ wget https://sourceforge.net/projects/libpng/files/libpng15/older-releases/1.5.15/libpng-1.5.15.tar.gz/download -O libpng-1.5.15.tar.gz
$ tar -zxvf libpng-1.5.15.tar.gz
$ cd libpng-1.5.15
$ ./configure --prefix=/usr
$ sudo make install
$ sudo yum install -y libtiff
```
## Install Asian fonts
```
$ sudo yum install wqy-zenhei-fonts
$ sudo fc-cache -f -v
```
End work and enjoy!

