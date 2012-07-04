==============
smartresponder
==============

This is a smartresponder (aka smartresponder.ru)
python API wrapper. The goal is to support all API methods (current and future)
that can be accessed from server.

Installation
============

::

    $ pip install smartresponder

Usage
=====

::

    >>> import smartresponder
    >>> api = smartresponder.API('my_api_id', 'my_api_secret')
    >>> print api.subscribers.create(email='tester@test.ru', first_name=u'Valentin Gorbunov', delivery_id='177879')
    {u'result': 1, u'id': 39727504}

    >>> subscriber = api.subscribers.list(id='39727504')['list']['elements'][0]
    >>> print subscriber['email']
    tester@test.ru

All API methods that can be called from server should be supported.

See http://goo.gl/DrmQU for detailed API help.