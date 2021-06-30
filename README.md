* Start Date: (2021-06-28)
* RFC PR:
* Core services Module:
# Summary
Core services is a module for implementing the process of authorization and authentication for all services in the platform Platzily.

# Motivation
### What are we doing this?
this development will allow improvement in different knowledge, for example, the correct form to create an architecture, what must have in consideration for implement how's
* structure
* database for selecting
* language for selecting
* providers of services
* how to encrypt information
* how to generate the integration with other services.
* how to standarize the ask for to information

### What use cases does it support?

* encrypt information when is received and distribute for appropriate service.

* receive all config about other services and changed for handling since core service

* protect the infrastructure of other services

ui login
plugin de oauth

- Start Date: (2021-16-06)
- RFC PR:
- Admin services Module:

# Summary

Core Services is in charge of Authentication and Authorization Method to protect the application from attacks and organizer the users calls.

Services like:

- Apigateway
- Authentication for end users.
- Authorization for private microservices.

# Motivation

Why are we doing this?

- The system requires a control for all the calls inside the application, and manage the apis issues, campaings, statistics, links and users.

What use cases does it support?

- Expose a public api with only the methods the client need.
- Mantain as private the services and methods who need to be private.
- Protect the application from attacks.
- 

What is the expected outcome?

- Successfully control over authentication services.
- Manage the api calls.
- An Healthy application traffic.
- Monitoring the status of mthe app.

# Detailed design

▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬

## Golang

- This programming lenguage its more powerfull than javascript. Its stable, and have high performacne memory process, his garbage collector are more efficient.

- As a team and students we want challenge ourselves in learning process of a entirely new programing lenguage.

- Is the favorite programing lenguage of our CEO.

## Apigateway

When consumers of API content (especially in microservices) query backend services, the implementations suffer a lot of complexity and burden with the sizes and complexity of their microservices responses.

Sits between the client and all the source servers, adding a new layer that removes all the complexity to the clients, providing them only the information that the UI needs.

- Chaining Request
- Merge Request

## KrakenD Apigateway

KrakenD is a high-performance open source API Gateway.

Its core functionality is to create an API that acts as an aggregator of many microservices into single endpoints, doing the heavy-lifting automatically for you: aggregate, transform, filter, decode, throttle, auth and more.

KrakenD needs no programming as it offers a declarative way to create the endpoints. It is well structured and layered and open to extending its functionality using plug-and-play middleware developed by the community or in-house.

- KrakenD Features
- Validation of JWT with krakend-jose plugin.
- Auth0 Integration.
- OAuth2 Client Credentials using krakend-oauth2-clientcredentials plugin.
- Revoking valid tokens.

Add main image in 'https://www.krakend.io/docs/overview/introduction/'

## Secrets Provider (JWT Validation)

In order to increment the trustaliability of the system, krakenD allow us to use a Secrets Provider for storage crucial information like JWK Tokens, and implement rotation of the secrets.

Can use almost any provider of the market:
- Amazon KMS
- Azure’s Key Vault
- Google Cloud KMS
- Hashicorp’s Vault

## OAuth2 Client Credentials

Through the OAuth 2.0 Client Credentials Grant KrakenD can request to your authorization server an access token to reach protected resources.

The client credentials authorize KrakenD, as the client, to access the protected resources.

Successfully setting the client credentials for a backend means that KrakenD can get the protected content, but the endpoint offered to the end-user is going to be public unless you protect it with JWT.

## Architecture

Objectives:

- Atenuate the coupling to the dependencies between microservices using the 'aggregation' feature of KrakenD.

- Protect resources using OAuth2 client-credential.

-

## Como construir el archivo de configuración de Krakend
-- Cada equipo va a crear un archivo de configuracion con nuestras especificaciones para despues de manera automatizadas crear el archivo de configuración final para Krakend.




