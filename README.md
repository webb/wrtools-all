# WR Tools: All
=====

This repo packages up a set of tools, including:

- WR Tools: Core: <https://github.com/webb/wrtools-core>
- WR Tools: Git: <https://github.com/webb/wrtools-git>

Tools may require other tools to build and install, so they build in order, and the PATH for building each stage includes the build target directory. 

# Usage

```
$ ./configure --prefix=${install directory}
$ make
$ make install
```

Assume things will break if you try to `make install` before you've done `make`. We don't know what all the files will be until everything is built.

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

# Build a zip with everything in it

```
$ PATH=/usr/bin:/bin ./configure --prefix=$PWD/build/out && make zip
```

# Install a zip

{example using stow}

# Submodules to add

- apache-tika.git
- code-list-tools.git
- doc-processing
- gen-xsd-diagrams.git
- jing-cli
- mac-copy-to-inbox
- niem-ndr-tools.git
- niem-schema-assembly
- pandoc-2.3
- saxon-cli
- schematron-cli.git
- simple-xsd
- wrtools-core
- wrtools-git
- wrtools-gui.git
- wrtools-json
- wrtools-user
- xalan-cli
- xml-schema-validator-0.1
- xml-tools
- xsd-rename.git



