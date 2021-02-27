# CodInGame Python Multi-file Script phyCharm

Minimally forked from https://github.com/devYaoYH/cg_pyEnv 

Simple script to collect python class definitions across multiple files with `build <file>`.

## Installation

Install it by downloading the package from 
 ``github`` and running ``pip install <folder where cg_py_class_merger is located>``

## Sample Workflow
**project structure:**

    codInGame/

        lib/
             your_packages/
             cg_py_class_merger/
        
        any_project/ # for example 'mars_lander'
     

Before import your own package you have to insert a line # IMPORT
After import your own package you have to insert a line # END_IMPORT

example:

``# IMPORT``

from lib.classes.matrix_ import *

``# END_IMPORT``

In any_project folder (mars_lander for example) simply run ``build xxx.py``, or define a file watcher in your IDE.

Output will be cg.py in your any_project folder

## Issues

1. Generate dependency tree and resolve order of imports automatically
