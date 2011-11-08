---
layout: default
title: September Maintenance
categories:
    - Update

---

##Schedule
Server maintenance will begin at 19:00 GMT+10. During this time client sites will
be locked. It is expected that the server maintenance will last around 6 hours.

There are also infrastructure upgrades where we will be updating our DNS records.
Depending on client locally configured DNS server caching options these effects
may take anywhere from as little as 6 hours to 48 hours to propagate. If you require,
contact your local systems administrator and ask them to clear your organisation's 
DNS cache to help decrease the propagation time.

###Maintenance Details
The scheduled maintenance will provide our customers a more responsive system, and
improved security.

This maintenance will also provide a greater capacity to expand the CompliSpace 
services and software while providing an easier system to manage and maintain.

##Change Log
This month there are 11 specific issues that will be rolled out. 

###Issue #265 - Refactor to external library use
The code has been refactored to common libraries that have been extracted to a single
location in the application stack instead of being duplicated across all sites.
This will lead to more efficient upgrades.

###Issue #320 - Update [deprecated function calls](http://en.wikipedia.org/wiki/Deprecation)
Upgrade to our underlying application stack. For best impedance we have made 
updates to the core Komodo CMS that removes and replaces deprecated function 
calls ensuring full compatability with the most recent application stack. This 
will also provide ease of portability with future advances in the application 
stack and the CompliSpace Fundamentals program.

###Issue #321 - Refactor for partial use of the CompliSpace Ghatanothoa library
CompliSpace Technology has written an [ORM](http://en.wikipedia.org/wiki/Object-Relational_Mapping)
 library to abstract the Komodo CMS database. CompliSpace specific extensions can 
use this library easily while providing easy forward porting in future development.

###Issue #322 - Upgrade ID3 library to 1.9.0
This library is responsible for detecting file types and extracting meta-data in
the file library. CompliSpace Technology has replaced the v1.7.5 (25th December 2005) 
used by Komodo CMS with this more recent v1.9.0 (20 June 2011).

###Issue #325 - Refactor request data variable usage in CGI scripts
Variable usage has been refactored to provide greater efficiency and security.

###Issue #332 - Invalid Page Image Report was reporting false positives
This report used internally by the CompliSpace Operations Team was delivering
false positives. This has been addressed reducing the workload for our Operations Team.

###Issue #329, #330 #331 - Consolidation of link consistency reports
Individual reports for broken internal links, broken external links and broken
download links were being generated for each site and sent to the Operations Team.
These reports have been merged into a single report for each site with a much better
layout to assist the Operation Team to more efficiently monitor client site consistency.

###Issue #339 - Rebuild assessment reports
The assessment report has been rebuilt from the ground up and provides a better
format for monitoring completed and outstanding assessments. The report now consists 
of two parts showing outstanding assessments and those completed since the last report.
Each section is broken down to show the user and the tests outstanding or completed
along with relevant assignment and completed dates.

###Issue #338 - Rebuilt backup scripts
Backup scripts have been completely re-written and are batched with system load level
monitoring. Now each site is batched to run individually and will run in parallel, only spawning 
new backup tasks when the system load is below ~31.25%. Additionally each task has 
a positive ['nice' level](http://en.wikipedia.org/wiki/Nice_level) ensuring 
backups do not over consume processing resources.

The previous method simply ran a single script that iterated over each site sequentially
backing up one after the other. While this was run at around 2am each morning when nobody was
using any sites, it consumed a lot of resources and would not sustain future growth.

[Markdown]: http://daringfireball.net/projects/markdown/
[Markdown Extra]: http://michelf.com/projects/php-markdown/extra/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache

[Bullet Proof]: http://www.bulletproof.net.au/

*[Refactor]: By continuously improving the design of code, we make it easier and easier to work with. This is in sharp contrast to what typically happens: little refactoring and a great deal of attention paid to expediently adding new features. If you get into the hygienic habit of refactoring continuously, you'll find that it is easier to extend and maintain code.
*[refactor]: By continuously improving the design of code, we make it easier and easier to work with. This is in sharp contrast to what typically happens: little refactoring and a great deal of attention paid to expediently adding new features. If you get into the hygienic habit of refactoring continuously, you'll find that it is easier to extend and maintain code.
