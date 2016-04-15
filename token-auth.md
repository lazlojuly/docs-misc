# Token Authentication

## Introduction

Token Authentication, also called ‘Bearer Token Authentication’.
Can be used for communicating with REST APIs where every request needs to be authenticated.
Specifically useful with Single Page Applications (SPAs) where client sends
credentials in an AJAX request and then uses the received token to make subsequent API calls.

## Actors
* CLIENT (Browser/UI)
* SERVER (REST API)

## Flow

1. CLIENT submits credentials to SERVER for authentication

	* UI collects credentials and sends them to REST API with an AJAX request for authentication

	* REST API checks received credentials

2. SERVER returns a `Bearer Token` in the AJAX response

	* UI stores `Bearer Token`
	
3. CLIENT uses `Bearer Token` over HTTPS on every subsequent requests (in cookie or in Authorization header)

## Sources:
* https://docs.stormpath.com/java/servlet-plugin/http-request-authentication.html#token-authentication
