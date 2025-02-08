# ArcoLinux Python3 Virtual Environment Setup


List all Outdated packages in Python:
pip list --outdated

pip list --outdated                                                                                            [20:59:32]
Package    Version Latest Type
---------- ------- ------ -----
setuptools 65.5.0  69.0.2 wheel

How to Upgrade a python package:
pip3 install msgpack==1.0.7gV8

## GO: To (https://pypi.org/project/numpy/). and Search for package latests version
## Then run this command with the updated verion number.

### How to install Python3 Utilities

```python3
$ pipx install pyjokes
```


┌─[srhills@minipcpn62] - [~] - [1052]
└─[$] python -m site --user-site

/home/srhills/.local/lib/python3.11/site-packages

## Create a Python Virtual Environment

python3 -m venv venv

## Activate the Virtual Environment

. venv/bin/activate

## Exit the Python Virtual Environment

In case you need to leave or deactivate the virtualenv environment run the following command.

deactivate

```
You can list only packages in the virtualenv by pip freeze --local or pip list --local. This option works irrespective of whether you have global site packages visible in the virtualenv.
```
## In Python3

pip list

Empty venv is

Package    Version
---------- ------- 
pip        19.2.3 
setuptools 41.2.0

To create a new environment

python3 -m venv your_foldername_here

Activate

cd your_foldername_here
source bin/activate

Deactivate

deactivate

```
After completing this step, you will notice that your terminal changes. 
Some will place (env) or (venv) at the beginning of your terminal line. 
Other terminals and terminal modifications may have different 
indications but something will change to indicate that you are 
now in the virtual environment.
```
At this point, you can proceed to install pip packages and they will be specific to this project.

pip3 install pynvim
pip3 install pyperclip
pip3 install cryptography
pip3 install pyshorteners

## Using Pacman Package Manager

sudo pacman -S python-pynvim
sudo pacman -S python-pyperclip
sudo pacman -S python-cryptography
sudo pacman -S python-pyshorteners
OR
pip3 install pyshorteners --break-system-packages


## AND To Upgrade Packages Use

pip3 install --upgrade pip

# To comment

Press ESC
hit V
Move the cursor until desired lines to comment
hit :
'<,'>s/^/#/g

# To uncomment

Do the same, but command is:
'<,'>s/^#//g

# '<,'> indicates the range you've selected with VISUAL MODE.

# To comment

ESC
ctrl+v 
Move the cursor until desired end of lines to comment
I
type what to want to insert at the begining of the line
Esc
What you wrote should now be at the begining of every line you selected

# To uncomment

Esc
ctrl+v
select the column(s) you want to deleted

## Installing Packages

pip supports installing from PyPI, version control, local projects, and directly from distribution files.

The most common scenario is to install from PyPI using Requirement Specifiers

## Linux

python -m pip install SomePackage            # latest version
python -m pip install SomePackage==1.0.4     # specific version
python -m pip install 'SomePackage>=1.0.4'     # minimum version

Examples

Install SomePackage and its dependencies from PyPI using Requirement Specifiers
Unix/macOS

python -m pip install SomePackage            # latest version
python -m pip install 'SomePackage==1.0.4'   # specific version
python -m pip install 'SomePackage>=1.0.4'   # minimum version

Windows

Install a list of requirements specified in a file. See the Requirements files.
Unix/macOS

python -m pip install -r requirements.txt

Windows

Upgrade an already installed SomePackage to the latest from PyPI.
Unix/macOS

python -m pip install --upgrade SomePackage

Windows

Install a local project in “editable” mode. See the section on Editable Installs.
Unix/macOS

python -m pip install -e .                # project in the current directory
python -m pip install -e path/to/project  # project in another directory

Windows

Install a project from VCS
Unix/macOS

python -m pip install 'SomeProject@git+https://git.repo/some_pkg.git@1.3.1'

Windows

Install a project from VCS in “editable” mode. See the sections on VCS Support and Editable Installs.
Unix/macOS

python -m pip install -e 'git+https://git.repo/some_pkg.git#egg=SomePackage'          # from git
python -m pip install -e 'hg+https://hg.repo/some_pkg.git#egg=SomePackage'            # from mercurial
python -m pip install -e 'svn+svn://svn.repo/some_pkg/trunk/#egg=SomePackage'         # from svn
python -m pip install -e 'git+https://git.repo/some_pkg.git@feature#egg=SomePackage'  # from 'feature' branch
python -m pip install -e 'git+https://git.repo/some_repo.git#egg=subdir&subdirectory=subdir_path' # install a python package from a repo subdirectory

Windows

Install a package with extras.
Unix/macOS

python -m pip install 'SomePackage[PDF]'
python -m pip install 'SomePackage[PDF] @ git+https://git.repo/SomePackage@main#subdirectory=subdir_path'
python -m pip install '.[PDF]'  # project in current directory
python -m pip install 'SomePackage[PDF]==3.0'
python -m pip install 'SomePackage[PDF,EPUB]'  # multiple extras

Windows

Install a particular source archive file.
Unix/macOS

python -m pip install './downloads/SomePackage-1.0.4.tar.gz'
python -m pip install 'http://my.package.repo/SomePackage-1.0.4.zip'

Windows

Install a particular source archive file following PEP 440 direct references.
Unix/macOS

