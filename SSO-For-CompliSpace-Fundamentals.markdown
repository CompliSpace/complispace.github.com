---
layout: default
title: SAML Single Sign On (SSO) Service for CompliSpace Fundamentals
---

##Introduction
Security Assertion Markup Language (SAML) is an XML standard that allows secure web domains to exchange user
authentication and authorisation data. Using SAML, an online service provider can contact a separate online identity
provider to authenticate users who are trying to access secure content.

CompliSpace Fundamentals offers a SAML based Single Sign-On (SSO) service that provides customers with full control over
the authorisation and authentication of hosted user accounts that can access the CompliSpace Fundamentals web-based
application. Using the SAML model, CompliSpace acts as the service provider and provides services such as Fundamentals.
CompliSpace customers act as **identity providers** and control usernames, passwords and other information used to identify,
authenticate and authorise users for web applications that CompliSpace hosts. There are a number of existing [open source](https://developers.google.com/google-apps/help/open-source#sso)
and [commercial](http://www.google.com/enterprise/marketplace/search?categoryId=2&orderBy=rating) identity provider
solutions that can help you implement SSO with CompliSpace Fundamentals.

The CompliSpace SSO service is based on the [SAML v2.0 specifications](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=security#samlv20). SAML v2.0 is supported by several widely known
vendors.

<div class="alert alert-info">
    CompliSpace Technology supports this single sign-on experience as the integration 
    of a SAML 2.0 compliant Identity Provider (IdP) you have already installed and made operational. 
    CompliSpace Technology will do it's best to provide support with the SAML protocol, however 
    your Identity Provider (IdP) is a third-party product and therefore CompliSpace Technology
    does not provide detailed support for the deployment, configuration, troubleshooting, best practices, etc. 
    Issues and questions regarding your Identity Provider (IdP) should be directed to
    your vendor.
</div>


##Understanding SAML based SSO for CompliSpace Fundamentals
The following process explains how a user logs into the CompliSpace Fundamentals application through an organisation's,
SAML based SSO service.

Figure 1, shown below, illustrates the process by which a user logs in to the CompliSpace Fundamentals application
through a SAML based SSO service. The numbered list that follows the image explains each step in more detail.

<div class="alert">
<b>Note:</b> Before this process takes place, the organisation must provide CompliSpace with the <i>metadata XML</i> for their IdP. CompliSpace will also provide the organisation the <i>metadata XML</i> for the Fundamentals SP.
</div>

**Figure 1: Logging in to CompliSpace Fundamentals using SAML**

![SAML Transaction Steps](/images/saml-transaction-steps.png)

This image illustrates the following steps:

1. The user attempts to reach the CompliSpace Fundamentals application.
2. CompliSpace generates a SAML authentication request. The SAML request is encoded and embedded into the URL for the
organisation's SSO service. The RelayState parameter containing the encoded URL of the CompliSpace Fundamentals site
that the user is trying to reach is also embedded in the SSO URL. This RelayState parameter is meant to be an opaque
identifier that is passed back without any modification or inspection.
3. CompliSpace sends a redirect to the user's browser. The redirect URL includes the encoded SAML authentication request
that should be submitted to the organisation's SSO service.
4. The organisation decodes the SAML request and extracts the URL for both CompliSpace's ACS (Assertion Consumer Service)
and the user's destination URL (RelayState parameter). The organisation then authenticates the user. Organisations could
authenticate users by either asking for valid login credentials or by checking for valid session cookies.
5. The organisation generates a SAML response that contains the authenticated user's username and other details.
In accordance with the SAML 2.0 specification, this response is digitally signed with the organisations's public and
private DSA/RSA keys.
6. The organisation encodes the SAML response and the RelayState parameter and returns that information to the user's
browser. The organisation provides a mechanism so that the browser can forward that information to CompliSpace's ACS. For
example, the organisation could embed the SAML response and destination URL in a form and provide a button that the user
can click to submit the form to CompliSpace. The organisation could also include JavaScript on the page that automatically
submits the form to CompliSpace.
7. CompliSpace's ACS verifies the SAML response using the organisation's public key. If the response is successfully
verified, ACS redirects the user to the destination URL.
8. The user has been redirected to the destination URL and is logged in to CompliSpace Fundamentals.

##Required Assertions
CompliSpace Fundamentals requires several claims/assertions that your SAML IdP must provide
in order to work correctly. These can be provided using either the `short name`, `url scheme` or `urn oid`

The claims in the `short name` format include:

* `givenName` - The first name of the user
* `sn` - The surname of the user
* `mail` - The email address used by the user
* `objectGUID` - A unique identifer for the user that is persistent even if the user changes name or email address
* `memberOf` - The list of groups the user belongs in the *Distinguished Name* (DN) format or as a simple string.

For the full list of claim maps in all formats, please see the Google Sheets Document, [SAML Required Attributes](https://docs.google.com/spreadsheets/d/1yMnq7leUjX-iulmQecVv3_HMIHxqGjOOHBNFNDCSi_g/edit?usp=sharing)

##Working with Permissions and Groups
CompliSpace Fundamentals has a rather thorough permissions system, but has been simplified for integration with
SSO. First, if you want a user to have any kind of access to Fundamentals they must belong to a group called `Fundamentals`.
This allows you to temporarily remove access to a user without having to remove and re-add all the detailed permissions.

Fundamentals partitions content into *sections* such as *Public* (available to all staff), *HR Admin* (only available for
your Human Resources staff), etc. Please contact your CRM for details on sections availble to your installation. 
A user with access to a section may have *read only (RO)* or *read/write (RW)* access.

Section access is granted by ensuring the user belongs to a group that is made by taking the `section name` and appending
either `RO` or `RW` as required for the access they require.

For example, if you wish for a user to have read only access to the Public section then they must belong to a group
called `Public RO`. Should the user require read/write access then they must belong to a group called `Public RW`.

All characters in a group must match exactly. For example, the section called `Human Resources (Admin Only)` can be granted
read only access to a user by assigning them to a group called `Human Resources (Admin Only) RO`

###Group Format
The format for the group name can be either a simple string or in the **Distinguished Name (DN)** format. 


With the DN format, only the **CN** RDN component is used. 

Example: `CN=Human Resource (Admin Only) RO,OU=Fundamentals,OU=CompliSpace,OU=Vendors,DC=complispace,DC=net`

