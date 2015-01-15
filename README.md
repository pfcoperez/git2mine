# git2mine
A python application aimed to make easier the tedious task of logging time for Redmine tasks by extracting information from GIT commits comments.

## Purpose

My experience so far, working as software developer for different companies indicates that:

For most of the project management approaches, the developer must report how much time he or she took to fix a bug, implement a change or a new functionality.
Being, on the other hand, version control systems a practical need for code management implies spending some time writing change descriptions and using them as messages for each code commit/version/...

Thus, SW developers trend to write at least two descriptions for each task we complete:

  1. A *commit* message.
  2. A time log entry for the project management system.
  
Personally, I found myself writing essentially the same text for (1) and (2) and that's the reason I decided to write a little script aimed to mine the messages registered at the VCS (1) and use them as time reports for the issue tracker (2).
Being [GIT] and [Redmine] the VCS and project management tool I interact with at work I wrote my script for working with them.

## How does it work?

First, once the application has been installed in your system using PyPi's **pip**, you can start it by invoking 

    mineCommits

Obviously, the application won't be creative concerning your spent time and issue id, its user must add some suggar to her/his commit messages. This is the format currently recognized expressed as a (roughly simplified) regular expression:

    [CI|NF|BUG|INT] <\d+(h|m)> \d+ : .+

The actual re accepts from 0 to n spaces between each expression's element.

Some use examples:

- [NF] <2h> 1898: Implemented inversion counting algortithm
- [BUG]   <15m>         9000: Changed label translation in the main window...
- [CI] <8h> 8258: Improved core engine performance, now the solution calculation is calculated within 24h
- [INT] <1m> : Added *.so to .gitignore

NF, BUG, CI and INT stand for:

- **BUG**: A bug fix.
- **CI**: Change Improvement.
- **INT**: Some internal task or change unnoticeable by the user.
- **NF**: New functionality.

## Known issues (Hopefully to be  fixed soon)

- The connection parammeters to the Redmine server has been always tested providing the user REST key you can get at **http://YOUR_REDMINE_URL/my/account**. It doesn't seem to work with user/password identification.
- After clicking at "Check, apply and load Activities" button, the application GUI hangs until the connection has been *established*


[GIT]:http://git-scm.com/
[Redmine]:http://www.redmine.org/



