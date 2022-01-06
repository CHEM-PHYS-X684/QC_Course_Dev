# Virtual Environments

    Virtual environments make it easy to manage multiple python projects. Imagine that you have two projects, A and B. 
    Project A requires NumPy (v1.17.2) whereas Project B requires NumPy (v1.22.0).
    You could install v1.17.2, do some work on project A. Then uninstall NumPy, install v1.22.0 then do some work on project B. 
    Then go back to v1.17.2, and continue until you pull all your hair out. This would be insane no?
    Luckily we can use so-called *virtual environments* which allow us to create an *environment* specific to a given project.
    In this context, *environment* is used to refer to a list of installed packages that you have access to when building your own python code. 
    There are two different approaches used for creating and maintaining project-specific environments:
    1.  Anaconda: https://docs.conda.io/en/latest/
    2.  VirtualEnv: https://virtualenv.pypa.io/en/latest/index.html
