---
layout: default
title: February Fundamentals Updates
---

##Schedule
February rollouts will commence from Tuesday 22nd February and conclude 
Thursday 24th February. There will be no disruption to services. If a client 
has unexpected behaviour, be sure to have them clear their cache.

##Change Log
This month there are 7 specific issues that will be rolled out, 
many of which will have no visible impact on customers:

###Issue #147 - Printable CSS for new skins
This has already been rolled out as a patch but is included in this release for
 consistency. When pages are printed the web browser artifacts are removed: 
 only the breadcrumb bar and main content will be printed. There is no header, 
 footer or side navigation bar on printed pages. For page title and page url, 
 these are options when printing and depends on the end users browser 
 and operating system.

###Issue #170 - Complaints search dates were broken
The date field in the complaints search was completely broken. Obviously this 
custom app isn't being used much since this was found as part of investigating
 Issue #135.

###Issue #169 - Update hard coded email addresses from @komodocms.com emails to appropriate @complispace.com
There were numerous hard coded email addresses throughout the core Komodo CMS
 code sending of various error reporting information to Komosion. This has now
  been altered to send to the appropriate development email addresses.

###Issue #167 - Update hard coded email addresses from support@compli.com.au to helpdesk@complispace.com
Various places in the custom application had hard coded emails being sent to a 
deprecated ComlpiSpace domain. This is now being sent to helpdesk@complispace.com.

###Issue #151 - Corrupt or password protected PDF files can't be indexed during publishing
This has applied to corrupted PDF files in the past, but there has been an
increase in clients using password protected PDF's or documents that contain
security plugins and hence non-standard PDF files. This was breaking during
publishing as the Komodo CMS could not extract the text for indexing. 
This has now been changed to fail silently. Pages will now publish, 
however the content of the PDF files will not be searchable.

###Issue #144 - 'Hiding' Subscribed to Mailing List in all sites
The user details screen available to administrators 
(Komodo Bar->User->Search->[find user]->Details) had a field for subscribing
to the mailing list. This is something used by Komosion on their own hosted
websites. This data was stored in the database but not accessible by
Komosion. It is not used by CompliSpace so it is now hidden to avoid
confusion. The code is still there in case we want it for future use.

###Issue #165 - Implement prompt for Chrome Frame
To enhance compatibility, end users with internet explorer that do not already
have Google Chrome Frame plugin installed will be prompted to install GCF.
A small bar appears above the site advising them to install the plugin. 
It includes links/buttons to install the plugin, more information
(link to a [Google YouTube](http://www.youtube.com/watch?v=sjW0Bchdj-w) video explaining what it is) and a cancel button 
that hides the information bar. The information bar will appear again in the
next browser session if they have not already installed GCF.

*Big thanks to Tracy and Ellen for their feedback on this issue!*
￼
![Google Chrome Frame Installer Preview][gcf-preview]

*[GCF]: Google Chrome Frame
*[PDF]: Portable Document Format

[gcf-preview]: /images/gcf-preview.png