## Best to run <sudo apt update> before any install]
====================================================  
  
  
  sudo apt update && sudo apt upgrade

  
  

**Usage: apt command [options]**
       **apt help command [options]**
```
Commands:
  add-repository   - Add entries to apt sources.list
  autoclean        - Erase old downloaded archive files
  autoremove       - Remove automatically all unused packages
  build            - Build binary or source packages from sources
  build-dep        - Configure build-dependencies for source packages
  changelog        - View a package's changelog
  check            - Verify that there are no broken dependencies
  clean            - Erase downloaded archive files
  contains         - List packages containing a file
  content          - List files contained in a package
  deb              - Install a .deb package
  depends          - Show raw dependency information for a package
  dist-upgrade     - Upgrade the system by removing/installing/upgrading packages
  download         - Download the .deb file for a package
  edit-sources     - Edit /etc/apt/sources.list with your preferred text editor
  dselect-upgrade  - Follow dselect selections
  full-upgrade     - Same as 'dist-upgrade'
  held             - List all held packages
  help             - Show help for a command
  hold             - Hold a package
  install          - Install/upgrade packages
  list             - List packages based on package names
  policy           - Show policy settings
  purge            - Remove packages and their configuration files
  recommends       - List missing recommended packages for a particular package
  rdepends         - Show reverse dependency information for a package
  reinstall        - Download and (possibly) reinstall a currently installed package
  remove           - Remove packages
  search           - Search for a package by name and/or expression
  show             - Display detailed information about a package
  showhold         - Same as 'held'
  showsrc          - Display all the source package records that match the given package name
  source           - Download source archives
  sources          - Same as 'edit-sources'
  unhold           - Unhold a package
  update           - Download lists of new/upgradable packages
  upgrade          - Perform a safe upgrade
  version          - Show the installed version of a package
```

----------------------------------------------------------------------------------
#######################################
#                                     #
# sudo apt search --help              #
# aptitude 0.8.12                     #
# Usage: aptitude [-S fname] [-u|-i]  #
#  aptitude [options] <action> ...    #
#                                     #
#######################################

Actions (if none is specified, aptitude will enter interactive mode):
 
```
 install         Install/upgrade packages.
 remove          Remove packages.
 purge           Remove packages and their configuration files.
 hold            Place packages on hold.
 unhold          Cancel a hold command for a package.
 markauto        Mark packages as having been automatically installed.
 unmarkauto      Mark packages as having been manually installed.
 forbid-version  Forbid aptitude from upgrading to a specific package version.
 update          Download lists of new/upgradable packages.
 safe-upgrade    Perform a safe upgrade.
 full-upgrade    Perform an upgrade, possibly installing and removing packages.
 build-dep       Install the build-dependencies of packages.
 forget-new      Forget what packages are "new".
 search          Search for a package by name and/or expression.
 show            Display detailed info about a package.
 showsrc         Display detailed info about a source package (apt wrapper).
 versions        Displays the versions of specified packages.
 clean           Erase downloaded package files.
 autoclean       Erase old downloaded package files.
 changelog       View a package's changelog.
 download        Download the .deb file for a package (apt wrapper).
 source          Download source package (apt wrapper).
 reinstall       Reinstall a currently installed package.
 why             Explain why a particular package should be installed.
 why-not         Explain why a particular package cannot be installed.

 add-user-tag    Add user tag to packages/patterns.
 remove-user-tag Remove user tag from packages/patterns.

Options:
 -h              This help text.
 --no-gui        Do not use the GTK GUI even if available.
 -s              Simulate actions, but do not actually perform them.
 -d              Only download packages, do not install or remove anything.
 -P              Always prompt for confirmation of actions.
 -y              Assume that the answer to simple yes/no questions is 'yes'.
 -F format       Specify a format for displaying search results; see the manual.
 -O order        Specify how search results should be sorted; see the manual.
 -w width        Specify the display width for formatting search results.
 -f              Aggressively try to fix broken packages.
 -V              Show which versions of packages are to be installed.
 -D              Show the dependencies of automatically changed packages.
 -Z              Show the change in installed size of each package.
 -v              Display extra information. (may be supplied multiple times).
 -t [release]    Set the release from which packages should be installed.
 -q              In command-line mode, suppress the incremental progress
                  indicators.
 -o key=val      Directly set the configuration option named 'key'.
 --with(out)-recommends     Specify whether or not to treat recommends as
                            strong dependencies.
 -S fname        Read the aptitude extended status info from fname.
 -u              Download new package lists on startup.
                  (terminal interface only)
 -i              Perform an install run on startup.
                  (terminal interface only)
```
See the manual page for a complete list and description of all the options.

This aptitude does not have Super Cow Powers.
