---
layout: post
title: May Fundamentals Updates
categories:
    - Update

---

##Schedule
May updates are scheduled to take place on Thursday 31st May with no 
disruption to services expected. If a client has unusual behaviour, be sure to 
have them [clear their cache][Clear Cache].

##Change Log
This month there are 5 specific issues.

###Issue-468: Non latin character problems
After previous security upgrades, certain non-latin characters were not being rendered.
These characters are now being displayed as expected.

###Issue-465: 'Bungarra' based application not redirecting after authentication
When a user requested a page but was not already authenticated they were not being
redirected back to the original page they requested.

Redirection after authentication on Bungarra based applications are now working.
Notably this improves the usability of CompliFlow when following assigned links in
emails.

###Issue-449: Removal of debug email
One custom application was sending debug data to development. This is no longer the case.

###Issue-467: Table usage warning
Warnings are now displayed when using tables advising that tables should only be
used for displaying tabular data. 

It is also clearer in showing the settings that should be included if a table 
*must* be used for layout purposes only

###Issue-483: Email address normalisation
Email addresses that the Fundamentals system sends from have been normalised. This
will help customers improve their mail system spam filters to allow legitimate
Fundamentals emails.

A further post will be made available shortly listing the valid email addresses


[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
