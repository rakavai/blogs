---
layout: post
title: Quick Overview of OpenAPI Specification
---

## What is OpenAPI

OpenAPI is a specification that defines how to describe a RESTful API with the
standardized format readable by both humans and machines.

### Quick History

Previously, the `OpenAPI specification` was part of `Swagger` and known as
`Swagger specification`. Now it's separated from `Swagger` and moved to a 
[new repo](https://github.com/OAI/OpenAPI-Specification).

So `OpenAPI` is the specification, and `Swagger` is a set of some open source
and paid tools for implementing `OpenAPI specification`. Besides `Swagger`, there
are [many tools for OpenAPI implementation](https://github.com/OAI/OpenAPI-Specification/blob/main/IMPLEMENTATIONS.md#implementations)
out there.

## Benefits of OpenAPI

What makes OpenAPI great is the number of tools built around this specification.
These tools have a lot of usages and applications.

### Easy collaboration and communication 

OpenAPI specification is a standardized format for RESTapi. Therefore, it is
straightforward to share knowledge of an API with widely used ubiquitous API
descriptions.

The specification can be used as contract between two services. 

Mock RESTful API server can be made from an OpenAPI specification. So even if
the server is not ready, the client can be implemented and tested with the mock
server.

### Ensure quality

There are tools to check an OpenAPI specification by running through validation
to ensure the api follows the industry standards.

It is also easy to catch breaking changes early since the OpenAPI specification
describes API from a high level. And there are tools for that too.

### Saves time with code generation

There are many implementations of OpenAPI that can generate server-side code for
implementation and client SDK in almost any programming language.

With swagger tools, interactive documentation also can be generated. [Here is an
example from Swagger.](https://petstore.swagger.io/) How awesome is that!

### Agnostic of programming language and process

OpenAPI is just a standardized API specification that is language-agnostic.

Using OpenAPI specification, we can develop following the approach 
`Specification-first` or `Implementation-first`.

For the Specification-first approach, code can be generated for the server for 
implementation and SDK for the client-side.

> **Don't drink too much Kool-Aid:**  
> There is a chance of being in the waterfall with the specification or 
> design-first approach. Make sure to design with iteration in mind.

### A large number of companies use OpenAPI

Many companies like GitHub, Atlassian, MuleSoft, Netflix, etc., use OpenAPI
specifications. So it is easy to use those API with OpenAPI implementations.

## Implementation of OpenAPI specification

These benefits are possible because of the vast number of tools for implementing
OpenAPI specification.

[List of known tooling that implements OpenAPI](https://github.com/OAI/OpenAPI-Specification/blob/main/IMPLEMENTATIONS.md#implementations)
