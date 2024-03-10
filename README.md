# Node.js for [a-Shell](https://holzschu.github.io/a-Shell_iOS)
A version of Node that I coded for ios a-Shell. It uses the jsc command, and it includes a fake NVM (Node Version Manager).

### Install (for a-Shell):

Run these commands in a-Shell:

```
mkdir -p ~/Documents/.nvm/bin
curl -o ~/Documents/.nvm/bin/nvm.py
curl -o ~/Documents/.nvm/bin/node.py
```

Now run **ONLY ONE PAIR** of commands shown below:

> _This one uses ```~/Documents/.bashrc```:_
```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.bashrc
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.bashrc
```

> _This one uses ```~/Documents/.profile```:_
```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.profile
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.profile
```

### Uninstall (for a-Shell)

Run this command in a-Shell:

```
rm -rfv ~/Documents/.nvm
```

Now find these lines and remove them in ```~/Documents/.bashrc``` and ```~/Documents/.profile``` (if one file doesn't exist, then do the other one):

```
alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"
alias node="python3 -ub ~/Documents/.nvm/bin/node.py"
```
