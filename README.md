## System Requirements
General note: prefer to do python related stuff in a `virtualenv`.

### mbed-cli tool
* `pip install mbed-cli`

### arm-gcc-embedded
* Grab it from [here](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)

### openocd
`openocd` in the Debian Buster repository is old, so you'll have to build it yourself. Oh boy.

#### Building/installing from source
* `git clone git://git.code.sf.net/p/openocd/code`
* `cd code`
* `bootstrap` (install missing dependencies if needed)
* `./configure --enable-stlink`
* `sudo make install`

## Compiling
* `mbed export -i make_gcc_arm`
* `make -j4`