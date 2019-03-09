# ElasticIdentityServer4
This tutorial shows the way to connect the Elastic stack (Elastic Search and Kibana) to your IdentityServer4 solution to make the users login to the Kibana by IdentityServer4

## Introduction
In some cases, software teams need to make an integration between Elastic and IdentityServer to let their users login throught the IdentityServer to the Elastic stack. This tutorial shows the way to shape such an integration.

## IdentityServer4 preparation
In order to make it easier to add news clients, scopes, etc., the [IdentityServer4 admin panel](https://github.com/skoruba/IdentityServer4.Admin) is recomended. When running the project, you need to define a new client, with the id of `elastic-mvc` and the name of `ElasticSearch`, for instance, as shown below:

![Screenshot](01-ClientCreation.PNG)

For the nest step, add the `profile`, `openid` and `roles` as he allowed scopes. Then add the `http://localhost:5601/auth/openid/login` and `http://localhost:5601` URLs as the Redirect Uris. The allowed grnt type must be set to `authorization_code`.
