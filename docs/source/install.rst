.. module:: PycURL2


Installation
------------

You can install the most recent PycURL2 version using `easy_install`_ or `pip`_::

    easy_install pycurl2
    pip install pycurl2

.. _easy_install: http://peak.telecommunity.com/DevCenter/EasyInstall
.. _pip: http://pypi.python.org/pypi/pip


**NOTE**: You need Python and libcurl installed on your system to use or
build pycurl.  Some RPM distributions of curl/libcurl do not include
everything necessary to build pycurl, in which case you need to
install the developer specific RPM which is usually called curl-dev.


Distutils
~~~~~~~~~

Build and install pycurl with the following commands::

    (if necessary, become root)
    tar -zxvf pycurl-$VER.tar.gz
    cd pycurl2-$VER
    python setup.py install

``$VER`` should be substituted with the pycurl version number, e.g. 7.10.5.

Note that the installation script assumes that `curl-config` can be
located in your path setting.  If curl-config is installed outside
your path or you want to force installation to use a particular
version of `curl-config`, use the `--curl-config` commandline option to
specify the location of curl-config.  Example::

    python setup.py install --curl-config=/usr/local/bin/curl-config

If libcurl is linked dynamically with pycurl, you may have to alter the
`LD_LIBRARY_PATH` environment variable accordingly.  This normally
applies only if there is more than one version of libcurl installed,
e.g. one in `/usr/lib` and one in `/usr/local/lib`.


Windows
~~~~~~~

When installing on Windows, you need to manually configure the path to
the curl source tree, specified with the `CURL_DIR` variable in the file
'setup.py'.  The `CURL_DIR` variable can also be set using the
commandline option `--curl-dir` when invoking setup.py::

    python setup.py install --curl-dir=c:\curl-7.10.5
