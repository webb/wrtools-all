# WR Tools: All
=====

This repo packages up a set of tools, including:

- https://github.com/webb/doc-processing
- https://github.com/webb/saxon-cli.git
- https://github.com/webb/schematron-cli.git
- https://github.com/webb/wrtools-core.git
- https://github.com/webb/wrtools-git.git
- https://github.com/webb/xalan-cli.git
- https://github.com/webb/xml-schema-validator.git

Tools may require other tools to build and install, so they build in order, and the PATH for building each stage includes the build target directory. 

# Install

Use Jabba to install & select Java JVM: <https://github.com/shyiko/jabba#installation>

`$ jabba install zulu@1.11.0`

`$ jabba use zulu@1.11.0`

Grab all the packages, which are submodules to this git repo:

`$ git submodule init`

`$ git submodule update`

Pick a root directory (I use `$HOME`) & configure:

`$ ./configure --prefix=${root directory}`

For example: `$ ./configure --prefix=/User/home/foo`

Build the packages:

`$ make`
    
Install into the directory you gave with `--prefix` above. There are 2 ways to do this: a direct install, and installing with `stow`. I vastly prefer `stow`.

Installing with stow

1. Make sure you have stow: `$ type -p stow` should not have an error. If you don't have stow, install it with your package manager.

2. Run `make -f stow.mk install`, which will install the package in a directory `${prefix}/stow/wrtools-all`, and will link to there from `${prefix}/bin`, etc.

3. Later, you can use `stow` to uninstall, or you can uninstall with `$ make -f stow.mk uninstall`

Installing directly:

1. `$ make install`

2. Later, you can uninstall with `$ make uninstall`

# Packages required

Things you'll need from your package manager include:

- make
- gradle
- zip
- m4
- stow

# License

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
details.

You should have received a copy of the GNU General Public License along with
this program.  If not, see <http://www.gnu.org/licenses/>.

