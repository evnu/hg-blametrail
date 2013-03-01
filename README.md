Mercurial Blame Trail
=====================

An interactive mode for hg blame that helps you trace when a particular line was introduced - not just when it was last edited.

Essentially it automates this process:

    hg blame -n some/file.py
    <manually inspect file to find changeset line was last modified in>
    hg up <changeset>
    hg blame -n some/file.py
    <manually inspect file to find changeset line was last modified in>
    hg up <changeset>
    hg blame -n some/file.py
    <manually inspect file to find changeset line was last modified in>
    hg up <changeset>
    ...

Usage
-----

    $ hg blame --trail 116 some/file.py --context=2

Install
-------

Add the following to your `.hgrc`:

    [extensions]
    blametrail = /path/to/hg-blametrail/blametrail.py
