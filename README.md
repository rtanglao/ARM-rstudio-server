# ARM-rstudio-server
Build script for rstudio-server on:
* ARM64 Windows 10 
* Lenovo C630 Yoga 
* Windows 10 Insider Build Fast Ring `Microsoft Windows [Version 10.0.18999.1]`
* WSL 1 (WSL 2 doesn't work on Windows 10 ARM64 ! Except for I guess :-) The Samsung Book 2 and the future Surface X

This is built on the excellent work of [jrowen/ARM-rstudio-server](https://github.com/jrowen/ARM-rstudio-server) which was built on the excellent work of [dashaub/ARM-RStudio](https://github.com/dashaub/ARM-RStudio).

## Build
This script has been used to successfully build RStudio Server 1.2.5001

The commands below can be used to build the server:

```bash
bash -x build_rstudio.sh
/usr/sbin/rstudio-server start
```
The build took about 2 hours to complete.

The `VERS` variable in the script can be updated to build different versions of the server.  The latest version number and be found on the rstudio server [download page](https://www.rstudio.com/products/rstudio/download-server/), and note that this will likely differ from the latest desktop version.

## Launching RStudio Server
After the server has been built and installed, the easiest way to start the server from a WSL  using the commands below:

```bash
sudo  /usr/sbin/rstudio-server start
```
Finally, from a new Firefox (or Chrome :-)) tab navigate to `localhost:8787` and log in using your WSL credentials.

## Contributions
Please don't hesitate to file an issue if you run into problems, and pull requests are welcome.
