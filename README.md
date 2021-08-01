Samsung has removed the download for some (vintage) devices including most of the trlte variants. The initial
tag is an untouched upload of the kernel.zip for the SM-N910V. [Mirror](https://www.androidfilehost.com/?fid=14943124697586354076) of the original zip from Samsung.

I'm not a developer nor do I have any formal education regarding Android development (or anything else).
These notes are here just for convenience. Some information could be inaccurate and I welcome any input/corrections.

* Repo & Host Specs 
      
      * Linux kernel v.3.10.40    * Distro = LMDE 4 Debbie
      * Device = trltevzw         * Base = Debian 10.2
      * Firmware = N910VVRU2CQL1
      * Toolchain = arm-eabi-4.8
      
**Build Environment Setup**

* openjdk-8-jre

      sudo apt-get install openjdk-8-jre
      
May need this:

      deb http://ftp.us.debian.org/debian stretch main

      

* Build Tools

      sudo apt-get install git-core ccache automake lzop bison gperf build-essential zip curl zlib1g-dev g++-multilib python3-networkx libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev liblz4-tool make optipng gnupg flex libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig

**Kernel prebuilt toolchains**
* Google's prebuilt toolchain:

      git clone https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8
      
* UberTC's prebuilt toolchain:

      git clone https://bitbucket.org/UBERTC/arm-eabi-4.8.git

* Building with CCACHE

      export USE_CCACHE=1
      export CCACHE_EXEC=$(command -v ccache)
    
**Python Errors**

[Initializing a repo client](https://source.android.com/setup/build/downloading#initializing-a-repo-client)--Link to Android source. Fix near bottom of the page.

Above fix works. Just in case it doesn't, installing these pkgs should work.

    sudo apt-get install python2.7 python-all

**Links to all info on Android. Plus some ones that interest me.** 
* [Android Source](https://source.android.com/) -- All the answers are here.
* [Anykernel3](https://github.com/osm0sis/AnyKernel3.git) && [Android Image Kitchen](https://github.com/osm0sis/Android-Image-Kitchen.git) from @osm0sis rep0s
* [Magisk](https://github.com/topjohnwu/Magisk.git) -where all the Magisk happens.
* [OpenGapps](https://github.com/opengapps/opengapps.git) -my new obsession
* [AOSP-Mirror Links](https://aosp-mirror.github.io/)
* [XDA](https://www.xda-developers.com/)
* [Samsung Source Code](https://opensource.samsung.com)
* [Manpages for xz compression](http://http://manpages.org/xz)
* [Kernel.org commit tree v3.10.y](https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git/log/?h=linux-3.10.y)
* [Google kernel source for v3.10.y](https://kernel.googlesource.com/pub/scm/linux/kernel/git/stable/linux/+/refs/heads/linux-3.10.y)
* [Repo and git references](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/manifest-format.md#XML-File-Format)
* [All things Repo](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/README.md)
