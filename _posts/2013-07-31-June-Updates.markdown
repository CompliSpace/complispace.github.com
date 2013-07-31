---
layout: post
title: June Fundamentals Updates
categories:
    - Update

---

##Introduction
June updates, if a client has unusual behaviour, be sure to 
have them [clear their cache][Clear Cache].


##Change Log
This month there are 16 specific issues.

###Issue-863: Reduce HTTP Requests
Client side code has been refactored to reduce the number and size of HTTP requests.
This means a faster loading experience.

###Issue-861: Excel Template Documents
Microsoft Excel Template Documents are supported.

###Issue-859: Fixed the Confusion Around the User 'Active' Status
There were two kinds of 'active' status for users, the functionality has been merged into
a single state.

###Issue-858: Hazard Register Terminology
Terminology has been standardised.

###Issue-852: Navigation Buttons Not Showing
In some instances navigation buttons were not showing correctly. This has been resolved

###Issue-840: Unable to Assign CompliFlow Forms on Mobile Devices
Now works as expected on mobile devices.

###Issue-838: Tables Not Pasting Correctly
In some circumstances tables were not pasting correctly. This has been resolved.

Please note: CompliSpace Technology discourages the use of tables. If you use them
your content will not display correctly on mobile devices.

###Issue-832: Archive Page Interface
The interface to the archive pages has been improved.

###Issue-817: Default File Library Section
The default section for the file library is now 'Public'. Note that 'Public' means
available to all your users. The section 'Global' means available to all users on the Internet.
You can now enter an incident up to five years old.

###Issue-815: File Library 'Fake Path' Fixed
For security, modern browsers in windows often replace the path on your hard drive
with 'c:\fakepath'. We now detect this and try to make the path easier to read.
General internal code improvements

###Issue-804: Merge Field Usage
Information about merge field usage is now available.

###Issue-781: Removal of Spell Check Tool
Modern browsers now support spell checking in input fields and reference your local
language and dictionary settings. This is now used in favour of the outdated Komodo spell check library.


###Issue-775: Improved Functionality in CompliFlow for Forms Assigned to Deleted Users
Improved Functionality in CompliFlow for Forms Assigned to Deleted Users.

###Issue-699: Unable to Edit Tables
In some circumstances tables could not be edited. This has been resolved.

Please note: CompliSpace Technology discourages the use of tables. If you use them
your content will not display correctly on mobile devices.


[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
