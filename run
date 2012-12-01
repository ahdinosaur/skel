#!/usr/bin/env python

from glob import glob
import os
import subprocess

# install dotfiles
os.chdir("dotfiles/")
subprocess.call("gem install bundler")
subprocess.call("bundle")
subprocess.call("bundle exec rake install")
os.chdir("../")

# install modules
os.chdir("modules/")
for module in glob("modules/*"):
    subprocess.call("modules/%s" % module)
