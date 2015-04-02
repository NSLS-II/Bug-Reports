Bug Reports
===========

Unified issue-tracker for bugs in the data acqusition, management, and analasys software at NSLS-II

How to write a good bug report
------------------------------

Reporting bugs is cirtical to software delevopment (we can't fix bugs we don't know exists) but
it is important to write *good* bug reports.  For bugs to be as useful as possible they need to be

- short :: Most bugs can be produced in a few lines of code.  Making the code short helps to convince 
  the developers the bug is in *their* code not *your* code
- self contained :: Include everything needed to replcate the bug
- correct :: should be able to copy-paste-run the code and see the bug
 
There are expaned at http://sscce.org/.

Useful tools
------------

It is also important to document what version of all of the dependancy.

At the python shell you can run ::
   
  dataportal.watermark()
   
which will print out the version of the python stack.  If you run ::

  conda list
  
In your activated enviroment to list all of the installed conda packages.  Both of these 
outputs are very helpful for debugging your problem.
