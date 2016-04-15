# OAuth 1.0

## Introduction

Approve one application interacting with another on your behalf without giving away your password.

## Actors
OAuth Love Triangle:
* USER (John)
* CONSUMER (App)
* PROVIDER (Twitter)

## Flow

1. USER Intent

	John wants App to post to his Twitter stream.

2. CONSUMER asks for `Request Token` from PROVIDER

	App asks Twitter for permission and receives `Request Token` and a `Secret`

3. USER is redirected to PROVIDER

	* App redirects John to Twitter

	* Twitter asks John to approve App access

4. USER approved CONSUMER access for PROVIDER

	* John approves App for using Twitter

	* Twitter marks request token as a "good-to-go"

	* Twitter redirects John back to App

5. CONSUMER requests exchange of `Request Token` to `Access Token`

	* App asks Twitter to exchange `Request Token` and `Secret` for an `Access Token`

	* App receives `Access Token`

6. CONSUMER accesses the protected resource at PROVIDER

	* App posts to John's Twitter account by using `Access Token`

## Sources:
* http://oauth.net/core/1.0/
* https://blog.varonis.com/introduction-to-oauth/
