IDKFA
=====
The all items cheat code for Docker based developer environments.

Purpose
-------
Define and maintain your project's development environment inside a Docker
and seemlessly run contained commands against your working directory.


If you frequently find yourself doing the following

.. code:: bash
    kaak@pc:/my/project/root$ docker --rm -it -v $(pwd):/develop -w /develop node:6.9.1 gulp build



Simply define `/my/project/root/.idkfa`

.. code:: javascript

{
  "image": "node:6.9.1"
}


You can now simply run

.. code:: bash
    kaak@pc:/my/project/root$ idkfa gulp build

from anywhere in your project and everything will be taken care of for you.

Todo
----
Lots. This is barely a proof-of-concept.

* Better stdout/err streaming
* Handle stdin
* Port mapping
* Environment variables
* External volumes
* Linking and composing
