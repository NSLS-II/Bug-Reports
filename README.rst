Bug Reports
===========

Unified issue-tracker for bugs in the data acqusition, management, and analysis
software at NSLS-II

Bug Report Checklist
--------------------
Please make sure that you have the following information in your bug report!

- verbose description of the bug that you found (:ref:`bug_reports`)
- watermark of the NSLS-II software stack (:ref:`watermark`)
- output of ``conda list`` from your activated conda environment (:ref:`conda_list`)

.. _bug_reports:

How to write a good bug report
------------------------------

Reporting bugs is critical to software development (we can't fix bugs we are
not aware of).  While reporting bugs is both necessary and helpful, it is
critical to ensure that the reports are *good* bug reports.  For bug reports
to be helpful to your friendly software developers, they need to be

- **Short.** Most bugs can be produced in a few lines of code.  Keeping the code
  short helps to convince the developers the bug is in *their* code not *your* code
- **Self contained.** Include everything needed to replicate the bug
- **Correct.** We should be able to copy/paste/run the code to reproduce the bug.
  If you are unsure how to reproduce the bug, providing a comprehensive
  description of *what* you did to (or what you were doing when) you encountered
  the bug is a reasonable substitute.

There are expanded at http://sscce.org/.

.. _watermark:

NSLS-II Software Watermark
--------------------------

It is important to let us know what versions of python libraries you are
using.  To obtain this information, you can run ``dataportal.watermark()`` from
the python shell which will print out our versions of the python stack ::

    In [7]: from dataportal.utils.diagnostics import watermark

    In [8]: dict(watermark())
    Out[8]:
    {u'bubblegum': u"FAILED TO DETECT: API 'QString' has already been set to version 1",
     u'channelarchiver': '0.0.3',
     u'enaml': u'0.9.8',
     u'filestore': 'v0.0.3.post0',
     u'matplotlib': '1.4.3',
     u'metadatastore': 'v0.0.4.post0',
     u'numpy': '1.9.2',
     u'pandas': '0.16.0',
     u'pims': '0.2.2',
     u'python': u'2.7.9',
     u'pyyaml': '0.2.2',
     u'scipy': '0.15.1',
     u'six': '1.9.0'}

.. _conda_list:

The `conda list command
-----------------------
Additional information that will help us track down your bug can be obtained by
running ``conda list`` which will print the following out to the console.
(Note that this command needs to be run from within your activated conda
environment)::

    (nikea2)edill@edill-810g:~/dev/python/dataportal (master *$ u+1)$ conda list
    # packages in environment at /home/edill/anaconda/envs/nikea2:
    #
    asv                       0.1                       <pip>
    atom (/home/edill/dev/python/atom) 0.3.10                    <pip>
    atom                      0.3.9                    py27_0
    auto-enaml                0.1.0                     <pip>
    backports.ssl-match-hostname 3.4.0.2                   <pip>
    bokeh                     0.8.2                np19py27_0
    cairo                     1.12.18                       0
    channelarchiver (/home/edill/dev/python/channelarchiver) 0.0.4                     <pip>
    colorama                  0.3.3                    py27_0
    controlsui                0.0.0                     <pip>
    coverage                  3.7.1                     <pip>
    coveralls                 0.5                       <pip>
    cython                    0.22                     py27_0
    dataportal                0.0.5.post0               <pip>
    dateutil                  2.4.1                    py27_0
    decorator                 3.4.0                    py27_0
    distribute                0.7.3                     <pip>
    docopt                    0.6.2                     <pip>
    docutils                  0.12                     py27_0
    enaml                     0.9.8                    py27_0
    enum34                    1.0.4                    py27_0
    filestore                 0.1.0.dev0                <pip>
    flask                     0.10.1                   py27_1
    freetype                  2.4.10                        0
    funcsigs                  0.4                      py27_0
    gevent                    1.0.1                    py27_0
    gevent-websocket          0.9.3                    py27_0
    greenlet                  0.4.5                    py27_0
    h5py                      2.4.0                np19py27_0
    hdf5                      1.8.14                        0
    hexrd-0.3.0.dev-205-gd1d356e dirty                     <pip>
    ipython                   3.0.0                    py27_0
    ipython-notebook          3.0.0                    py27_1
    itsdangerous              0.24                     py27_0
    jinja2                    2.7.3                    py27_1
    jpeg                      8d                            0
    jsonschema                2.4.0                    py27_0
    kiwisolver                0.1.3                    py27_0
    lcms                      1.19                          0
    libpng                    1.5.13                        1
    libsodium                 0.4.5                         0
    libtiff                   4.0.2                         1
    llvm                      3.3                           0
    llvmlite                  0.2.2                    py27_1
    llvmpy                    0.12.3                   py27_0
    lmfit                     0.8.3                     <pip>
    markupsafe                0.23                     py27_0
    matplotlib                1.4.3                np19py27_0
    metadatastore             0.1.0.dev0                <pip>
    mistune                   0.5                      py27_0
    mongoengine               0.8.7                     <pip>
    networkx                  1.9.1                    py27_0
    nose                      1.3.4                    py27_1
    numba                     0.12.2               np18py27_0
    numpy                     1.9.2                    py27_0
    openssl                   1.0.1k                        1
    pandas                    0.16.0               np19py27_1
    pil                       1.1.7                    py27_1
    pillow                    2.7.0                    py27_0
    pims                      0.2.2                    py27_0
    pip                       6.0.8                    py27_0
    pixman                    0.26.2                        0
    ply                       3.4                      py27_0
    pockets                   0.2.3                     <pip>
    ptyprocess                0.4                      py27_0
    py2cairo                  1.10.0                   py27_2
    pygments                  2.0.2                    py27_0
    pymongo                   2.8                       <pip>
    pyparsing                 2.0.3                    py27_0
    pyqt                      4.10.4                   py27_0
    python                    2.7.9                         2
    python-dateutil           2.4.1                    py27_0
    pytz                      2015.2                   py27_0
    pyxrf                     0.0.0.dev0                <pip>
    pyyaml                    3.11                     py27_0
    pyzmq                     14.5.0                   py27_0
    qt                        4.8.5                         0
    readline                  6.2                           2
    requests                  2.6.0                    py27_0
    scikit-image              0.10.1               np18py27_0
    scikit-xray               0.0.3.post0               <pip>
    scipy                     0.15.1               np19py27_0
    setuptools                14.3.1                   py27_0
    sip                       4.15.5                   py27_0
    six                       1.9.0                    py27_0
    sphinx                    1.2.3                    py27_0
    sphinx-bootstrap-theme    0.4.5                     <pip>
    sphinxcontrib-napoleon    0.3.1                     <pip>
    sqlite                    3.8.4.1                       1
    ssl_match_hostname        3.4.0.2                  py27_0
    system                    5.8                           2
    terminado                 0.5                      py27_0
    tifffile                  0.3.1                np18py27_0
    tk                        8.5.18                        0
    tornado                   4.1                      py27_0
    trackpy                   0.2.4                    py27_0
    tzlocal                   1.1.2                     <pip>
    ujson                     1.33                     py27_0
    werkzeug                  0.10.1                   py27_0
    xraylib                   master               np19py27_0
    yaml                      0.1.4                         0
    zeromq                    4.0.4                         0
    zlib                      1.2.8                         0



