---
layout: post
title: March Fundamentals Updates
categories:
    - Update

---

##Schedule
March rollouts will commence from Tuesday 22nd March and conclude 
Thursday 24th March. There will be no disruption to services. If a client 
has unexpected behaviour, be sure to have them [clear their cache][Clear Cache].

##Change Log
This month there are 5 specific issues that will be rolled out.

***Update: Issue 209 added to this release. Please see the [March
   Fundamentals Updates -
   Addendum](/2011/03/14/March-Updates-Addendum.html) post for more
   information. This will make 6 issues in this update.***

###Issue 186 - Form Builder Submission Data Working As Expected
Under some conditions form builder submissions were not saving to
the database. This has been addressed.

###Issue 187 - CompliFlow Date Fields Empty In Form Preview
Date fields were appearing empty in CompliFlow preview. This was by
design as the preview shows what a form looks like once it is complete. 
Fields display a default value if one is present or empty when none has
been supplied. As this was causing confusion with some people, empty date fields
now show a place holder when in preview mode.

###Issue 193 - Implement Basic Authentication (RFC 1945, 11.1)
If you wish to develop applications that interact directly with CompliSpace
Fundamentals, sending the [RFC 1945 standard Authentication (basic) headers][basic authentication] 
with a valid username and password will authenticate correctly.

This is an initial step in providing further integration into an organisation's 
already existing authentication infrastructure.

###Issue 194 - Add Markdown As Standard Multipart For Plain Text Emails
All email sent through the CompliSpace Fundamentals system that are usually plain text
will now be sent in multi-part format. The basic part will still contain the plain text,
however the extended part will use [Markdown] to convert the plain text to a nice HTML format.
CompliSpace Fundamentals uses [Markdown Extra].

CompliSpace Development is also experimenting with a Markdown *content item*. 
If this is something you would be interested in trying out (Beta stage), 
please contact <development@complispace.net>

###Issue 200 - Add Export For Complaints Register
The complaints manager now has a button labelled 'Export All Complaints'. This will
download a CSV file for all the complaints in the register. CSV files can be opened
 in your favourite spread sheet program or processed by your own programs.

[basic authentication]: http://www.freesoft.org/CIE/RFC/1945/67.htm
[Markdown]: http://daringfireball.net/projects/markdown/
[Markdown Extra]: http://michelf.com/projects/php-markdown/extra/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache

*[CSV]: Comma Separated Values
