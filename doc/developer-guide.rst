CMItemplate developer guide
===========================

Here are a few simple guidelines to please be obeyed when working on CMIdiffract

* Document your code!

  * Use spinx-compatible docstrings to document all classs, methods, functions, etc.

* Write code that is compatible with the latest stable Python 3.x version.
* Make use of NumPy as much as possible.


Source code formatting
----------------------

* CMI Python projects use the 4-spaces standard for indentation of blocks.
* Do not use tabs, always expand to spaces.
* Try to not extend lines beyond 100 characters
* Keep the utf-8 coding directive in the first line
* Keep the Emacs local variables section at the end of all files, and try to stick to the directives
  (manually) when not using Emacs.


Version control (git) details
-----------------------------

* CMItemplate uses git as a version control system with a central repositories on github_.

  * CMItemplate uses the git-flow branching model

    * the principal development branch is ``develop``
    * all new developments should be done on a ``feature/`` branch and, once ready, be branched into
      ``develop``

  * Never touch the branch ``master`` -- this is to be done by the maintainers.

    * the ``master`` branch is only for releases. There should never be any development done on
      ``master``, nor any release preparations. The latter is done on ``release/``, then the release
      is put onto ``master``, and possibly necessary fixes are done on ``hotfix/``.

  * Do not repeatedly branch feature branches into ``develop`` instead merge ``develop`` into your
    ``feature/`` branch.

  * General documentation work should always be made on ``develop`` (only)!

    * commit such doc-only updates as separate commits!
    * one can then merge these doc-only commits into ``feature/`` branches

  * **Never implement a change twice** manually. Implement it on the most appropriate branch, then
    merge it into whatever branch you want to have it.




Descriptions of source code files
---------------------------------

Here one would provide a short introduction into the different code files, their intended content,
and their interplay.


  .. _github: https://github.com/CFEL-CMI/CMI-Python-project-template


.. comment
   Local Variables:
   coding: utf-8
   fill-column: 100
   truncate-lines: t
   End:
