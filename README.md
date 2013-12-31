Server Tools
============

This software package was developed by David Coss at St Jude Children's Research Hospital to provide user-level validation and assimilation routines. It is released for use under the GNU General Public License (see COPYING or http://www.gnu.org/licenses/gpl.html for details).

Setup
-----

* Server Tools contains two parts, C code and Python code. These are installed separately. In the top most directory, simply run configure and make to build the C code. In the python/ subdirectory, run "python setup.py install" to install the python code.
* python/boinctools/__init__.py has a field, called project_path, that needs to be the full path to the BOINC project.
* Also, src/pyboinc.cpp contains the same project path. This needs to be updated as well. Search for init_filename
* Python code can move invalid results into a subdirectory of the project, called invalid_results. It is used if a user validation/assimilation code fails, to prevent data from being lost due to user error.


Requires
--------

This code embeds Python in the BOINC validation and assimilation programs, which are written in C. To do this, the development package of Python is required. This may be obtained from your OS distribution repositories, i.e. yum or apt-get, or from the Python website, http://www.python.org. Currently, this code has only been used with Python 2.7.

Documentation
-------------

A script, docs/generate_docs.sh, may be used to generate API documentation. Python API documentation requires Epydoc. This may be downloaded at http://epydoc.sourceforge.net. C API documentation is generated with doxygen. This may be downloaded at www.doxygen.org.

License
-------

Available for use under the GNU General Public License version 3.