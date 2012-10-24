---
layout: post
title: October Fundamentals Updates
categories:
    - Update

---

##Schedule
October updates are scheduled to take place on Thursday 25th October with no 
disruption to services expected. If a client has unusual behaviour, be sure to 
have them [clear their cache][Clear Cache].

##Change Log
This month there are 9 specific issues.

###Issue-583: Updates to internal SQL
Some updates to how data is handled

###Issue-572: Updated the 'custom apps' to use `GET` instead of `POST`
This means that when you use any of the custom applications (such as injury register)
to view an item the link to that specific item can be kept and possible emailed
(you will need to be logged in to view it of course)

###Issue-571: Correct custom app redirection after logging in
When receiving and email that links to an item in a custom app, you will now
be redirected to the right page after logging in.

###Issue-559: Disabled BrowserID for older browsers
To avoid confusion we now disable the Browser ID login for users with older browsers.
If you have an older browser we will display a message explaining why this option
is not available.

###Issue-576: Add ID to CompliFlow lists and forms
The internally generated ID that is unique to each CompliFlow form is now displayed
for your reference.

###Issue-560: CompliFlow Export
Under certain circumstances some CompliFlow reports were not exporting. This has
been fixed.

###Issue-636: Search button not working
Under certain conditions the search button was not working. This has been fixed.

###Issue-634: Breadcrumbs not working
Under certain conditions the bread crumb navigation was not displaying on custom
applications. This has now been fixed.

###Issue-629: Login panel redirect
The correct behaviour for login panels is to redirect a logged in user back to
the home page. This was occurring even in edit mode which was confusing. The redirect
feature will now not work in edit mode.


[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
