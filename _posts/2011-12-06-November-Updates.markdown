---
layout: post
title: November Fundamentals Updates
categories:
    - Update

---

##Schedule
November updates have been completed with no disruption to services. If a client 
has unexpected behaviour, be sure to have them [clear their cache][Clear Cache].

##Change Log
This month there are 5 specific issues, plus some infrastructure 
changes.

##Infrastructure Changes
We've been working hard to identify how we can improve performance while maintaining
our high standards of security and have made some tweaks to our DNS and web server headers.

You will find content is delivered faster, and if your organisation uses a caching proxy
you will gain even more efficiency as your cache is primed.

###Issue 376 - Merge Fields not correctly escaping dollar symbols ($)
In some cases the use of a dollar symbol ($) followed immediately by two or more 
numeric digits caused the first 2 digits to disappear.

This has been corrected.

###Issue 377 - Link for administrators to visit Q2A
We've added in a quick link at the top of each page for administrators to easily
access our <a href="http://q2a.complispace.net" target="q2a">CompliSpace Questions 
to Answers</a> community driven forum. [learn more](http://complispace.github.com/Article/2011/11/10/Community-Questions-And-Answers.html)

The 'CompliSpace Helpdesk' link also shows users the 5 most recent questions with 
easy access to the provided answer.

<div style="border: 1px dashed ghostwhite; text-align: center; padding: .5em;margin: .5em;">
<strong>Try it now! <a href="http://q2a.complispace.net" target="q2a">CompliSpace Questions to Answers</a></strong>
<a href="http://q2a.complispace.net" target="q2a"><img src="/images/q2a-screenshot.png" alt="Questions to Answers" style="margin-top: 1em"/></a>
</div>


###Issue 387 - Implement BrowserID
CompliSpace Fundamentals now supports the BrowserID single-sign-on protocol! If the
contact e-mail address associated with your sign in username matches you can use
this to easily sign in.

Please not that if your organisation has assigned the same contact e-mail address 
to multiple usernames, then to ensure security, CompliSpace Fundamentals will reject 
the sign in.

This has been tested to work with the following <mark>minimum browser versions</mark>:

* Firefox 3.6
* Google Chrome 12.0
* Safari 4.0
* Internet Explorer 9.0

The [BrowserID] team have several [open tickets](https://github.com/mozilla/browserid/issues/search?q=relay+frame) to support the Opera browser.

[BrowserID] is a very easy way to log into web sites by proving you own an email 
address. [BrowserID] is designed to be tightly integrated into your web browser 
for ease-of-use, and it is designed to be privacy-protecting: the only data 
exchanged is that which is strictly necessary to log in. [BrowserID] is a product 
of [Mozilla] who are working to standardize it so that other browser vendors can, 
if they choose, easily integrate it. In the meantime, [Mozilla] provides a simple 
JavaScript mechanism that lets web sites use [BrowserID] right away, across all 
modern browsers, on desktop and on mobile.

###Issue 386 - CompliFlow Groups Limiting Group Displays
In some cases the CompliFlow Groups editor was truncating the list of groups to
ten. This has been resolved.

[BrowserID]: http://browserid.org/about
[Mozilla]: http://identity.mozilla.com/
[Clear Cache]: http://www.wikihow.com/Clear-Your-Browser's-Cache
