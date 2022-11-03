# Introduction

Welcome to the Opkit developer documentation!

## Overview

Opkit is a platform for collecting and verifying patient health insurance details. Our platform makes it easy for healthcare organizations to collect accurate insurance information from patients and verify their coverage and benefits.

## Getting Started

To start developing with Opkit, you must first be an Opkit customer! You can learn more and schedule a demo from our main website: <https://www.opkit.co/>

## API vs. Webhooks

Opkit supports two different integration modes: "pull" (via our JSON REST API) and "push" (via webhooks). To determine which mode is right for your use-case, continue reading.

## Security and Compliance

Opkit is SOC 2 Type 2 certified and HIPAA-compliant. Our software is built on Amazon Web Services, the leading secure cloud services provider. We use state-of-the-art cryptographic protocols to encrypt data in transit and at rest. Our network is secured by AWS' Virtual Private Cloud and Security Groups features.

## Support

We're happy to answer your questions and hear your feedback. Please reach out to us at founders@opkit.co.

## About Us

Opkit is a Y Combinator-backed healthcare payments startup based in New York City.

# The API

Opkit exposes a JSON REST API that allows healthcare organizations to fetch their data on-demand from Opkit's backend servers.

## Why the API?

Opkit's API is the fastest and easiest way to start pulling data from Opkit into your system. Webhooks, while more powerful, generally require more work to use.

## Design Principles

Opkit's API exhibits the following characteristics:

- RESTful URLs
- JSON request and response bodies
- Standard HTTP methods and response codes
- API key-based authentication
- Cursor-based pagination

## API Keys

You can generate and manage API keys from the settings page of the Opkit dashboard. Remember to store these values somewhere safe. After all, they can be used to gain access to Protected Health Information (PHI).

## Authentication

Opkit's API uses API key-based authentication via the HTTP Bearer Token scheme. To authenticate a request, simply include an "Authorization" header with your API key, like so:

```
curl https://api.opkit.co/v1/insurance_cards -H "Authorization: Bearer <api-key>"
```

# Webhooks

In addition to our JSON REST API, Opkit also supports webhooks.

## Why Webhooks?

In general, a webhook-based integration will require more engineering work than an API-based integration. However, webhooks are much more powerful - not only do they ensure your application receives data as fast as possible, they also provide you with more fine-grained detail than is accessible through the API.

## Webhook Event Type Definitions

You can find definitions of the various Opkit webhook event types in the API reference.

## Registering a Webhook

You can register a webhook endpoint from the settings page of the Opkit dashboard.
