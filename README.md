* Build Tools

      sudo apt install git-core ccache automake lzop bison gperf build-essential zip curl zlib1g-dev g++-multilib python3-networkx libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev liblz4-tool make optipng gnupg flex libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig libncurses5 libtinfo5
      
* [AOSP guide](https://source.android.com/setup/build/initializing) for setting up your build environment.
________________________________________________________________________________________________________________________________________________________

## Troubleshoot my common problems

**git errors**
* "fatal: remote origin already exists." - [Solution](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories)


**Fix for "/usr/bin/env 'python' no such file or directory"**

* [AOSP suggestion](https://source.android.com/setup/build/downloading#initializing-a-repo-client)
  If your Ubuntu 20.04.2 LTS is a newly installed (vs. upgraded) Linux version:

      sudo ln -s /usr/bin/python3 /usr/bin/python

* Above fix works with certain distros, but if not try:

      sudo apt install python-is-python2

* python-all was needed once, but probably just a fluke...

      sudo apt install python-all
_________________________________________________________________________________________________________________________________________________________

#### Environment Variables:
  *Warning-These could be as inaccurate as everything else in this readme.*

    export USE_CCACHE=1                                     #Android 9 and below just needs this one
    export ANDROID_SDK_ROOT="$HOME/Android/Sdk"             #Path to some dumb kevin. For when I get lost.
    export OUT_DIR_COMMON_BASE=""$HOME/path/to/salvation"   #Set this for common out directory for Android builds
    export PATH="$HOME/android-studio/jre/bin:$PATH"        #This is needs to set for building Magisk
    export PATH="$HOME/.bin:$PATH"                          #This is where I install repo.
    export ALLOW_FILE_DISCOVERY=1                           #Self explanatory
    export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx4g"  #this is for my lack of ram

    export CCACHE_EXEC=$(command -v ccache)                 #Android 10+ only??!!
________________________________________________________________________________________________________________________________________________________

**@osm0sis' rep0s, odds, ends, and evens**
* [Anykernel3](https://github.com/osm0sis/AnyKernel3.git)
* [Android Image Kitchen](https://github.com/osm0sis/Android-Image-Kitchen.git)
* [Odds and End thread](https://forum.xda-developers.com/t/tools-zips-scripts-osm0sis-odds-and-ends-multiple-devices-platforms.2239421/)

### References, Links, etc.
* [Android Source](https://source.android.com/)
* [AOSP-Mirror Links](https://aosp-mirror.github.io/)
* [XDA](https://www.xda-developers.com/)
* [Samsung Source Code](https://opensource.samsung.com)
* [Magisk](https://github.com/topjohnwu/Magisk.git)
* [OpenGapps](https://github.com/opengapps/opengapps.git)
* [Kernel.org commit tree v3.10.y](https://git.kernel.org/pub/scm/linux/kernel/git/stable/linux.git/log/?h=linux-3.10.y)
* [Google kernel source for v3.10.y](https://kernel.googlesource.com/pub/scm/linux/kernel/git/stable/linux/+/refs/heads/linux-3.10.y)
* [All things Repo](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/README.md)
* [AOSP-Mirror Links](https://aosp-mirror.github.io/)
* [Repo and git references](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/manifest-format.md#XML-File-Format)
* [Github Documentatation](https://docs.github.com)
* [Magisk Documentation](https://topjohnwu.github.io/Magisk)
* [Manpages for xz compression](http://http://manpages.org/xz)
