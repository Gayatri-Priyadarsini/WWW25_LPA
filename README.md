# Least-Privilege-Access-for-Persistent-Storage-Mechanisms-in-Web-Browsers
This repository is discuses the changes required in mozilla nightly build proposed in the paper titled "Least Privilege Access for Persistent Storage Mechanisms in Web Browsers" 

You can find our firefox build at https://doi.org/10.5281/zenodo.14822718. This can then be used to run the firefox browser by `./mach run`. 



## Set-up
For our work, we instrumented the firefox codebase in order to integrate fine grained access control for third-party scripts, which otherwise have full control over first-party storage. 

To replicate our work, you can setup to build firefox on your machine by following the instructions from this tutorial: https://firefox-source-docs.mozilla.org/setup/index.html . We used "Nightly Firefox version 127.0a1" for our work. 

For crawling the 10,000 websites, we used marionette testing environment which visited the websites and collected the logs required for assessing the third-party accesses to the first-party storage. This script can be found in the `scripts` folder.   

## Usage

You can build the firefox code with the following command:
```bash
./mach build
```
You can run the browser with the command:
```bash
./mach run
```

