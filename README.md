# Quick Start Guide

|NOTE|This development branch has not yet been released/supported officially by CompuLab.|
|---|---|

Supported CompuLab Machines:
* `ucm-imx8m-plus`

# Set a desire machine
* `ucm-imx8m-plus`
<pre>
export MACHINE=ucm-imx8m-plus
</pre>

# Prepare Boot2Qt build environment
<pre>
source <(curl -L https://raw.githubusercontent.com/compulab-yokneam/meta-boot2qt-compulab/mickledore/tools/run.me)
</pre>

# Create a Boot2Qt image
* For Boot to Qt for embedded Linux targets, run the build as follows:
<pre>
bitbake b2qt-embedded-qt6-image
bitbake meta-toolchain-b2qt-embedded-qt6-sdk
</pre>

# Links
https://doc.qt.io/Boot2Qt/b2qt-how-to-create-b2qt-image.html
