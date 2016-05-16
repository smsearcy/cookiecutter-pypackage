======================
cookiecutter-pypackage
======================

.. image:: https://img.shields.io/travis/ssearcy/cookiecutter-pypackage.svg
   :target: https://travis-ci.org/ssearcy/cookiecutter-pypackage

Cookiecutter_ template for a Python package.

* GitHub repo: https://github.com/smsearcy/cookiecutter-pypackage/
* Free software: BSD license

Features
--------

Forked from https://github.com/audreyr/cookiecutter-pypackage.git
with some changes to directory structure and test apparatus.

* Boilerplate ``setup.py`` based on
  https://hynek.me/articles/sharing-your-labor-of-love-pypi-quick-and-dirty/
* Testing setup with pytest_
* Travis-CI_: Ready for Travis Continuous Integration testing
* Tox_ testing: Setup to easily test for Python 2.7, 3.4, 3.5 and incorporates
  additional features from https://hynek.me/articles/testing-packaging/
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
* Install the dev requirements into a virtualenv. (``pip install -r requirements_dev.txt``)
* Run the script ``travis_pypi_setup.py`` to encrypt your PyPI password in Travis config
  and activate automated deployment on PyPI when you push a new tag to master branch.
* Add the repo to your ReadTheDocs account + turn on the ReadTheDocs service hook.
* Release your package by pushing a new tag to master.
* (Optional) If you feel like pinning the requirements for your package, you can
  add a ``requirements.txt`` that specifies packages and version numbers.

For more details, see the `cookiecutter-pypackage tutorial`_ (these are for the original
``cookiecutter-pypackage`` but should get you going in the right direction.

.. _`cookiecutter-pypackage tutorial`: http://cookiecutter-pypackage.readthedocs.org/en/latest/tutorial.html


Prompts
-------

An explanation of the information you will be prompted for when generating the Python package.

Templated Values
^^^^^^^^^^^^^^^^

The following appear in various parts of your generated project.

full_name
    Your full name.

email
    Your email address.

github_username
    Your GitHub username.

project_name
    The name of your new Python package project. This is used in documentation, so spaces and any characters are fine here.

project_slug
    The namespace of your Python package. This should be Python import-friendly. Typically, it is the slugified version of project_name.

project_short_description
    A 1-sentence description of what your Python package does.

project_uri
    URI for the project.

release_date
    The date of the first release.

pypi_username
    Your Python Package Index account username.

year
    The year of the initial package copyright in the license file.

version
    The starting version number of the package.

Options
^^^^^^^

The following package configuration options set up different features for your project.

use_pypi_deployment_with_travis
    Whether to use PyPI deployment with Travis.


TODO
----

* Add option for namespace packages
* Incorporate some of the additional naming prompts in
  https://github.com/ionelmc/cookiecutter-pylibrary


.. _pytest: http://pytest.org/latest/
.. _Travis-CI: http://travis-ci.org/
.. _Tox: http://testrun.org/tox/
.. _Sphinx: http://sphinx-doc.org/
.. _ReadTheDocs: https://readthedocs.org/
