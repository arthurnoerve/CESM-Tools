# CESM-Tools
Tools for running the CESM climate model in a manageable way.


## Installation
To download and extract the repo in the current folder do:
```
git clone https://github.com/arthurnoerve/CESM-Tools
```


## Setup
To make the commands executable from whereever clone/move the repo into your bin folder or add it to your PATH variable in your .bashrc/.bash_profile.

Remember to run ```chmod +x Q``` and ```chmod +x cesm``` to make them executable.


## Contents
* Q: Queue manager for the qsub/qstat command
* cesm: Main cesm interface


## Q
You can do:
```
Q # list all current jobs
Q sub "job" #submit the job to the queue system
```


## cesm
The first time you use the tool you should run ```cesm config``` to set up the environment variables.

```bash
cesm list #list cases
cesm create "case" #create new case
cesm setup "case" #run cesm setup
cesm build "case" #build/compile case
cesm sub "case" #add case to queue
cesm restart "case" "from case" #Copy restart files from "from case" to the input folder of "case"
cesm config #setup env vars
```
