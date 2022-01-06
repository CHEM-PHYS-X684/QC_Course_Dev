# CHEM/PHYS 3684 Setup 
Download and install data for course modules

## Installation

### System wide installs

1. Install `python`

    I assume you already have python installed on your computer. However this is probably python-2.7 which is no longer supported. Follow this link to download/install the latest version of `python`: https://www.python.org/downloads/
    
1. Install `git`

    It's likely that this has also already been installed on your computer. 
    If it hasn't, just follow the instructions here: https://github.com/git-guides/install-git

1. Install `virtualenv`

    Virtual environments make it easy to manage multiple python projects. Imagine that you have two projects, A and B. 
    Project A requires NumPy (v1.17.2) whereas Project B requires NumPy (v1.22.0).
    You could install v1.17.2, do some work on project A. Then uninstall NumPy, install v1.22.0 then do some work on project B. 
    Then go back to v1.17.2, and continue until you pull all your hair out. This would be insane no?
    Luckily we can use so-called *virtual environments* which allow us to create an *environment* specific to a given project.
    In this context, *environment* is used to refer to a list of installed packages that you have access to when building your own python code. 
    There are two different approaches used for creating and maintaining project-specific environments:
    1.  Anaconda: https://docs.conda.io/en/latest/
    2.  VirtualEnv: https://virtualenv.pypa.io/en/latest/index.html
   
    Read more here: [read](topics/virtual_env.md)


    Either can work, but for this class we will use virtualenv. Install `virtualenv` by typing:
        
        python -m pip install --user virtualenv

### Course Material Install/Setup

3. Download latest course content from GitHub. This will create a local repository (existing locally on your computer) which contains all the course modules.

        git clone https://github.com/robs84/QC_Course_Dev.git
        
    Change directory (`cd`) into the new folder.
    
        cd QC_Course_Dev

2. Create virtual environment. With `virtualenv` installed as described above, we can now create a virtual environment inside of our current directory:
        
        virtualenv -p python3 venv
        
    Now we will *activate* the environment so that when we type `python` it will use this new environment.
    
        source venv/bin/activate
        
    At this point, any software or packages we install with the `pip` command will be installed into the environment contained in the `./venv` directory. 
    
    > Tips: 
          Should we want to deactivate the environment, simply type `deactivate`. 
            Also, if you want to delete the environment and start over, you can just remove the `venv` folder, and all the downloaded packages are gone!
      

3. Install. By specifying the `-r requirements.txt` you are telling `pip` to install all the packages specified in the `requirements.txt` file. Since you have already activated your `virtualenv` these packages will now be in your environment. 

        pip install -r requirements.txt

4. Run tests. This will ensure that things are working correctly.

        pytest test/*.py


Now that you've installed Qiskit to your local machine, let's start familiarizing ourselves with it!

There are two modules that will briefly demonstrate visualization and simulation of quantum circuits using Qiskit.  You are highly encouraged to delve deeper into Qiskit as your schedule permits, which will help you with coding later in the semester.  Below, please find a brief description of these modules.  Each module will include some questions to answer, some of which may be facilitated by understanding Dirac notation.  Anyone who has no experience with such notation can let me know and we will work out a tutorial session.

Introduction to State Visualization will have several small steps with the goal of understanding what some fundamental one-qubit gates do when operating on a qubit of a given state.  This understanding will come from visualizing roataions about the Bloch sphere.

Introduction to superposition and entanglement will highlight two frequently used gates, the Hadamard and CNOT (or CX) gates.  The Hadamard gate takes a qubit of known state and yields a normalized linear combination of staes in that basis.  The CNOT gate will perform a NOT operation on the second qubit if the first (control) qubit is $|1\rangle$ and will not perform any operation if the control qubit is $|0\rangle$, in the computational basis.