python -m pip install 'SomeProject@http://my.package.repo/SomeProject-1.2.3-py33-none-any.whl'
python -m pip install 'SomeProject @ http://my.package.repo/SomeProject-1.2.3-py33-none-any.whl'
python -m pip install 'SomeProject@http://my.package.repo/1.2.3.tar.gz'

Windows

Install from alternative package repositories.

Install from a different index, and not PyPI
Unix/macOS

python -m pip install --index-url http://my.package.repo/simple/ SomePackage

Windows

Install from a local flat directory containing archives (and don’t scan indexes):
Unix/macOS

python -m pip install --no-index --find-links=file:///local/dir/ SomePackage
python -m pip install --no-index --find-links=/local/dir/ SomePackage
python -m pip install --no-index --find-links=relative/dir/ SomePackage

Windows

Search an additional index during install, in addition to PyPI

Warning

Using this option to search for packages which are not in the main repository (such as private packages) is unsafe, per a security vulnerability called dependency confusion: an attacker can claim the package on the public repository in a way that will ensure it gets chosen over the private package.
Unix/macOS

python -m pip install --extra-index-url http://my.package.repo/simple SomePackage

Windows

Find pre-release and development versions, in addition to stable versions. By default, pip only finds stable versions.
Unix/macOS

python -m pip install --pre SomePackage

Windows

Install packages from source.

Do not use any binary packages
Unix/macOS

python -m pip install SomePackage1 SomePackage2 --no-binary :all:

Windows

Specify SomePackage1 to be installed from source:
Unix/macOS

python -m pip install SomePackage1 SomePackage2 --no-binary SomePackage1


[My Python3 Virtual .venv Local]( /home/srhills/.venv )

If not installed then run this command:

Install venv

In order to install venv, we need to install the following packages:

` sudo apt install python3-venv`

After that Initialize the environment

Initialization of a Virtual Environment

Go to the root destination of your project and run the following command:

` python3 -m venv .venv `

This will create a virtual environment in the current directory. 
The virtual environment folder will be named
.venv

Now cd into the Project directory

cd .venv

Then run this command:

Activation of a Virtual Environment cd into the project directory

In order to activate a virtual environment, from the root directory of your project, run the following command:

source .venv/bin/activate

Check if the virtual environment is activated by running the following command:

which python3

The output should be with ../.venv/bin/python as the output.

You can add an alias to your bash profile to make it easier to activate the virtual environment:

we can have a look at whats in the directory with this command:

ls ~/.venv/bin

To look at the configuration file:

less ~/.venv/bin/activate

Please use this alias to Activate the .venv

alias activate='source .venv/bin/activate'

Run: env --> inside directory to see all Environment variables
Deactivation of a Virtual Environment

When you are done with the virtual environment, you can deactivate it by running the following command:

deactivate

Or alternatively you can exit the current shell.

Note: We can start a New Virtual Environment with this command:

virtualenv -p python3 venv


[](https://3os.org/development/python/virtualenv/#activation-of-a-virtual-environment)

About Python Virtual Environment - venv¶

venv is a tool to create isolated Python environments. Since Python 3.3, a subset of it has been integrated into the standard library under the venv module.

The venv module provides support for creating lightweight “virtual environments” with their own site directories, optionally isolated from system site directories. Each virtual environment has its own Python binary (which matches the version of the binary that was used to create this environment) and can have its own independent set of installed Python packages in its site directories.



## [The right way for ArchLinux](https://tinyurl.com/yo4jwbx7)

The right way to install PYTHON packages in ArchLinux is using PACMAN! To install packages to Python3 you have to use

sudo pacman -S python-'package'

If you want to install packages from Python2, you have to use

sudo pacman -S python2-'package'

Most python packages are in the ArchLinux repositories and the packages that are not in AUR (ArchLinux User Repositories) - for these packages you have to download the PKGBUILD file and compile. After that, you have to use PACMAN to finish the installation

makepkg -s
sudo pacman -U 'compiled-package'

The second right way for ArchLinux

When the package isn't in the AUR or the PKGBUILD isn't working, you can use PIP to install it to Python3

sudo pip install 'python-package'

or Python2

sudo pip2 install 'python-package'

BE AWARE: when you are using pip the same installation folder is shared with pacman and most of time, especially when you are updating all system packages (sudo pacman -Suy), will raise a conflict error. You always have to prefer the first option above.To solve conflict problems, just uninstall pip package and install they equivalent package on pacman (pip uninstall 'python-package').
You could give a chance to virtualenv or even conda

If you are planning to develop some python application or python package your better option is use virtual environments.

For python packaging applications you should try poetry it is current better option to manage application from start to finish. It is a much better option than requirements.txt + setup.py.

Another more simple option is use python-virtualenv. This can bring portability to your code and maintain old packages as well. Install it with

sudo pacman -S python-virtualenv

and try this

virtualenv -p /usr/bin/python3 yourenv
source yourenv/bin/activate
pip install package-name

When you create this environment yourenv, you will setup pip to install packages only into this environment, not to the entire system.
These other links can be useful with you want to learn more about managing packages on Linux with conda or virtualenv:

Installing Python Packages from a Jupyter Notebook

If you follow these rules, your ArchLinux will not break and won't have dependency problems between PACMAN and PIP.

Hope it's useful!
