# git2mine
A python application aimed to make easier the tedious task of logging time for Redmine tasks by extracting information from GIT commits comments.

## Purpose

My experience so far, working as software developer for different comapnies indicates that:

For most of the project management approaches, the developer must report how much time he or she took to fix a bug, implement a change or a new functionality.
Being, on the other hand, version control systems a practial need for code management implies spending some time writing change descriptions and using them as messages for each code commit/version/...

Thus, SW developers trend to write at least two descriptions for each task we complete:

  1. A *commit* message.
  2. A time log entry for the project management system.
  
Personally, I found myself writing essentially the same text for (1) and (2) and that's the reason I decided to write a little script aimed to mine the messages registered at the VCS (1) and use them as time reports for the issue tracker (2).
Being [GIT] and [Redmine] the VCS and project management tool I interact with at work I wrote my script for working with them.



[GIT]:http://git-scm.com/
[Redmine]:http://www.redmine.org/


