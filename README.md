# python-installattion

### This repo has been created for the correct installation of python2, python3, pip2 and pip3 all at the same time, same machine. Because there are still many scripts present that require Python 2, I decided to show the steps to achieve the correct installation for every necessary version of both python and pip <br />(Ubuntu, as of April, 2021).

## Table of Content
- [Try running the provided script first](#try-running-the-provided-script-first)
- [Check for installed python](#check-for-installed-python)
- [Install Python 3 and pip3](#install-python-3-and-pip3)
- [Install Python 2 and pip2](#install-python-2-and-pip2)
- [Check if all are set](#check-if-all-are-set)


### Try running the provided script first
Before starting manually, please try running the ```install.sh``` script, if it gives an error, you can always go step-by-step manually.
```sh
chmod +x install.sh
./install.sh
```

### Check for installed python
1. First and foremost, **please** check if you have python3.8, python3 or python2 (python2.7) installed on your machine. Normally you should only have python3.8 installed on ubuntu *by default*.

2. Type ```python3 --version``` to check the version of python installed on your computer.<br />
It should give you :
```sh
Python 3.8.5
```
3. And if you have fresh Ubuntu that has just been installed (or relatively fresh), the command<br />
```python --version```, ```python2 --version```, ```python2.7 --version``` **should not** print out anything.

4. Assuming you are set until now, you can start doing the procedures as follows.

### Install Python 3 and pip3
First, as you already have the Python 3.8.5, you can start installing **pip3** by the below command:<br />
```sh
sudo apt install python3-pip
```
as mentioned, it will install pip3 for python3 (obviously), you can also check if it is installed by typing<br />
```sh
pip3 --version
```

This will print something similar to<br />
```pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)```<br /><br />
**NOTE:** *The pip version at the beginning may be different from that of what mentioned in the above example. The main thing is that it should print python3.\* (any python version after python3) in parentheses.*<br />
Now that we have ```python3.8``` and ```pip3``` set, we should be able to move onto the next steps.<br />


### Install Python 2 and pip2
You can start installing Python 2 by typing
```sh
sudo apt install python2
```
It will install the scripts **python2**, **python2.7** in ```/usr/bin/``` making them accessible through everywhere.<br />
Check the installation by typing ```python2 --version``` which should print
```sh
Python 2.7.*
```
Now you should download and install **pip2** for *Python 2* through online script
```sh
curl https://bootstrap.pypa.io/pip/2.7/get-pip.py -o get-pip.py
```
This will download and save the installer script to ```get-pip.py``` file.<br />
Run the script to finally install pip2 **pip2**
```sh
python2 get-pip.py
```
After the installation is done, there is one last step you should do in order to use **pip2**.<br /><br />
As the last step, you should add the directory that the script *pip2* is installed in, which will be<br />
```/home/<username>/.local/bin``` (replace \<username\> with yours).<br /><br />
Just open your ```.bashrc``` file with ```sudo nano ~/.bashrc```, and add this line to the end of the file.<br />
```sh
export PATH="/home/<username>/.local/bin:$PATH"
```
It simply concatenates the ```$PATH``` variable with the new directory string in order to establish an even access to the **pip2** script from anywhere.


### Check if all are set
You can check by the below commands if you have python3, python2, pip3 and pip2 all at the same time and working!
```sh
python3 --version
python2 --version
pip3 --version
pip2 --version
```
These 4 commands should output you the corresponding versions for the mentioned scripts.
