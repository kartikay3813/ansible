Directory stracture of roles?
Ans. The concept of an Ansible role is simple; it is a group of variables, tasks, files, and handlers stored in a standardised file structure. Above all, 
      we always have the freedom to write our tasks and variable.
    Defaults:
    The defaults directory is for defining the variable defaults. The variables in default have the lowest priority thus becoming easy to override. If definition     of a variable is nowhere else, the variable in defaults/main.yml will be used.

    Files:
    We use the files directory to add files that are needed by provisioning machine, without modification. Mostly, we use copy task for referencing files in the       files directory. The most interesting part about this is that Ansible does not require a path for resources stored in files directory when working in the         role.

    Handlers:
    The handlers directory is used for storing Ansible handlers. Handlers are tasks that may be flagged during a play to run at the play’s completion. We can have      as many and as few handlers as we need.

    Tasks:
    The task directory is where we write most of our roles which includes all the tasks our role will perform. We write each series of tasks in a separate file       and include them into the main.yml file in the tasks directory.

   Templates:
   We use the template directory to also add files to our machine(similar to files directory). Only difference between template and files directories is that the    template directory supports alteration (modification). Jinja2 language to used to create these alteration. Most software configuration files become templates.

   Tests:
  We can use the tests directory if we have built and automated testing process around our role. This directory contains a sample inventory and a test.yml file.

  Vars:
  This is where we create variable files that define necessary variables for our role. The variables defined in this directory are meant for role internal use        only. Also, it is a good idea to namespace our role variable names, to prevent potential naming conflicts with variables outside of our role.
  
  What is ansible vault?
   Ansible feature that helps you encrypt confidential information without compromising security
