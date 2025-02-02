# Serious Grid World Game (now with zombies!)

BWSI Serious Grid World. A project based approach to learning serious games with AI.

This README will help you get the game running so that you can start your own modifications.

## Prerequisites / Installation

First, you need to have Python on your system. If you think you already have python on your computer, you can double
check with the following: Open either `cmd` (Windows) or Terminal (macOS) and type `python --version`. 
If this throws an error, or shows a version less than Python 3.8, please follow the instructions below to install 
python version 3.8 (the code was tested on 3.8.5).

We are using Anaconda for our python package manager. Anaconda is nice because it comes include with a number of 
packages we will need. While we can provide an Anaconda env file for the project, we've found this actually complicates 
installation. Our plan for installation is to provide pip installation (another python package manager) of the 
packages that we need that are not in Anaconda.

Here are instructions for downloading anaconda. Download the latest version or one that comes with python 3.8 or greater.
Graphical installers [found here](https://www.anaconda.com/products/individual). The Anaconda download includes 
python so downloading Anaconda will get you most of the way there.

The final tool to make sure is set up properly is Git. For a Git primer, 
check out this [help page](https://docs.github.com/en/github/getting-started-with-github/set-up-git)

Once Anaconda, Python, and Git are installed, here are a list of packages that still need to be installed. To install 
these, use pip as follows:
`pip install tensorflow keras keras-rl2 gym>=0.2.3 pygame argparse uuid xlrd pandas matplotlib`

## Getting Started
Step 0: Install python and the required packages by following the Prerequisites / Installation above.

Clone this repository.

This will get all the repository files on your system. Python files in the main directory can be run to get
an idea of how to use the game.

# Game Details
Out of the box, this is a command line interface (CLI) game and can be ran from a command prompt (or terminal) or 
from an integrated development environment (IDE). The entry points for the code have "RUN" as a prefix.

For example, to run basic tests, use the following command. NOTE: this command prints the help commands
for the CLI options. It will show you the usage and options for the CLI.
```
python RUN_Basic.Tests.py -h
```

Running "RUN_Machine.py" shows the machine playing one round of the game.
Running "RUN_Human.py" allows for human play. Starting the game allows you to move the "ambulance" using the Arrow Keys.
Pressing Right/Left will "turn" the ambulance, without changing its position, while Up/Down will move the ambulance depending on its rotation
The ambulance has a certain amount of "energy" that is required for it to move. This energy is drained upon movement or contact with the environmental hazard.

