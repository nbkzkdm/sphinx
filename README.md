# sphinx

sphinxサンプル

[Sphinx](https://www.sphinx-doc.org/ja/master/)


``` shell
pip3 install sphinx
```


``` shell
mkdir docs
```

``` shell
$ sphinx-build --version
sphinx-build 7.4.7
```

``` shell
$ sphinx-quickstart docs
Welcome to the Sphinx 7.4.7 quickstart utility.

Please enter values for the following settings (just press Enter to
accept a default value, if one is given in brackets).

Selected root path: docs

You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: y

The project name will occur in several places in the built documentation.
> Project name: SampleProject
> Author name(s): nbkz.Kdm
> Project release []: 1.0.0

If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.

For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: ja

Creating file /home/vagrant/sphinx/docs/source/conf.py.
Creating file /home/vagrant/sphinx/docs/source/index.rst.
Creating file /home/vagrant/sphinx/docs/Makefile.
Creating file /home/vagrant/sphinx/docs/make.bat.

Finished: An initial directory structure has been created.

You should now populate your master file /home/vagrant/sphinx/docs/source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

[vagrant@vbox sphinx]$ ll
total 4
drwxr-xr-x. 4 vagrant vagrant 4096 Mar  5 13:37 docs
-rw-r--r--. 1 vagrant vagrant    0 Mar  5 13:34 main.py
[vagrant@vbox sphinx]$ ll docs/
total 16
drwxr-xr-x. 2 vagrant vagrant 4096 Mar  5 13:37 build
-rw-r--r--. 1 vagrant vagrant  804 Mar  5 13:37 make.bat
-rw-r--r--. 1 vagrant vagrant  638 Mar  5 13:37 Makefile
drwxr-xr-x. 4 vagrant vagrant 4096 Mar  5 13:37 source
```

``` shell
cd docs
sphinx-apidoc -f -o ./source/ ../src
```

``` shell
$ tree
.
├── docs
│     ├── build
│     ├── make.bat
│     ├── Makefile
│     └── source
│         ├── conf.py
│         ├── index.rst
│         ├── memo
│         │     └── sphinx.rst
│         ├── modules.rst
│         ├── samplePy.rst
│         ├── _static
│         └── _templates
│             ├── conf.py
│             ├── index.rst
│             ├── memo
│             │     └── sphinx.rst
│             └── _static
├── README.md
└── src
    ├── __pycache__
    │     └── samplePy.cpython-39.pyc
    └── samplePy.py
```