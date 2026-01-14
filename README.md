# Quick Start Guide

|NOTE|This development branch has not yet been released/supported officially by CompuLab.|
|---|---|

## Setup Yocto environment

* WorkDir

  ```
  mkdir boot2qt-compulab && cd boot2qt-compulab
  ```

* CompuLab Yocto build environment</br>
Follow the instructions of the specific machine and prepare the Yocto Build environemt:

  NXP SoC | Build Environment Manual|
  --- | --- |
  `i.MX8MP` | [meta-bsp-imx8mp](https://github.com/compulab-yokneam/meta-bsp-imx8mp/tree/scarthgap-2.2.0)
  `i.MX93` | [meta-bsp-imx9](https://github.com/compulab-yokneam/meta-bsp-imx9/blob/scarthgap)

* Update the created Yocto Build environment with the Boot2Qt support:
  ```
  cd ${BUILDDIR}
  source <(curl -L https://raw.githubusercontent.com/compulab-yokneam/meta-boot2qt-compulab/boot2qt-addon/tools/run.me)
  ```

## Build Procedure
   
* Create ``b2qt-embedded-qt6-image`` image:
  ```
  bitbake -k b2qt-embedded-qt6-image
  ```
* Create ``Boot2Qt SDK`` for the host machine:
  ```
  bitbake meta-toolchain-b2qt-embedded-qt6-sdk
  ```

## Boot2Qt resources

* [How to create a Boot to Qt image](https://doc.qt.io/Boot2Qt/b2qt-how-to-create-b2qt-image.html)
