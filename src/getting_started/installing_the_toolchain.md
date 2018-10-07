Installing the toolchain
========================

The redox toolchain is required in order to compile certain parts of redox. This basically entails installing a patched version of gcc.

### Ubuntu and other Debian based systems

To install the toolchain, run the following commands:
```bash
# Get the Redox OS APT key
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys AA12E97F0881517F

# Install the APT repository
sudo add-apt-repository 'deb https://static.redox-os.org/toolchain/apt /'

# Update your package lists
sudo apt update

# Install the cross compiler
sudo apt install x86-64-unknown-redox-gcc
```

### Arch Linux
To install the toolchain, run the following commands:
 ```bash
 # Clone libc
 git clone --recursive https://gitlab.redox-os.org/redox-os/libc.git
 
 # Go to the packages
 cd libc/packages/arch
 
 # Start with binutils
 cd binutils
 makepkg -si
 
 # Then autoconf
 cd ../autoconf
 makepkg -si
 
 # Then gcc-freestanding
 cd ../gcc-freestanding
 makepkg -si
 
 # Then newlib
 cd ../newlib
 makepkg -si
 
 # Finally gcc
 cd ../gcc
 makepkg -si
 ```

### Other distros/Mac OS X
To install the toolchain, run the following commands:
 ```bash
 # Clone libc
 git clone --recursive git@gitlab.redox-os.org:redox-os/libc
 
 # Run the setup script
 cd libc
 ./setup.sh all
 
 # Add the tools to your path
 export PATH=$PATH:/path/to/libc/build/prefix/bin
 ```
Next steps
----------

Now that we have the build tools and the toolchain, we can [prepare our build](getting_started/preparing_the_build.html).
