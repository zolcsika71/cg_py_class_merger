# CG Python Multi-file Script

Minimally forked from https://github.com/devYaoYH/cg_pyEnv 

Simple script to collect python class definitions across multiple files with `build <file>`.

## Installation:

Install it by downloading the package from 
 ``github`` and running ``pip install <folder where cg_py_class_merger is located>``

## Sample Workflow:
**Project structure:**

    codingame/

        lib/
            __init__.py
            your_package_folder_1/
               __init__.py
               package_1.py
     
            your_package_folder_2/
               __init__.py
               package_2.py

            cg_py_class_merger/
               cg_py_class_merger/
                  __init__.py
                  build.py
               README.md
               setup.py

        
        any_project/ # for example 'ClashOfCodes'

Before import your own package you have to insert a line:

``# IMPORT``

After import your own package you have to insert a line:

``# END_IMPORT``

example:

``# IMPORT``

from lib.your_package_folder_1.package_1.py import *

``# END_IMPORT``

Do not forget to init your packages with ``__init__.py``

In ``any_project`` folder (ClashOfCodes for example) simply run ``build <filename>.py``, or define a file watcher in your IDE.

Example: https://github.com/zolcsika71/CodeInGames_PY

Output will be ``cg.py`` in your ``any_project`` folder

## Issues

1. Generate dependency tree and resolve order of imports automatically
