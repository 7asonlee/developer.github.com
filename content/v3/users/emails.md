---
title: User Emails API v3 | developer.github.com
---

# User Emails API

Mangement of email addresses via the API requires that you are
authenticated.

## Get email addresses

    GET /user/emails

### Response

<%= headers 200 %>
<%= json ["octocat@github.com", "support@github.com"] %>

## Add email address(es)

    POST /user/emails

### Input

You can post a single email address or an array of addresses:

<%= json ["octocat@github.com", "support@github.com"] %>

### Response

<%= headers 201 %>
<%= json ["octocat@github.com", "support@github.com"] %>

## Delete email address(es)

    DELETE /user/emails

### Input

You can include a single email address or an array of addresses:

<%= json ["octocat@github.com", "support@github.com"] %>

### Response

<%= headers 204, :no_response => true %>
