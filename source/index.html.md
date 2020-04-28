---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - http

toc_footers:
  - <a href='https://www.getfeedback.com/about-us' target='_blank'>About Us</a>
  - <a href='https://help.getfeedback.com/' target='_blank'>Support</a>
  - <a href='https://www.getfeedback.com/legal' target='_blank'>Terms of Use</a>
  - <a href='https://www.getfeedback.com/privacy' target='_blank'>Privacy Notice</a>
includes:
  - responses
  - errors

search: true
---

# Overview

The GetFeedback Reporting API is simple, modern, RESTful, and JSON-based. All API access is over HTTPS to the `api.getfeedback.com` domain. Appropriate HTTP verbs are used to manipulate resources.

# Authentication

```http
Authorization: Bearer mF_9.B5f-4.1JqM
```

API bearer tokens should be sent in an HTTP Authorization header. Follow the [RFC 6750 spec section 2.1](http://tools.ietf.org/html/rfc6750).

# Representation

All dates or timestamps are returned and expected as ISO 8601 strings.

The `Accept` HTTP header must always be sent to signify the correct resource representation. At this time only `application/json` is supported.