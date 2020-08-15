# Read:01 Summary
## Pain vs. Suffering (Summary)
* The pain that we maybe will  experience during this course like below :
  * we will be pushed mentally, having to think your way through problems that you had only even heard about a few hours beforehand.
  * we will have to research for hours on end
  * we will be pushed emotionally, constantly confronted with your own lack of understanding of a topic.
  * we will be pushed physically
  * we will lose sleep
 
***The greater the growth, the greater the pain.***
* suffering is pain without purpose. Pain with no higher goal. Pain with no dreams, no ambition, no aspiration.
---------------------------------------------------------------------------------------------------------------------------
## A beginner's guide to Big O notation(Summary)
* `Big O notation ` : describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to 
describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.
* ` O(1)` : describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.
* `O(N)` :  describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set
* `O(N2) `: represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.
* `O(2N) `: denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is 
exponential - starting off very shallow, then rising meteorically
* `O(log N) `: The iterative halving of data sets  produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase

---------------------------------------------------------------------------------------------------------------------------------------
## names and values in Python(Summary)
* names refers to values in python
* many names can refer to one value
* if we have a list ,so if we modify it then all names that referring to that list will change
* so the mechanisms almost the same between python  and other languages ,but the effects can be surprising in python 
-------------------------------------------------------------------------------------------------------------------------------------
## How to Setup an Awesome Python Environment for Data Science or Anything Else
***the most important thing when working with python: the interpreter.***
* `Pyenv :` Pyenv is a set of three tools, from which I present two here, that are pyenv(used to install python) andpyenv-virtualenv(used to configure your global tools).
* you can use pyenv to install almost any python interpreter, including pypy, and anaconda,etc ..
### Dependency Management
* `Poetry : ` comes with all the tools you might need to manage your projects dependencies in a deterministic way.

***poetry helps you to easily :***
  * manage your projects’ dependencies,
  * separate your projects through virtual environments,
  * build both applications as well as libraries without headaches.
  

* Before we start using poetry to create our first project ,we must configuring it, such that it creates your project’s virtual environment in a .venv
folder inside the project directory

> poetry config settings.virtualenvs.in-project true

> poetry config virtualenvs.in-project true

***Initialze a new project***

> poetry new dsexample 

> cd dsexample

***Add modules and create virtual environment.***

> poetry add pandas=0.25 fastapi --extras all

***As an example of how you could add a git module***

> poetry add tf2-utils --git git@github.com:Shawe82/tf2-utils.git

* `Black `: is a tool for python that allows you to focus on what is necessary, the content

***We add black as a development dependency with --dev as we don't need it when it comes to production***

> poetry add --dev black=19.3b0

***Assume we are inside the current toplevel dsexample folder***

> poetry run black .

* `Mypy`: is a static type checker for python code, that finds errors before they appear. Adding mypy and type-checking to your project using poetry 
is as easy as adding black

***We add mypy as a development dependency with --dev as we don't need it when it comes to production***

> poetry add --dev mypy

***Assume we are inside the current toplevel dsexample folder***

> poetry run mypy .

* `Pre-commit`: is a tool that executes checks before you commit code to your repository (I took for granted that your code is under git version control)

***Install pre-commit into the tools virtual env***

> pyenv activate tools

> pip install pre-commit 

***Leave the virtual env***

> pyenv deactivate

***As we have already added the tool venv, it will work directly***

> pre-commit --version

***To use it, you first need to add a config file called .pre-commit-config.yaml to the top-level folder of your project. In that file, you configure all the hooks
 that should run.***
 
##### Last, you must tell pre-commit to set up the hooks by executing

***I assume your are in the top level folder***

> pre-commit install










