ITKFDFImageIO
=============

.. |CircleCI| image:: https://circleci.com/gh/InsightSoftwareConsortium/ITKFDFImageIO.svg?style=shield
    :target: https://circleci.com/gh/InsightSoftwareConsortium/ITKFDFImageIO

.. |TravisCI| image:: https://travis-ci.org/InsightSoftwareConsortium/ITKFDFImageIO.svg?branch=master
    :target: https://travis-ci.org/InsightSoftwareConsortium/ITKFDFImageIO

.. |AppVeyor| image:: https://img.shields.io/appveyor/ci/itkrobot/itkfdfimageio.svg
    :target: https://ci.appveyor.com/project/itkrobot/itkfdfimageio

=========== =========== ===========
   Linux      macOS       Windows
=========== =========== ===========
|CircleCI|  |TravisCI|  |AppVeyor|
=========== =========== ===========


Overview
--------

This is a module for the `Insight Toolkit (ITK) <http://itk.org>`_ to read or
write the FDF image format.

It contains an `ImageIO` class to read or write the FDF image format.

This module is available in the ITK source tree as a Remote module. To enable
it, set::

  Module_IOFDF:BOOL=ON

in ITK's CMake build configuration.


License
-------

This software is distributed under the Apache 2.0 license. Please see
the *LICENSE* file for details.


Acknowledgements
----------------

Initial work was done by `Glenn Pierce <mailto:glennpierce@gmail.com>`_\; the
code was brought up to current ITK standards by
`Nicholas Tustison <mailto:ntustison@gmail.com>`_\; and it was converted to an
ITK Remote module by `Kent Williams <mailto:norman-k-williams@uiowa.edu>`_.
