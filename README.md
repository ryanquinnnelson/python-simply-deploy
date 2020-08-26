# pythontemplate
A standard template for organizing python code in a git repository.

## Using this package
### Installation
1. Ensure you are inside a virtual environment.
2. Install the package. The easiest method is to follow package documentation on TestPyPi or PyPi, which will provide the exact `pip` command. For ease of use, the commands are repeated in this document. *Note that TestPyPi is periodically purged, so the distribution may no longer be available there.*
    ```shell script
    $ pip install pythontemplate-rnelson5 # from PyPi 
    ```
    ```shell script
    $ pip install -i https://test.pypi.org/simple/ pythontemplate-rnelson5==0.1.0  # from TestPyPi
    ```
    ```shell script
    $ pip install -e . # from local files (if downloaded)
    ```

### Execution via Command Line
1. Ensure you are inside the same virtual environment which you used to install the package.
2. Use an entry point from the distribution's `setup.py` file, if there is one.
```shell script
$ run-pythontemplate
```

### Execution via Python Interpreter
1. Ensure you are inside the same virtual environment which you used to install the package.
2. Start your interpreter, then import the package or functions from the package to use.
```shell script
$ python
>>> from pythontemplatepackage.pythontemplatemodule import get_id
>>> get_id('John')
123
```

### Package Usage in Another Python Project
1. Ensure you are inside the same virtual environment which you used to install the package.
2. Import the package or functions from the package to use.
    ```python
    from pythontemplatepackage.pythontemplatemodule import get_id
    ```




## Distributing this package
1. Ensure you are not inside a virtual environment.
2. Assemble a distribution using `wheel`
    ```shell script
    $ python3 setup.py sdist bdist_wheel
    ```
3. Upload the distribution using `twine`
    ```shell script
    $ python3 -m twine upload --repository testpypi dist/*
    Uploading distributions to https://test.pypi.org/legacy/
    Enter your username: __token__
    Enter your password: <TestPyPi API key>
    :
    View at:
    https://test.pypi.org/project/pythontemplate-rnelson5/0.1.0/
    ```
