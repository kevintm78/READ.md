* [Source & Reference Links](../docs/references.md)

* Build Tools

      sudo apt install git-core ccache automake lzop bison gperf build-essential zip curl zlib1g-dev g++-multilib python3-networkx libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev liblz4-tool make optipng gnupg flex libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig libncurses5 libtinfo5 android-sdk-platform-tools-common

* Configure Git


      git config --global user.name kevintm78

      git config --global user.email kevintm78@gmail.com

* Install Repo

      export REPO=$(mktemp /tmp/repo.XXXXXXXXX)

      curl -o ${REPO} https://storage.googleapis.com/git-repo-downloads/repo

      gpg --recv-key 8BB9AD793E8E6153AF0F9A4416530D5E920F5C65

      mkdir ~/.bin

      curl -s https://storage.googleapis.com/git-repo-downloads/repo.asc | gpg --verify - ${REPO} && install -m 755 ${REPO} ~/.bin/repo

* [AOSP guide](https://source.android.com/setup/build/initializing) for setting up your build environment.

      sudo apt install git-core ccache automake lzop bison gperf build-essential zip curl zlib1g-dev g++-multilib libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev liblz4-tool make optipng gnupg flex lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig libncurses5 libtinfo5
      
* [Install Repo](../docs/build_setup/installing-repo.md)
________________________________________________________________________________________________________________________________________________________

#### Environment Variables:
  *Warning-These could be as inaccurate as everything else in this readme.*

    export USE_CCACHE=1                                     #Android 9 and below just needs this one
    export ANDROID_SDK_ROOT="$HOME/Android/Sdk"             #Path to some dumb kevin. For when I get lost.
    export OUT_DIR_COMMON_BASE="$HOME/path/to/salvation"    #Set this for common out directory for Android builds
    export PATH="$HOME/android-studio/jre/bin:$PATH"        #This is needs to set for building Magisk
    export PATH="$HOME/.bin:$PATH"                          #This is where I install repo.
    export ALLOW_FILE_DISCOVERY=1                           #Self explanatory
    export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx4g"  #this is for my lack of ram

    export CCACHE_EXEC=$(command -v ccache)                 #Android 10+ only??!!
