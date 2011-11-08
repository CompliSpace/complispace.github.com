---
layout: default
title: April Fundamentals Updates
categories:
    - Update

---

##Schedule
April updates will commence from Tuesday 2nd May and conclude 
Thursday 6th May. There will be no disruption to services. If a client 
has unexpected behaviour, be sure to have them [clear their cache][Clear Cache].

##Change Log
This month there are 5 specific issues that will be rolled out. 

Issue #220 provides significant benefits for clients who have other 
internal systems that they would like to seamlessly link to CompliSpace 
Fundamentals.


###Issue 210 - Under certain conditions an error occurs when uploading a file
After clients have requested or required database rollbacks some sites were not 
able to upload new files. This has been addressed.

###Issue 214 - Implement 401 and 403 response headers
Combined with Issue #220, this allows client developed software or integrators 
to rely on correct header responses when access restricted content.

###Issue 229 - Scheduled emails not being delivered
Under some circumstances scheduled system generated emails were not being sent
correctly. This has now been corrected.

###Issue 234 - Assessment module not handling certain characters
The Assessment Module was not encoding certain characters correctly. This has
now been corrected.

###Issue 220 - Infrastructure to support federated login 
CompliSpace Fundamentals now has the ability to integrate into a private system
by using signed referrer links. This is a major milestone in providing better
integration with existing systems.

Full technical details are available on the [Referred Sign In](ReferredSignIn.html) 
page that includes links to sample code and an algorithm for generating signed
referrer requests.

[basic authentication]: http://www.freesoft.org/CIE/RFC/1945/67.htm
[Markdown]: http://daringfireball.net/projects/markdown/
[Markdown Extra]: http://michelf.com/projects/php-markdown/extra/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache

*[CSV]: Comma Separated Values
