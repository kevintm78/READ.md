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
    
**Python Errors**

[Initializing a repo client](https://source.android.com/setup/build/downloading#initializing-a-repo-client)--Link to Android source. Fix near bottom of the page.

Above fix works. Just in case it doesn't, installing these pkgs should work.

    sudo apt-get install python2.7 python-all

__[lynx.md](https://github.com/kevintm78/READ.md/files/7072568/lynx.md)
.bashrc additions__

```
export ALLOW_FILE_DISCOVERY=1
export ANDROID_SDK_ROOT="$HOME/Android/Sdk"
export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx4g"  #this is for my lack of ram
export OUT_DIR_COMMON_BASE=""$HOME/path/me/the/salt"
export USE_CCACHE=1  #Android 9 and below just needs this one
export CCACHE_EXEC=$(command -v ccache)  #Android 10+ requires this line as well
