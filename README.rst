======================
cookiecutter-pypackage
======================

.. image:: https://img.shields.io/travis/ssearcy/cookiecutter-pypackage.svg
   :target: https://travis-ci.org/ssearcy/cookiecutter-pypackage

Cookiecutter_ template for a Python package.

* GitHub repo: https://github.com/ssearcy/cookiecutter-pypackage/
* Free software: BSD license

Features
--------

Forked from https://github.com/audreyr/cookiecutter-pypackage.git
with some changes to directory structure and test apparatus.

* Boilerplate `setup.py` based on
  https://hynek.me/articles/sharing-your-labor-of-love-pypi-quick-and-dirty/
* Testing setup with pytest_ and `python setup.py test`
* Travis-CI_: Ready for Travis Continuous Integration testing
* Tox_ testing: Setup to easily test for Python 2.7, 3.4, 3.5 and incorporates
  some other features from https://hynek.me/articles/testing-packaging/
* Sphinx_ docs: Documentation ready for generation with, for example, ReadTheDocs_
* Auto-release to PyPI when you push a new tag to master (optional)

.. _Cookiecutter: https://github.com/audreyr/cookiecutter

Quickstart
----------

Generate a Python package project::

    cookiecutter https://github.com/ssearcy/cookiecutter-pypackage.git

Then:

* Create a repo and put it there.
* Add the repo to your Travis CI account.
* Install the dev requirements into a virtualenv. (`pip install -r requirements_dev.txt`)
* Run the script `travis_pypi_setup.py` to encrypt your PyPI password in Travis config
  and activate automated deployment on PyPI when you push a new tag to master branch.
* Add the repo to your ReadTheDocs account + turn on the ReadTheDocs service hook.
* Release your package by pushing a new tag to master.
* (Optional) If you feel like pinning the requirements for your package, you can
  add a `requirements.txt` that specifies packages and version numbers.

For more details, see the `cookiecutter-pypackage tutorial`_.

.. _`cookiecutter-pypackage tutorial`: http://cookiecutter-pypackage.readthedocs.org/en/latest/tutorial.html

TODO
----

* Add option for namespace packages
* Incorporate some of the additional naming options in
  https://github.com/ionelmc/cookiecutter-pylibrary


.. _pytest: http://pytest.org/latest/
.. _Travis-CI: http://travis-ci.org/
.. _Tox: http://testrun.org/tox/
.. _Sphinx: http://sphinx-doc.org/
.. _ReadTheDocs: https://readthedocs.org/
