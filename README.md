# Quick Start Guide


|NOTE|This development branch has not yet been released/supported officially by CompuLab.|
|---|---|


Supported CompuLab Machines:
* `ucm-imx8m-plus`

https://raw.githubusercontent.com/compulab-yokneam/meta-boot2qt-compulab/mickledore/README.md

# Prepare Boot2Qt build environment
<pre>
bash <(curl -L https://raw.githubusercontent.com/compulab-yokneam/meta-boot2qt-compulab/mickledore/tools/run.me)
</pre>

# Set a desire machine
* `ucm-imx8m-plus`
<pre>
export MACHINE=ucm-imx8m-plus
</pre>

# Issue the CompuLab setup script
This script creates the build environment for the ${MACHINE}
<pre>
source compulab-setup-env -b build-b2qt-${MACHINE}
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
