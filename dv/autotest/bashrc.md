https://www.routerhosting.com/kb/what-is-linux-bashrc-and-how-to-use-it-full-guide/
```linux
vim ~/.bashrc

copy/insert commands to the end file. For example:
export PYTHONPATH=$(pwd)/atsdk_ci:${PYTHONPATH}
export PATH=$(pwd)/atsdk_ci/scripts:${PATH}

save and quit file
source ~/.bashrc 
