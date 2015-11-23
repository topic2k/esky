
Esky  - keep frozen apps fresh
==============================


[![Build Status](https://travis-ci.org/cloudmatrix/esky.svg)](https://travis-ci.org/cloudmatrix/esky)
[![Code Climate](https://codeclimate.com/github/cloudmatrix/esky/badges/gpa.svg)](https://codeclimate.com/github/cloudmatrix/esky)
[![Test Coverage](https://codeclimate.com/github/cloudmatrix/esky/badges/coverage.svg)](https://codeclimate.com/github/cloudmatrix/esky/coverage)

Esky is an auto-update framework for frozen Python applications.  It provides
a simple API through which apps can find, fetch and install updates, and a
bootstrapping mechanism that keeps the app safe in the face of failed or
partial updates. Updates can also be sent as patches.

Esky is currently capable of freezing apps with py2exe, py2app, cxfreeze and
bbfreeze. Adding support for other freezer programs should be easy;
patches will be gratefully accepted.

#### Limitations
 - Cannot sign the bootstrap executable


#### News

 - Python2.6 support may be depreciated (as moving codebase to python3)
 - Bbfreeze will be depreciated

#### Screencast

Ryan has done a talk at pycon to help you get started:

* [Keep your frozen app fresh](http://pyvideo.org/video/470/pyconau-2010--esky--keep-your-frozen-apps-fresh)


Installation
------------

The simplest way to install esky is

`pip install esky`

To install the latest development branch you can install directly from github with

```
git clone git@github.com:cloudmatrix/esky.git
pip install -e esky
```

**To uninstall the development version do** `python setup.py develop --uninstall`


Usage
-----

Freezing your app with esky requires the setup file to be modified,
you are then able to run

`python setup.py bdist_esky`

which will setup the correct directory structure for esky to work

- see the [tutorial](https://github.com/cloudmatrix/esky/tree/master/tutorial) which will guide you through setting up and freezing with esky.

- for more information on the setup file
see [Setup file Options](https://github.com/cloudmatrix/esky/wiki/Setup-file-Options) 

The main interface is the 'Esky' class, which represents a frozen app.   
A simple example of using the esky class to automatically update is given
in the tutorial.

Check [Using the Esky Class](https://github.com/cloudmatrix/esky/wiki/Using-the-Esky-Class) on customizing the process.
Esky is currently capable of hitting a http server and there is a patch
for amazon s3 which should be merged soon.

There is also a wrapper for esky in for the gui library wxpthon, see [blog post](http://www.blog.pythonlibrary.org/2013/07/12/wxpython-updating-your-application-with-esky/) 

Development / Contributing
--------------------------

See the [Contributing Guide] (https://github.com/cloudmatrix/esky/wiki/Contributing)

#### Author

[Ryan Kelly](https://github.com/rfk)

#### Current Core

 - [Timothy Eichler](https://github.com/timeyyy)

#### Contributors

https://github.com/cloudmatrix/esky/graphs/contributors

