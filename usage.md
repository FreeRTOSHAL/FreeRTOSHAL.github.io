---
layout: page
title: Usage
permalink: /usage/
---
Build under Windows 10
===============================

Install Windows-Subsystem for Linux.
Manual can be found [here][Win 10].

Install Ubuntu 18.04 LTS from Store and follow Ubuntu instructions.

Hint: Home folder can be found under: /c/Users/[username]/

A small Linux Terminal how to can be found [here][Terminal].

Build under Ubuntu 18.04 LTS 
===============================

Run this script:
{% highlight bash %}
sudo apt-get update; sudo apt-get install build-essential libncurses5-dev git;
{% endhighlight %}

Download ARM GNU Toolchain for Linux [here][ARM Toolchain]. Install the arm-none-eabi Toolchain form Repositories is not recommended!
ARM GCC Version 6 is not supported!

This small script for gcc-arm-none-eabi Version 8-2019-q4 download, extract and added toolchain to PATH:

{% highlight bash %}
wget https://developer.arm.com/-/media/Files/downloads/gnu-rm/8-2018q4/gcc-arm-none-eabi-8-2018-q4-major-linux.tar.bz2?revision=d830f9dd-cd4f-406d-8672-cca9210dd220?product=GNU%20Arm%20Embedded%20Toolchain,64-bit,,Linux,8-2018-q4-major # Download Toolchain
mv gcc-arm-none-eabi-*-*-*-*-*.tar.bz2* gcc-arm-none-eabi.tar.bz2 # rename File
tar -xf gcc-arm-none-eabi.tar.bz2 -C ~ # extract archive
mv gcc-arm-none-eabi-*-*-*-* gcc-arm-none-eabi # rename folder
echo "export PATH=$HOME/gcc-arm-none-eabi/bin:\$PATH" >> ~/.profile # add to PATH
# New Login needed or source .profile
{% endhighlight %}


Create Project
==============
For simple initialize a script was created. This can be downloaded [here][script]. Run this command to create a new project. A Git repo will be created automatically.

{% highlight bash %}
mkdir <projekt dir>
cd <project dir>
<script location>/createProcect.sh <projectname> master
{% endhighlight %}

After the creation small sample files will be created at this location plus submodules linkt to the project files at github.

The Build System use Kbuild. To configure the new project with a graphical interface use this command: 

{% highlight bash %}
make menuconfig
{% endhighlight %}

[docu]: /doxygen
[script]: https://github.com/FreeRTOSHAL/fhal-buildsystem/blob/master/createProject.sh
[ARM Toolchain]: https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads
[Win 10]: https://docs.microsoft.com/en-us/windows/wsl/install-win10
[Terminal]: http://www.linuxandubuntu.com/home/10-basic-linux-commands-that-every-linux-newbies-should-remember
