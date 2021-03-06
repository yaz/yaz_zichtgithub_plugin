=========
Changelog
=========

All notable changes to this project will be documented in this file.

The format is based on `Keep a Changelog <http://keepachangelog.com/>`_
and this project adheres to `Semantic Versioning <http://semver.org/>`_.

[Unreleased]
------------

0.5.12
------

- Archived repositories will now be marked 'Obsolete' automatically
  on the repository list

0.5.11
------

- Fixed the version distance hash, adding the 'g' character indicating a git hash
- Changed the way that the deployed versions are computed, it will now only process
  repos that are in the google sheet.  Also, it will no longer try to find the
  version if it is further away than 9 hops.  This helps the performance considerably.

0.5.10
------

- Fixed: Will now match deployment tags only based on the `-env` postfix

0.5.9
-----

- Fixed: Added missing binary file to setup.py

0.5.8
-----

- Added: yaz deployed version

0.5.7
-----

- Fixed: trying to persist zero cells is now properly ignored

0.5.6
-----

- Fixed: multiple retries are performed with progressively longer delays
- Changed: the repos will now be processed in random order

0.5.5
-----

- Fixed: changed `cells.length` into `len(cells)`.  This is not typescript :p

0.5.4
-----

- Changed: increase throttle delay to 35 seconds

0.5.3
-----

- Added: throttle checks, i.e. when a read or write action fails,
  a 5 second delay is imposed and we try again.  This retry can only
  occur once

0.5.2
-----

- Fixed: the shebang of the scipts no longer use /usr/bin/env.  This
  prevents the pip installer from expanding the path when the python
  wheel is generated

0.5.1
-----

- Fixed: the entry-points scripts are now properly exported and
  installed

0.5.0
-----

- Added: yaz plugin to scan the repository and update a google sheet
  with separated by repo type
- Changed: the file structure to be more maintainable

0.4.0
-----

- Added: new task to scan the repository and summarize it

0.3.0
-----

- Added: new task update-repo
- Changed: renamed update-spreadsheet to update-all

0.2.1
-----

- Changed: references to yaz/yaz_zichtgithub_plugin because the
  repository changed owner

0.2.0
-----

- Added: a tool to perform regexp search on repo files

0.1.0
-----

- Added: support for multiple worksheets
- Added: only use columns and rows marked with 'any'

0.0.2
-----

- Working importer.  Running from Jenkins daily.
