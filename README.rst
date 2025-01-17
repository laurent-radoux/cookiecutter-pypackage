======================
cookiecutter-pypackage
======================

.. image:: https://api.travis-ci.org/laurent-radoux/cookiecutter-pypackage.svg?branch=master
   :target: https://travis-ci.org/laurent-radoux/cookiecutter-pypackage


This was forked from: https://github.com/audreyr/cookiecutter-pypackage. Here are the differences of this forked version:

* Required packages are not hardcoded in the ``setup.py`` file. All the required packages are inside the ``requirements`` folder.

* Package requirements are broken down into separate files::

.. code:: bash

    ├── requirements
    │   ├── dev.txt
    │   ├── prod.txt
    │   ├── test.txt

* Creates a default class based on the package name.

Cookiecutter template for a Python package. See https://github.com/audreyr/cookiecutter.

* Free software: BSD license
* Vanilla testing setup with `unittest` and `python setup.py test`
* Travis-CI_: Ready for Travis Continuous Integration testing
* Tox_ testing: Setup to easily test for Python 2.6, 2.7, 3.3, 3.4
* Sphinx_ docs: Documentation ready for generation with, for example, ReadTheDocs_
* Bumpversion: Pre-configured version bumping with a single command


Usage
-----

Generate a Python package project::

    cookiecutter https://github.com/laurent-radoux/cookiecutter-pypackage.git

About the package ``requirements``:

* Install the dev requirements in your local machine by running::
    
    pip install -r requirements/dev.txt

* Requirements for Unit testing (on Travis) can be found in ``requirements/test.txt``

* Requirements for Prod build can be found in ``requirements/prod.txt``

* Prod requirements are reused in both Dev and Test requirements.

Then:

* Create a repo and put it there.
* Add the repo to your Travis CI account.
* Run the script `travis_pypi_setup.py` to encrypt your PyPI password in Travis config
  and activate automated deployment on PyPI when you push a new tag to master branch.
* Add the repo to your ReadTheDocs account + turn on the ReadTheDocs service hook.
* Release your package the standard Python way. Here's a release checklist: 
  https://gist.github.com/audreyr/5990987
* (Optional) If you feel like pinning the requirements for your package, you can
  add a `requirements.txt` that specifies packages and version numbers.

Not Exactly What You Want?
--------------------------

Don't worry, you have options:

Similar Cookiecutter Templates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* `Nekroze/cookiecutter-pypackage`_: A fork of this with a PyTest test runner,
  strict flake8 checking with Travis/Tox, and some docs and `setup.py` differences.
  
* `tony/cookiecutter-pypackage-pythonic`_: Fork with py2.7+3.3 optimizations. 
  Flask/Werkzeug-style test runner, ``_compat`` module and module/doc conventions.
  See ``README.rst`` or the `github comparison view`_ for exhaustive list of 
  additions and modifications.

* `laurent-radoux/cookiecutter-pypackage`_: A fork of this with updated Pytest, flake8,
  requirement management and default github workflows.

* Also see the `network`_ and `family tree`_ for this repo. (If you find
  anything that should be listed here, please add it and send a pull request!)

Fork This / Create Your Own
~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have differences in your preferred setup, I encourage you to fork this
to create your own version. Or create your own; it doesn't strictly have to
be a fork.

* Once you have your own version working, add it to the Similar Cookiecutter
  Templates list above with a brief description. 

* It's up to you whether or not to rename your fork/own version. Do whatever
  you think sounds good.

Or Submit a Pull Request
~~~~~~~~~~~~~~~~~~~~~~~~

I also accept pull requests on this, if they're small, atomic, and if they
make my own packaging experience better.


.. _Travis-CI: http://travis-ci.org/
.. _Tox: http://testrun.org/tox/
.. _Sphinx: http://sphinx-doc.org/
.. _ReadTheDocs: https://readthedocs.org/
.. _`Nekroze/cookiecutter-pypackage`: https://github.com/Nekroze/cookiecutter-pypackage
.. _`tony/cookiecutter-pypackage-pythonic`: https://github.com/tony/cookiecutter-pypackage-pythonic
.. _github comparison view: https://github.com/tony/cookiecutter-pypackage-pythonic/compare/audreyr:master...master
.. _`network`: https://github.com/audreyr/cookiecutter-pypackage/network
.. _`family tree`: https://github.com/audreyr/cookiecutter-pypackage/network/members
