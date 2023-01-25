Start script(s) for DEEP containers
==================================

deep-start
-----------

The **main start script** for DEEP containers. Automatically detects if NVIDIA-GPU is present in the system.
Default start is equivalent to ``deep-start -d``.

Usage: deep-start <options> 

    Options:
    -h|--help 		 the help message
    -c|--cpu 		 force CPU-only execuition (otherwise detected automatically)
    -g|--gpu 		 force GPU execution mode (otherwise detected automatically)
    -d|--deepaas 	 start deepaas-run
    -i|--install 	 enforce that the latest git repo of the deep-start script is installed
    -j|--jupyter 	 start JupyterLab; if not installed, will be automatically installed
    -o|--onedata 	 mount remote storage using oneclient
    -s|--vscode  	 start VSCode (code-server); if not installed, will be automatically installed
    -v|--version 	 print script version and exit
NOTE: if you try to start deepaas-run AND jupyterlab (or vscode), only deepaas-run will start!

run_jupyter.sh
--------------
** GOING TO BE DEPRICATED! KEPT FOR COMPATIBILITY. jupyter lab is started directly in the deep-start (as before, accepts jupyterOPTS for more options) **
Script to start jupyterlab, also checks jupyterOPTS environment for more advanced configuration

jupyter_notebook_config.py
--------------------------
Module to set Jupyter access password from the jupyterPASSWORD environment, if available.
BASED ON: https://github.com/tensorflow/tensorflow/blob/master/tensorflow/tools/docker/jupyter_notebook_config.py

(directory) lab
----------------
contains very basic configuration for Jupyter Lab

(directory) vscode
-------------------
contains very basic configuration for VSCode
