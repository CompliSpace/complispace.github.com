---
layout: post
title: November Fundamentals Updates
categories:
    - Update

---

##Schedule
November updates are scheduled to take place on Thursday 13th December with no 
disruption to services expected. If a client has unusual behaviour, be sure to 
have them [clear their cache][Clear Cache].

##Change Log
This month there are 11 specific issues.

###Issue-668: Adding photos to the staff directory
A bug has been fixed that stopped the addition of photos to a staff directory entry.

###Issue-664: Complaints Manager
Under some circumstances the complaints manager was not showing all complaints.
This has been fixed.

###Issue-662: Access to Incident Register
In some cases access to the incident register was being denied to general users.
This has been fixed.

###Issue-658: Password Reset Case Sensitivity
The password reset mechanism was overly strict in requiring an exact case match
for the email address. Email addresses are not case sensitive so this has been rectified.

###Issue-652: RSS Feed
A 'custom app' for allowing the embedding of RSS feeds is now available.

###Issue-688: Decouple Database
Improvement on our hosting infrastructure has allowed us to decouple the database.
This is an infrastructural improvement.

###Issue-687: Improved SQL
Improvements to SQL has resulted in some pages that were previously taking several
seconds to render are now rendered in less that half a second.

###Issue-673: Sitemap Updates for Operations
Certain CompliSpace Operations functions on the sitemap have been improved.

###Issue-690: Versioning Note On Printed Pages
A note is now on the top of the first printed page advising that the printed
version is not under version control and to refer to the Fundamentals site for the
most recent version.

###Issue-671: Sitemap Draft Pages
The behavior of the show/hide drafted pages has been modified for use in the sitemap.
Using this button in the sitemap when in edit mode will show/hide drafted pages
in the sitemap itself rather than drafted items on the sitemap page.

###Issue-685: File Updates Being Reported
In some cases changing only a file is not showing up affected pages in the 
publish site report. This has been addressed.


[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
