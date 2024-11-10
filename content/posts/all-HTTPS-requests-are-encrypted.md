---
title: all HTTPS requests are encrypted
categories:
  - cybersecurity
date: 2024-09-12T18:30:00.000Z
---

this fact is obvious to anyone with the least bit of background in cybersecurity, but that category excludes everyone else, so:

all HTTPS requests (not plain HTTP) are encrypted end-to-end. of course, this is not the holy grail of safety, because "end-to-end" doesn't guarantee what the ends are. these encryptions are unbreakable by all conventional means, although there are workarounds (which are either pathologically hard or involve downgrading to HTTP).

realistically, this means a few things. firstly, sending secrets in HTTP headers or query parameters is secure. of course, this doesn't look secure, because you can see them on the URL, right there. but all query parameters are encrypted on transit. POST requests are not inherently more secure than GET. encrypting your secrets in transit doesn't do anything. if the encrypted secret is decrypted on reception, then it's the same as passing an unencrypted secret. there are fancier encryption schemes involving nonces and certificates, but at that point you're re-implementing TLS in your app for no good reason.

on the flipside, this means that having proper TLS certificates is very very very (3 veries) important. all of the protections given to you by HTTPS don't mean anything if your website's certificate is self-signed, or if it isn't signed at all. chances are there's some person who's responsible for making sure that the certificate is applicable everywhere and up to date, and chances are you never have to think about that person. but if your browser or http request library ever throws an error while parsing the server certificate, please don't ignore it (you shouldn't ignore errors in general, but that's a longer topic)
