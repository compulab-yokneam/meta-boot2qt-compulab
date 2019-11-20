# Quick Start Guide

Supported CompuLab Machines:
* `cl-som-imx8`
* `cl-som-imx8x`
* `ucm-imx8m-mini`

# Prepare Boot2Qt build environment
<pre>
mkdir -p ~/Qt/sources; cd ~/Qt
git clone https://github.com/compulab-yokneam/meta-boot2qt-compulab.git sources/meta-boot2qt-compulab
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
