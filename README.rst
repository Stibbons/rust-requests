*************
Rust Requests
*************

Full featured asynchroneous HTTP library for Rust.


Features
========

- Asynchronous request, using a configurable number of task count
- Easy to use, clear as crystal API syntax
- Reuse same socket connection for multiple requests
- Connection Pooling
- International Domains and URLs
- Keep-Alive
- Session automatically closed on server Fin/Ack
- Sessions with Cookie Persistence
- Basic/Digest Authentication
- Automatic Decompression (Gzip and deflate)
- File posting
- Unicode Response Bodies
- Multipart File Uploads
- Connection Timeouts
- .netrc support and manual proxy support


Wanted
======

- Browser-style SSL Verification


Introduction
============

Rust-Request is being developped with simplisity of usage in mind, following the Python's PEP20 (http://www.python.org/dev/peps/pep-0020/) principles. To be faire, it is heavily inspirated from Python's Requests library (http://www.python-requests.org/en/latest/user/intro/) and txrequests (https://pypi.python.org/pypi/txrequests):

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Readability counts.

License
=======

TBD

Installation
============

TBD


Usage
=====

Requests
--------

.. code-block:: rust

    r = requests.get(~"https://github.com/timeline.json')
    r = requests.post(~"http://httpbin.org/post")
    r = requests.put(~"http://httpbin.org/put")
    r = requests.delete(~"http://httpbin.org/delete")
    r = requests.head(~"http://httpbin.org/get")
    r = requests.options(~"http://httpbin.org/get")

Requests with payload
---------------------

.. code-block:: rust

    payload = {a: 1}
    payload = json()
    r = requests.post(~"http://httpbin.org/post", payload)


Content
-------

.. code-block:: rust

    r.text() for encoding translated version of body content
    r.bynary_content() for binary content
    r.json_content() for json translated content
    r.stream_content(10) for strea raw content

Encoding
--------

.. code-block:: rust

    r.encoding()

Custom Headers
--------------

TBD

Status Codes
------------

.. code-block:: rust

    r.status_code()

Headers
-------

TBD

Request Headers
~~~~~~~~~~~~~~~

.. code-block:: rust

    r.requests().headers()

Response Headers
~~~~~~~~~~~~~~~~

.. code-block:: rust

    r.headers()

Cookies
-------

Requests
~~~~~~~~

.. code-block:: rust

    let req = requests.make_request()
    req.set_cookies()
    req.put(~"https://github.com/timeline.json')

Response
~~~~~~~~

.. code-block:: rust

    r.get_cookies()

Redirections
============

Requests automatically does redirections

r.history to access to track redirections

Timeout
=======

Set the timeout in miliseconds in the requests

.. code-block:: rust

    r.put(~"...", 2000);

timeout is not a time limit on the entire response download; rather, an exception is raised if the server has not
issued a response for timeout seconds (more precisely, if no bytes have been received on the underlying socket for
timeout seconds).


Session
=======

TBD


SSL Verification
================

TBD


Keep Alive
==========

TBD


Streaming
=========


Straeming Uploads
~~~~~~~~~~~~~~~~~

TBD


Streaming Requests
~~~~~~~~~~~~~~~~~~

TBD


Proxies
=======

TBD


Verbs
=====

GET, OPTIONS, HEAD, POST, PUT, PATCH and DELETE

Blocking or Asynchronous
========================

TBD



