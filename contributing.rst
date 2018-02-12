How to install for developing
-----------------------------

Clone the repository with::

    git clone git@github.com:PLOS/allofplos.git

Install from the downloaded directory with::

    pip install -U -e /local/path/allofplos


Thing to check before doing a release
-------------------------------------

* Run the tests
* Version number is stated in the setup.py file
* HISTORY.txt file with the last change at the beginning

Making a release
----------------
Remove untracked files::
	git clean -xfdi

Delete previous packages from dist directory::

    rm dist/*.*

Run bdist_wheel::

    python setup.py bdist_wheel --universal

Upload with twine::

    twine upload dist/*

(you will need pypi credentials to do the upload)
