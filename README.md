# codInGame Python Multi-file Script

Minimally forked from https://github.com/devYaoYH/cg_pyEnv 

Simple script to collect python class definitions across multiple files with `build <file>`.

## Installation

Install it by downloading the package from 
 ``github`` and running ``pip install <folder where cg_py_class_merger is located>``

## Sample Workflow
**project structure:**

    codingame/

        lib/
             your_packages/
               your_package
             cg_py_class_merger/
        
        any_project/ # for example 'mars_lander'
     

Before import your own package you have to insert a line

``# IMPORT``

After import your own package you have to insert a line

``# END_IMPORT``

example:

``# IMPORT``

from lib.``your_packages.your_package`` import *

``# END_IMPORT``

Do not forget to init your packages with ``__init__.py``

In any_project folder (mars_lander for example) simply run ``build mars_lander.py``, or define a file watcher in your IDE.

Output will be ``cg.py`` in your ``any_project`` folder

## Issues

1. Generate dependency tree and resolve order of imports automatically
