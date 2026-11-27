# Godaddy for `libdns`

[![godoc reference](https://img.shields.io/badge/godoc-reference-blue.svg)](https://pkg.go.dev/github.com/libdns/godaddy)

This package implements the libdns interfaces for the [Godaddy API](https://developer.godaddy.com/doc/endpoint/domains)

## Authentication

`APIToken` accepts either kind of GoDaddy credential:

- **Personal Access Token (PAT)**: pass the token as-is. It is sent as `Authorization: Bearer <token>`. The token needs the `domains.domain:read` and `domains.dns:update` scopes.
- **Classic Developer Key**: pass `KEY:SECRET`. It is sent as `Authorization: sso-key KEY:SECRET`. GoDaddy is deprecating Classic Developer Keys for the Domains API, so prefer a PAT for new setups.

## Example

Here's a minimal example of how to get all your DNS records using this `libdns` provider (see `_example/main.go`)
