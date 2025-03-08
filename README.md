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



```shell
$ sphinx-apidoc --help
usage: sphinx-apidoc [OPTIONS] -o <OUTPUT_PATH> <MODULE_PATH> [EXCLUDE_PATTERN, ...]

Look recursively in <MODULE_PATH> for Python modules and packages and create one reST file with automodule directives per package in the <OUTPUT_PATH>. The <EXCLUDE_PATTERN>s can be file and/or
directory patterns that will be excluded from generation. Note: By default this script will not overwrite already created files.

positional arguments:
  module_path           path to module to document
  exclude_pattern       fnmatch-style file and/or directory patterns to exclude from generation

optional arguments:
  -h, --help            show this help message and exit
  --version             show program's version number and exit
  -o DESTDIR, --output-dir DESTDIR
                        directory to place all output
  -q                    no output on stdout, just warnings on stderr
  -d MAXDEPTH, --maxdepth MAXDEPTH
                        maximum depth of submodules to show in the TOC (default: 4)
  -f, --force           overwrite existing files
  -l, --follow-links    follow symbolic links. Powerful when combined with collective.recipe.omelette.
  -n, --dry-run         run the script without creating files
  -e, --separate        put documentation for each module on its own page
  -P, --private         include "_private" modules
  --tocfile TOCFILE     filename of table of contents (default: modules)
  -T, --no-toc          don't create a table of contents file
  -E, --no-headings     don't create headings for the module/package packages (e.g. when the docstrings already contain them)
  -M, --module-first    put module documentation before submodule documentation
  --implicit-namespaces
                        interpret module paths according to PEP-0420 implicit namespaces specification
  -s SUFFIX, --suffix SUFFIX
                        file suffix (default: rst)
  --remove-old          Remove existing files in the output directory that were not generated
  -F, --full            generate a full project with sphinx-quickstart
  -a, --append-syspath  append module_path to sys.path, used when --full is given
  -H HEADER, --doc-project HEADER
                        project name (default: root module name)
  -A AUTHOR, --doc-author AUTHOR
                        project author(s), used when --full is given
  -V VERSION, --doc-version VERSION
                        project version, used when --full is given
  -R RELEASE, --doc-release RELEASE
                        project release, used when --full is given, defaults to --doc-version

extension options:
  --extensions EXTENSIONS
                        enable arbitrary extensions
  --ext-autodoc         enable autodoc extension
  --ext-doctest         enable doctest extension
  --ext-intersphinx     enable intersphinx extension
  --ext-todo            enable todo extension
  --ext-coverage        enable coverage extension
  --ext-imgmath         enable imgmath extension
  --ext-mathjax         enable mathjax extension
  --ext-ifconfig        enable ifconfig extension
  --ext-viewcode        enable viewcode extension
  --ext-githubpages     enable githubpages extension

Project templating:
  -t TEMPLATEDIR, --templatedir TEMPLATEDIR
                        template directory for template files

For more information, visit <https://www.sphinx-doc.org/>.
```
















