# Introduction

Approve one application interacting with another on your behalf without giving away your password.

# Actors
OAuth Love Triangle:
* USER (Joe)
* CONSUMER (App)
* PROVIDER (Twitter)

# Flow

1. USER Intent

	Joe wants App to post to his Twitter stream.

2. CONSUMER asks for `Request Token` from PROVIDER

	App asks Twitter for permission and receives `Request Token` and a `Secret`

3. USER is redirected to PROVIDER

	* App redirects Joe to Twitter

	* Twitter asks Joe to approve App access

4. USER approved CONSUMER access for PROVIDER

	* Joe approves App for using Twitter

	* Twitter marks request token as a "good-to-go"

	* Twitter redirects Joe back to App

5. CONSUMER requests exchange of `Request Token` to `Access Token`

	* App asks Twitter to exchange `Request Token` and `Secret` for an `Access Token`

	* App receives `Access Token`

6. CONSUMER accesses the protected resource at PROVIDER

	* App posts to Joe's Twitter account by using `Access Token`

# Sources:
* http://oauth.net/core/1.0/
* https://blog.varonis.com/introduction-to-oauth/
