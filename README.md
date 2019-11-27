# Quick Start Guide
The purpose of this page is to provide a step-by-step procedure for creating Boot2Qt images for the CompuLab SoMs.

Supported CompuLab Machines:
* `cl-som-imx8`
* `cl-som-imx8x`
* `ucm-imx8m-mini`

# Prereqisites
Make sure that the build machine meats the Boot2Qt build host [requirements](https://doc.qt.io/QtForDeviceCreation/qtee-custom-embedded-linux-image.html#requirements).

Install the dependecies for the Yocto tools:
* Add the `git-lfs` repository:
<pre>
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
</pre>

* Install the debian packages:
<pre>
sudo apt-get install --yes gawk curl git-core git-lfs diffstat unzip p7zip-full texinfo \
gcc-multilib build-essential chrpath libsdl1.2-dev xterm gperf bison g++-multilib 
</pre>

* Initialize the `git-lfs`:
<pre>
git-lfs install
</pre>

# Prepare Boot2Qt build environment
<pre>
mkdir -p ~/Qt/sources; cd ~/Qt
git clone -b devel https://github.com/compulab-yokneam/meta-boot2qt-compulab.git sources/meta-boot2qt-compulab
</pre>

# Set a desire machine
* `cl-som-imx8`
<pre>
export MACHINE=cl-som-imx8
</pre>

# Issue the CompuLab setup script
This script creates the build environment for the ${MACHINE}
<pre>
source sources/meta-boot2qt-compulab/tools/setup-b2qt-env
</pre>

# Create a Boot2Qt image
* For Boot to Qt for embedded Linux targets, run the build as follows:
<pre>
bitbake b2qt-embedded-qt5-image
</pre>

* For Qt Automotive targets, run the build as follows:
<pre>
bitbake b2qt-automotive-qt5-image
</pre>
