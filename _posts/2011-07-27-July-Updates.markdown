---
layout: default
title: July Fundamentals Updates
---

##Schedule
July updates will commence from Wednesday 28th July and conclude 
Monday 1st August. There will be no disruption to services. If a client 
has unexpected behaviour, be sure to have them [clear their cache][Clear Cache].

##Change Log
This month there are 4 specific issues that will be rolled out. 

###Feature 178 - Addition of a Markdown content type
A Markdown content type has been added for advanced users. If you would like this
feature enabled for your site please contact your sales representative. More
information on markdown can be found at [Daring Fireball][Markdown]. This 
CompliSpace implementation uses [Markdown Extra][].

###Issue 282 - Intermitent problems with CompliFlow submission to special group or group member 'Self'
Under some circumstances submissions to 'Self' were failing. This has been addressed.

###Issue 296 - HTML entity translation of '&' character failing
Under some circumstances the underlying CMS was not correctly translating the 
ampersand (&) character to correct HTML encoding (`&amp;`). This has been addressed.

###Issue 305 - Carriage Returns/New Lines not being escaped in CompliFlow Builder
Some Windows based CR/LF characters were not being escaped. This has been addressed.


[basic authentication]: http://www.freesoft.org/CIE/RFC/1945/67.htm
[Markdown]: http://daringfireball.net/projects/markdown/
[Markdown Extra]: http://michelf.com/projects/php-markdown/extra/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache

*[CSV]: Comma Separated Values
