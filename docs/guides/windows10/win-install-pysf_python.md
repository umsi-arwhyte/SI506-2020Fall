# Windows 10: Installing Python 3.x

There are several ways to install and manage Python on Windows 10. One method involves obtaining
Python from the Python Software Foundation [website](https://www.python.org/).

:exclamation: As of 20 July 2020 the latest stable
[release](https://www.python.org/downloads/mac-osx/) in the Python 3.x series is Python 3.8.5. You
can also run Python 3.7 (3.7.8 is the latest maintenance release) if already installed.

:warning: Installing Python 3.x is straightforward but involves clicking a checkbox during the
installation process that ensures the Python environment variables are added to the `PATH` variable.
_Clicking the checkbox is a critically important step_; failure to configure the install process
properly will require manually adding the environment variables (not fun) or deleting the Python
install and starting over.

## 1.0 Check for previous install

First, confirm whether or not Python is installed on your machine.

### 1.1 Open PowerShell

Next to the `Start` button located at the lower left corner of the screen, enter "PowerShell" in the
search box. This will surface the Windows PowerShell app. Click "Open" to start the shell (you can
also run it as Administrator).

![Windows 10 search for PowerShell](assets/win-search_powershell.png)

### 1.2 Check if Python 3.x is installed

At the prompt, type `python --version` and then press __Enter__.

:bulb: Windows users invoke Python by typing `python` _not_ `python3`.

```commandline
PS C:\Users\arwhyte> python --version
Python 3.8.5
```

If Python version 3.8.5 or above is returned, you have the correct version of Python installed on
your machine. _Proceed no further and exit this install guide_.

The more likely scenario is that _no version information is returned_. No problem, installing
Python 3.x is not difficult.

To close a PowerShell session type 'exit' at the prompt and then press the __Return__ key.

:bulb: If you are running an earlier version of Python 3 you can remove it by searching for
"Settings" in the search box on the taskbar. Open the Settings app, then click on "Apps". Scroll
down the list of installed apps and when you reach Python, click on it and then click the
"Uninstall" button.

## 2.0 Download and install Python 3.x

Once you've checked your machines for previous Python installs, visit the Python Software Foundation
[website](https://www.python.org) and download the lastest stable Python 3.x release.

### 2.1 Download Python 3.x

:warning: Downloading Python 3.x from the Python Software Foundation's home page (as described
below) defaults to a 32 bit version of the latest stable release. If you prefer to download and
install the 64 bit version of Python 3.x visit
[https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/) and download
either Windows x86-64 executable installer or x86-64 web-based installer.

Hover over "Downloads" on the blue menu bar. Your Windows 10 operating system version should have
been detected on the page load and the link to the Python 3.8.x release package displayed as a grey
button. Click the grey button to download the install package.

![Python Software Foundation Python for Windows download](assets/win-install_python_pysf_download_3_8_5.png)

Windows 10 will ask "What do you want to do with `python-3.8.1.exe` (25.2 MB)?" Click the grey
`Save` button.

### 2.2 Install Python 3.x

Once the Python installer `*.exe` file is downloaded click the grey "Open folder" button. Then
double-click the Python installer `*.exe` file icon to start the install process.

#### 2.2.1 Click the install checkbox "Add Python 3.8 to PATH"

:warning: __Before__ clicking the "Install Now" box you __MUST__ click the checkbox
"Add Python 3.8 to PATH". Selecting this option ensures that the necessary Python environment
variables are added during the installation process.

Adding Python to the `PATH` variable ensures that you can call `python` _directly_ from the
PowerShell or Command Prompt. If you fail to click the checkbox you (or likely your friendly
instructor or GSI) will need to set your Python environment variables manually. Manually adding
Windows environment variables is tedious work.

Do this:

1. click the "Add Python 3.8 to PATH" checkbox
2. click "Install Now"
3. click the "Yes" button to allow the installer to make changes to the system.

At the end of the installation process you have the option to disable the 260 max character path
length limit. I opted to disable it.

![Windows Python install click add Path](assets/win-install_python_add_path_3_8_5.png)

### 2.3 Confirm installation

Once installed return to PowerShell and type "exit" and then press __Enter__ to close the app.
Restart PowerShell and confirm that Python 3 has been installed successfully.

```commandline
PS C:\users\arwhyte> python --version
Python 3.8.5
```

Then at the prompt type `python` and press __Enter__ to start the Python Interpreter. Issue the
following `print()` statement:

```commandline
PS C:\users\arwhyte> python

>>> print('I just installed Python 3 on my laptop.')
I just installed Python 3 on my laptop.
```

:bulb: You can also start and run the Python Interpreter using the Command Prompt app (`cmd`).

![Windows Search for Command Prompt app](assets/win-search_cmd_app.png)

![Windows Python Command Prompt](assets/win-cmd-python_interp.png)

## 3.0 Source code editor

The Windows Python installer also installs Python's Integrated Development and Learning Environment
(IDLE). The `IDLE` app provides a multi-window text editor, interactive shell window,
search/replace, and debugger. It is one of several text editors that you can use to write and test
Python code. To learn more about IDLE see
[https://docs.python.org/3/library/idle.html](https://docs.python.org/3/library/idle.html).

:exclamation: The SI 506 teaching team __does not__ use IDLE. Instead, we use Microsoft's popular
(and free) [Visual Studio Code](https://code.visualstudio.com/) which serves as the default source
code editor for this course. See the companion guide
[Windows 10: Installing Visual Studio Code](win-install_vscode_with_py_extension.md) for installation
instructions.

## License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
