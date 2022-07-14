# PSP-DEV
My initial PSP dev environment

# Sources
Based on [This article](https://victorbush.com/2020/11/psp-dev-windows/). Except uses [this](https://github.com/ticky/docker-pspdev) docker image.

I could not get the docker image in the article to work for love nor money no matter what I tried.

# Structure

* `./references` - Collection of PSP development resources.
* `./pspsdk` - Contains the PSPSDK repository, used for reference.
* `./pspdev-socker` - Contains the docker image repository, used for reference.
* `./ppsspp` - Contains the PPSSPP emulator. VSCode tasks reference this. Not checked in as its massive.
* `./projects` - Contains individual projects.

# How to use

* Clone this repo.
  * This uses sub modules execute `git clone --recurse-submodules https://github.com/ste2425/PSP-DEV.git` to include them in the clone
* Install [Docker](https://www.docker.com/products/docker-desktop/)
* Download and extract the [PPSSPP](https://www.ppsspp.org/) emulator to the root of the `ppsspp` folder.
* Within each project folder execute the various batch scripts as needed.
  * *psp-make.bat* - Will build the project
  * *psp-clean.bat* - Will clean the project (useful if experiencing odd bugs even though the code compiles)
  * *psp-rebuild.bat* - Will re-build the project
* There are VSCode tasks for the above build scripts
  * The task `run-sample` will launch the sample game in the `PPSSPP` emulator. Be sure to do a build first.

# TLDR;
To see something happen for the first time execute the following VSCode tasks in order.

`build-sample` then `run-sample`.

It *should* just be plug and play.