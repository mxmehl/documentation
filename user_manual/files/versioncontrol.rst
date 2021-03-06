Version Control
===============

ownCloud supports simple version control for files. Versioning is
enabled by default, and creates backups of files which are accessible
via the history tab. This tab also links to the history page, where you
can roll back a file to any previous version. Changes made at intervals
greater than two minutes are saved in data/[user]/versions, and made
accessible using the above pages.


The versioning app expires old versions automatically to make sure that
the user doesn't run out of space. Following pattern is used to delete
old versions:

* For the first 10 seconds ownCloud keeps one version every 2 seconds
* For the first hour ownCloud keeps one version every minute
* For the first 24 hours ownCloud keeps one version every hour
* For the first 30 days ownCloud keeps one version every day
* After the first 30 days ownCloud keeps one version every week

The versions are adjusted along this pattern every time a new version gets
created.

Beside that the version app takes care to never use more that 50% of the users
currently available free space. If the stored versions exceed this limit ownCloud
delete the oldest versions until it meets the memory usage limit again.
