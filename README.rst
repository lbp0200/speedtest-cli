speedtest-cli
=============

Command line interface for testing internet bandwidth using
speedtest.net

.. image:: https://img.shields.io/pypi/v/speedtest-cli.svg
        :target: https://pypi.python.org/pypi/speedtest-cli/
        :alt: Latest Version
.. image:: https://img.shields.io/travis/sivel/speedtest-cli.svg
        :target: https://pypi.python.org/pypi/speedtest-cli/
        :alt: Travis
.. image:: https://img.shields.io/pypi/l/speedtest-cli.svg
        :target: https://pypi.python.org/pypi/speedtest-cli/
        :alt: License

Versions
--------

speedtest-cli works with Python 2.4-3.10

.. image:: https://img.shields.io/pypi/pyversions/speedtest-cli.svg
        :target: https://pypi.python.org/pypi/speedtest-cli/
        :alt: Versions

Installation
------------

pip / easy\_install
~~~~~~~~~~~~~~~~~~~


Github
~~~~~~

::

    pip install git+https://github.com/lbp0200/speedtest-cli.git

or

::

    git clone https://github.com/lbp0200/speedtest-cli.git
    cd speedtest-cli
    python setup.py install

Just download (Like the way it used to be)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    wget -O speedtest-cli https://raw.githubusercontent.com/lbp0200/speedtest-cli/master/speedtest.py
    chmod +x speedtest-cli

or

::

    curl -Lo speedtest-cli https://raw.githubusercontent.com/lbp0200/speedtest-cli/master/speedtest.py
    chmod +x speedtest-cli

Usage
-----

::

    北京移动
    $ speedtest-cli --server-url http://speedtest.bmcc.com.cn:8080/speedtest/upload.php

    上海联通
    $ speedtest-cli --server-url http://5g.shunicomtest.com:8080/speedtest/upload.php

    天津电信
    $ speedtest-cli --server-url http://tjrate.tjtele.com:8080/speedtest/upload.php

    上海电信
    $ speedtest-cli --server-url http://speedtest1.online.sh.cn:8080/speedtest/upload.php

Python API
----------

See the `wiki <https://github.com/sivel/speedtest-cli/wiki>`_.


Inconsistency
-------------

It is not a goal of this application to be a reliable latency reporting tool.

Latency reported by this tool should not be relied on as a value indicative of ICMP
style latency. It is a relative value used for determining the lowest latency server
for performing the actual speed test against.

There is the potential for this tool to report results inconsistent with Speedtest.net.
There are several concepts to be aware of that factor into the potential inconsistency:

1. Speedtest.net has migrated to using pure socket tests instead of HTTP based tests
2. This application is written in Python
3. Different versions of Python will execute certain parts of the code faster than others
4. CPU and Memory capacity and speed will play a large part in inconsistency between
   Speedtest.net and even other machines on the same network

Issues relating to inconsistencies will be closed as wontfix and without
additional reason or context.
