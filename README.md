# python-installattion

### This repo has been created for the correct installation of python2, python3, pip2 and pip3 all at the same time, same machine. (Ubuntu, as of April, 2021)

- Before starting manually, please try running install.sh script, if it gives an error, you can always go step-by-step manually:

#### Check for installed python
1. First and foremost, **please** check if you have python3.8, python3 or python2 (python2.7) installed on your machine. Normally you should only have python3.8 installed on ubuntu *by default*.

2. Type ```python3 --version``` to check the version of python installed on your computer.<br />
It should give you :
```sh
Python 3.8.5
```
3. And if you have fresh Ubuntu that has just been installed (or relatively fresh), the command<br />
```python --version``` **should not** print out anything.

4. Assuming you are set until now, you can start doing the procedures as follows.

#### Install Python 3.8 and pip3
1. First, as you already have the Python 3.8.5, you can start installing **pip3** by the below command:<br />
```sh
sudo apt install python3-pip
```
as mentioned, it will install pip3 for python3 (obviously), you can also check if it is installed by typing<br />
```sh
pip3 --version
```
- This will print something similar to<br />
```pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)```<br /><br />
**NOTE:** *The pip version at the beginning may be different from that of what mentioned in the above example. The main thing is that it should print python3.\* (any python version after python3) in parentheses.*<br />
Now that we have ```python3.8``` and ```pip3``` set, we should be able to move onto the next steps.<br />
- 
