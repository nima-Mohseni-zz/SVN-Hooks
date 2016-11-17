# SVN-Hooks
This repository will contain a set of sample hooks and files that will integrate Jenkins and Rally after each submit in SVN.
The files will contain two simple .bat files that can be easily transferred to a Linux bash. The pre commit section would contain 
a configuration file that will hold functions and basic data and a logic file. The post commit will contain the same files plus an additional file for Jenkins update. The pre commit hook will enforce a log message format as follows:
Tickets ... : summary
Then we will check the Rally to see if such tickets exist and they are eligible for submission. the post commit file would set up a change set based on the commit and send to rally for update and then update Jenkins based on the commit and if there is a build configured it will trigger that. We need poll SCM in Jenkins to be ticked but a time is not necessary. the Rally work space needs to have change set available as well.

