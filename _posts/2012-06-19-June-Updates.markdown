---
layout: post
title: June Fundamentals Updates
categories:
    - Update

---

##Schedule
June updates are scheduled to take place on Thursday 28th June with no 
disruption to services expected. If a client has unusual behaviour, be sure to 
have them [clear their cache][Clear Cache].

##Change Log
This month there are 7 specific issues.

###Issue-475: Locked page message
The message on locked pages is now more useful by describing the reason the page
is locked rather than just saying that it is.

###Issue-479: Normalise internal API
Internally we have improved the usage of certain database calls by standardizing
on a single entry point.

###Issue-489: CSS for logged in/out state
We now have a CSS class for user authentication state. Useful for clients wishing
to change the format or layout of the login page.

###Issue-490: Improved password security check
Passwords can no longer be dictionary words. Please ensure you use adequate complexity
on your passwords. CompliSpace Technology recommends the use of a pass *phrase*.

###Issue-499: Complaints custom app now allows for customised "Third Party Status"
The "Third Party Status" is now taken from the database instead of being hard coded. 
This allows customisation on this field for individual clients.

###Issue-505: JavaScript incompatability with the ancient IE7 browser
An incompatability with the JavaScript code and the ancient Internet Explorer 7 browser
has been addressed.

<div class="alert alert-error">

CompliSpace Technology strongly advises that you should use a modern browser for
all your web browsing. If you <b>must</b> use Internet Explorer, use the most <a rel="nofollow" target="_blank" href="http://windows.microsoft.com/en-au/internet-explorer/downloads/ie">recent version</a>
or install the <a rel="nofollow" target="_blank" href="http://www.google.com/chromeframe/eula.html?prefersystemlevel=true">Google Chrome Frame plugin</a>.

</div>

###Issue-500: Display table type (layout/data) when creating a table
The option for setting a table as being a data table or layout table is now
available when creating a table as well as when editing a table.

[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
