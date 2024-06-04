# Node.js for iOS/iPadOS [a-Shell](https://holzschu.github.io/a-Shell_iOS)
A [Node.js](https://nodejs.org)-like program that I coded for iOS/iPadOS a-Shell. It uses the jsc command, and it includes a fake [NVM](https://github.com/nvm-sh/nvm) (Node Version Manager).

> Coded in Python

> Please note that this is not an official release of Node.js, and that this program may not include every feature and some may be changed or tweaked

## Table of Contents:

- [Install](/#install)
- [Uninstall](/#uninstall)
- [Help Text](/#help-text)
  - [Node.js Help Text](nodejs-help-text)
  - [NVM Help Text](nvm-help-text)

### Install:

Install dependencies:

```
pip install colorama
```

Run these commands in a-Shell:

```
mkdir -p ~/Documents/.nvm/bin
curl https://github.com/XRG2014/node.js-a-shell/blob/main/.nvm/bin/nvm.py -o ~/Documents/.nvm/bin/nvm.py
curl https://github.com/XRG2014/node.js-a-shell/blob/main/.nvm/bin/node.py -o ~/Documents/.nvm/bin/node.py
```

Now run **ONLY ONE PAIR** of commands shown below:

> _This one uses ```~/Documents/.bashrc```_:

```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.bashrc
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.bashrc
```

> _This one uses ```~/Documents/.profile```_:

```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.profile
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.profile
```

### Uninstall:

(optional) Uninstall dependencies:

```
pip uninstall colorama
```

Run this command in a-Shell:

```
rm -rfv ~/Documents/.nvm
```

Now find these lines and remove them in ```~/Documents/.bashrc``` or ```~/Documents/.profile``` (Which ever file you used to install Node.js):

> If the lines don't exist in the file then Node.js might already be uninstalled

```
alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"
alias node="python3 -ub ~/Documents/.nvm/bin/node.py"
```

### Help Text:

#### Node.js Help Text

```
usage: node [--help] [--version] [--in-window] [--silent] [-hv?] <file>
    -?, -h, --help:  display help text
    -v, --version:   display current version
    --in-window:     runs inside the main window (this can change terminal appearance or behaviour; use with caution)
    --silent:        do not print output of the JavaScript execution
```

#### NVM Help Text

```
usage: nvm [--help] [--version] [-hv?] ...
    -?, -h, --help:              display help text
    -v, --version, version:      display current set version of Node
    ls-remote, version-remote:   list available Node releases / versions
    list:                        display all installed versions of Node
    ls:                          display all installed versions of Node with extra release info
    use, install:                set current version of Node
    alias:                       set Node version alias
    exec, run:                   run javascript program with Node
    which:                       display path to Node executable
```
