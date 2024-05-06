# Monthly playground hacking 2024/05/07

## Prerequisites
* [Source code](https://github.com/barney71/oauth2-proxy-example)
* [Git](https://git-scm.com/downloads)
* Docker
* Docker Compose
* Okta Developer Edition Service [Account](https://developer.okta.com/signup/)
* REST client
  * [Insomnia](https://insomnia.rest/download)
  * [Postman](https://www.postman.com/downloads/)

## Sources of information
* [OAuth2 Proxy Configuration](https://oauth2-proxy.github.io/oauth2-proxy/configuration/overview)
* [OAuth2 Proxy Endpoints](https://oauth2-proxy.github.io/oauth2-proxy/features/endpoints/)
* [Okta developer documentation](https://developer.okta.com/)

## First task 
Clone the source code to your local machine. Then set up your Okta account. Create an application (Web Application) and two users to be used with the oauth2-proxy.

Task list:

- [ ] repo cloned
- [ ] Okta account created
- [ ] application set up
- [ ] users set up

## Second task
Configure the oauth2-proxy to support the Authorization Code Flow with Okta as an identity provider. Therefore set the missing parameters in [.env](.env) and [docker-compose.yml](docker-compose.yml). Find them in your Okta account and/or by opening the OpenID Connect metadata endpoint.

**Tip:** To create a secret for the oauth2-proxy cookie use the following command:
```sh
openssl rand -base64 32 | tr -- '+/' '-_'
```

When finished, test the setup and investigate the flow e.g. by using your browser's web developer tool. Especially have a look at the cookies, created by the oauth2-proxy. 

Task list:

- [ ] oauth2-proxy configured
- [ ] oauth2-proxy setup tested
- [ ] flow investigated 

## Third task ##
Enable PKCE (Proof Key for Code Exchange) by setting the respective parameter(s) in [docker-compose.yml](docker-compose.yml). 

When finished, test the setup and investigate the flow. Watch out for the differences introduced by PKCE.

Task list:

- [ ] PKCE enabled on oauth2-proxy
- [ ] oauth2-proxy setup tested
- [ ] flow investigated

## Fourth task ##
Configure the oauth2-proxy to support the Client Credentials Flow with Okta as an identity provider. Therefore create a second application in Okta representing a consuming machine.

When finished, test the setup and investigate the flow. 

Task list:

- [ ] oauth2-proxy configured
- [ ] oauth2-proxy setup tested
- [ ] flow investigated 



 
