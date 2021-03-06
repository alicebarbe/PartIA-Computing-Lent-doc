Getting started
===============

.. You will be developing programs in Python using multiple files, editors,
  the command-line, and version control. This is the usual way of
  creating *libraries*, especially for larger projects. To help you
  start, a skeleton repository in which some tasks have already been
  completed is provided as a starting point.

.. To get started:

#. Read the :ref:`Requirements` section.

#. Install, configure and test your development environment
   (`Development environment`_).

#. Create a Git repository for your team/project (`Creating and
   sharing a development repository`_) from the provided template.

#. Read :ref:`using-git`.

#. Read the :ref:`Deliverables` section, and with your team consider
   dependencies between 'tasks' in the deliverables and allocate
   independent tasks to a team member (`Project planning`_).

#. Start implementing your tasks (`Editing and executing Python code`_).

.. tip::

  Start simple and work in small steps. It is much easier to add
  functionality to a working program than to fix a complicated
  non-working program.

.. note::

  When developing your programs, you may need to review the activity
  notebooks from Michaelmas Term.


.. _development_environment:

Development environment
-----------------------

.. note::

   Experienced developers have their preferred tools and development
   environments. If you are experienced with Git, Python and using
   editors, you are free to use your preferred tools.

   The following procedures and tools are suggested.


Software installation
^^^^^^^^^^^^^^^^^^^^^

The following instructions are for installing the necessary tools on
your own computer, and are common for Linux distributions, macOS and
Windows. The tools are already installed on the computers in the DPO.

#. Install Anaconda (https://www.anaconda.com/download/).

   a. Select the Python 3 version for download.

   #. The default install options are recommended.

   #. Select option to install Microsoft Visual Studio Code (VS Code).

#. Install Git following the instructions at https://git-scm.com/.

   .. admonition:: Windows

      When asked which editor to configure select 'nano'.


.. _open_terminal:

Command line terminal
^^^^^^^^^^^^^^^^^^^^^

Some of the following steps require a command line terminal. To open a
command line terminal:

- Linux: Open a 'Terminal' (from DPO use ``Programming`` -> ``Anaconda
  Shell``).
- macOS: Open a 'Terminal'
- Windows: Launch 'Anaconda Prompt'.


Configure Git
^^^^^^^^^^^^^

To configure Git with your name and email address, open a
terminal/command prompt and use the commands:

.. code-block:: bash

   git config --global user.name "John Doe"
   git config --global user.email johndoe@example.com

To configure an editor for use with Git, under macOS and Linux
(including in the DPO under Linux),

.. code-block:: bash

   git config --global core.editor nano

You will need to configure Git on each computer that you use.


Testing your Python installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. note::

   In the DPO, 'Anaconda Navigator' and 'Anaconda Shell' can launched
   from the 'Programming' menu. Use 'Anaconda Shell' rather than a
   regular terminal as it is configured for Anaconda Python.

#. Open the 'Anaconda Navigator' program.

#. From Anaconda Navigator, launch VS Code.

#. Create a new file in VS Code with the extension ``.py`` and enter
   some simple Python code, e.g.::

     print("Testing Python install")

#. Right-click on the file and select `Run Python File in Terminal`. The
   output of your program should appear in a terminal window inside VS
   Code.


.. _creating-and-sharing:

Creating and sharing a development repository
---------------------------------------------

It is strongly recommended that you use the hosted Git service `GitLab
<https://gitlab.com/>`__.

#. Create an account on `GitLab <https://gitlab.com/>`__ and log in.
   Share your username with your team member.

#. *One* team member should create a 'fork' of the starter code
   by going to:

   https://gitlab.com/CUED/partia-flood-warning-system/forks/new

   a. Make your repository private (`Setting -> General -> Permissions -> Project visibility`).

   #. From the overview page (https://gitlab.com/dashboard/) you should
      see your repository. Click on it.

   #. Give your team member access (`Setting -> Members`). Give them
      'Maintainer' access.

      .. attention:: Be sure to make your fork *private*.

#. Check that you can see the repository at
   https://gitlab.com/dashboard/.

#. Fetch a local copy of your repository by *cloning* it. The 'Clone'
   button on the GitLab page for your repository gives the address of
   your Git repository. From a terminal::

     git clone <address of my repository>

   You should now have a local (on your computer) copy of the code.

#. From the terminal, enter the code directory attempt to execute file
   ``Task1A.py``:

   .. code-block:: bash

     python Task1A.py

   (If you are not using Anaconda, on some systems you may need to use
   ``python3 Task1A.py``).

   You should see some output on river level monitoring stations.

.. note::

   The Python code from which you will start uses some modules
   (``requests`` and ``dateutil``) that are not part of the Python
   standard library, but which are distributed as part of Anaconda. If
   you see an error that a module is missing, you can install the module
   using ``pip``. Use:

   .. code-block:: bash

      pip install requests --user
      pip install python-dateutil --user

   Depending on your system, you may need to replace ``pip`` by
   ``pip3``.



Editing and executing Python code
---------------------------------

These instructions are for the `Anaconda <https://www.anaconda.com/>`__
Python environment.

#. From Anaconda Navigator launch 'VS Code' and from VS Code open your
   local code repository directory.

#. Open/create the files you wish to edit. 'Module' files should go in
   the directory ``floodsystem/``. The ``Task*.py`` files should go in
   the root directory of the repository.

#. Use right-click -> 'Run Python File in Terminal' on the program text in VS Code to run
   the Python code.

Python code can be run directly from a terminal. In a directory
containing Python code in a file named ``test.py``, it can be be
executed from the terminal using::

   python test.py

As you develop you programs, commit your changes (using Git) and push
these to your shared online repository. If you are unsure how often to
commit and push changes, err on the side of committing and pushing
frequently. *Commit at least upon the completion of each task.*


.. _continuous-integration:

Automated testing
-----------------

The starter repository at
https://gitlab.com/CUED/partia-flood-warning-system includes the file
``.gitlab-ci.yml`` and which configures automated testing, known as
*continuous integration* (CI), on GitLab. On your GitLab repository page
you will see an icon indicating whether or not the tests are passing.

Edit the ``.gitlab-ci.yml`` file to run your deliverables in the test
system and to add code tests to your test suite.


Project planning
----------------

#. Examine the first few project deliverables, and divide independent
   tasks amongst team members. Each team member can then work on tasks
   independently.

#. Communicate frequently with team members to update them on your
   progress, and seek help from a team member if required.

#. As tasks are completed review each others work and provide feedback.

#. As you progress through the tasks, periodically assess which tasks
   are independent and allocate these to a team member.
