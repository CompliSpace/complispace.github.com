---
layout: default
title: CompliSpace Fundamentals Referred Sign In
---

##Introduction
For better integration into existing client sites, CompliSpace is currently investigating simplified methods for signing in to Fundamentals sites.

This is accomplished by allowing an organisation's internal sites to generate signed links that signify to Fundamentals that the user is already trusted by the referring site.

It is expected that this functionality will be rolled out to all Fundamentals customers in the near future. If you are interested in this feature and would like a pre-trial, please contact <development@complispace.net>.

A helper class written in [PHP](http://www.php.net) is available on [GitHub](https://github.com/CompliSpace) as [GIST 907000](https://gist.github.com/907000).

##Proposed Prototype Implementation
The prototype currently in use consists of appending several `GET` request parameters that are signed by a secret key.



To use the referred login mechanism for CompliSpace Fundamentals, simply link to the regular page you want people to view (eg, <http://xyz.complispace.com.au/HRAdministrationManagersOnly>) and append the following `GET` parameters:

<pre class="note"><code>referredUserLogin=&lt;login username&gt;
referredExpires=&lt;unix epoch timestamp, must be no greater than 6 hours in the future&gt;
referredAccessKeyId=&lt;your sites key id&gt;
referredSignature=&lt;base 64 encoded calculated signature of the request&gt;
</code></pre>


The `referredSignature` is calculated with the following pseudo-code:  
<pre class="note"><code>$stringToSign = (sting)$referedUserLogin+":"+(string)$referredExpires+":"+(string)$secretAccessKey;
$referredSignature = base64_encode(hash_hmac("sha256", $stringToSign, $secretAccessKey));
</code></pre>

Note that for this implementation the output of the `hash_hmac()` function is expected to be a lowercase string of hex digits ([see the hash_hmac() PHP function](http://au2.php.net/hash_hmac)).

Example (pseudo code):

<pre class="note"><code>referredUserLogin=bob (the user who is accessing the site)
referredExpires=1320969600  (11am, 11th November 2011 - <a href="http://www.awm.gov.au/commemoration/remembrance/">rememberance day</a>)
referredAccessKeyId=mySiteId (the key that identifies the signer)
secretAccessKey=connie (the secret, unshared key used to sign the request)
</code></pre>

<p></p>

1. Calculate the string to sign:  
  `$stringToSign = "bob:1320969600:mySiteId";`
2. Create the signature:  
  `$signature = hash_hmac("sha256", "bob:1320969600:mySiteId", "connie");`  
   The result will be `7435b9129f07a93f790875f061c9396b27cf5d6bb5be8cf7b37afacd11dd00ca`
3. Base64 encode the signature:  
  `$signature = base64_encode($signature);`  
   The result will be `NzQzNWI5MTI5ZjA3YTkzZjc5MDg3NWYwNjFjOTM5NmIyN2NmNWQ2YmI1YmU4Y2Y3YjM3YWZhY2QxMWRkMDBjYQ==`
4. Build the url:  
  <pre class="note"><code>$url = sprintf("http://xyz.complispace.com.au/Home?referredUserLogin=%s&referredExpires=%s&referredAccessKeyId=%s&referredSignature=%s", $referredUserLogin, $referredExpires, $referredAccessKeyId, $signature);</code></pre>

<p></p>
This will result in the final URL:  

<pre class="note"><code>http://xyz.complispace.com.au/Home?referredUserLogin=bob&referredExpires=1320969600&referredAccessKeyId=connie&referredSignature=NzQzNWI5MTI5ZjA3YTkzZjc5MDg3NWYwNjFjOTM5NmIyN2NmNWQ2YmI1YmU4Y2Y3YjM3YWZhY2QxMWRkMDBjYQ==
</code></pre>

If you have any questions or feedback, please contact <development@complispace.net>
