tfvm
========

CLI for managing terraform-cli versions.

Usage
-----

To use *version* of terraform:

    $ tfsv use {version}

To list local versions and check current

    $ tfsv list

To install selected *version*:

    $ tfsv install {version}
    
To list remote versions: #Not implemented yet

    $ tfsv list --candidate

Installation and Configuration
-------------
Before Installation and Configuration please remove any terraform you has installed in directories from your ```$PATH``` variable.

First choose wisely, your terraform bin path must be in your ```PATH``` env variable.
As it's user specific solution I strongly suggest creating ```~/bin``` directory where you will store user binaries.
You could add ~/bin to your PATH by setting up line in ```.bashrc```. It start work after reloading session.

    export PATH=$HOME/bin:$PATH

Second you need to download ```tfsv```, put it there and setup permissions.

    $ wget hhttps://github.com/piotr-jarosz/tfvm/releases/download/0.0.3-bash/tfsv
    $ mv tfsv ~/bin/
    $ chmod 700 ~/bin/tfsv

And finally run command:

    $ tfsv setup {version} {terraform PATH} {installation path}
    $ tfsv setup 0.11.14 ~/bin ~/.tfvm/bin

