# CHEM/PHYS 3684 Setup 
Download and install data for course modules

## Installation

1. Install `python`

    I assume you already have python installed on your computer. However this is probably python-2.7 which is no longer supported.  
    Follow this link to download/install the latest version of `python`: https://www.python.org/downloads/
    
1. Install `git`

    It's likely that this has also already been installed on your computer. 
    If it hasn't, just follow the instructions here: https://github.com/git-guides/install-git

1. Download

        git clone https://github.com/robs84/QC_Course_Dev.git
        cd QC_Course_Dev

2. create virtual environment (optional)

        virtualenv -p python3 venv
        source venv/bin/activate

3. Install 

        pip install .

4. run tests

        pytest test/*.py


Now that you've installed Qiskit to your local machine, let's start familiarizing ourselves with it!

There are two modules that will briefly demonstrate visualization and simulation of quantum circuits using Qiskit.  You are highly encouraged to delve deeper into Qiskit as your schedule permits, which will help you with coding later in the semester.  Below, please find a brief description of these modules.  Each module will include some questions to answer, some of which may be facilitated by understanding Dirac notation.  Anyone who has no experience with such notation can let me know and we will work out a tutorial session.

Introduction to State Visualization will have several small steps with the goal of understanding what some fundamental one-qubit gates do when operating on a qubit of a given state.  This understanding will come from visualizing roataions about the Bloch sphere.

Introduction to superposition and entanglement will highlight two frequently used gates, the Hadamard and CNOT (or CX) gates.  The Hadamard gate takes a qubit of known state and yields a normalized linear combination of staes in that basis.  The CNOT gate will perform a NOT operation on the second qubit if the first (control) qubit is $|1\rangle$ and will not perform any operation if the control qubit is $|0\rangle$, in the computational basis.
