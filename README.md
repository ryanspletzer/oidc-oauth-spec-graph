# OpenID Connect and OAuth Specification Graph

This repository contains a visual representation of the relationships between OpenID Connect, OAuth 2.0, and related specifications including JWT (JSON Web Token) and JOSE (JSON Web Signature/Encryption) standards and more.

## Specification Graph

See [graph.md](graph.md) and expand the graph in GitHub to browse more easily, or view the graph code in your preferred
Mermaid chart viewer.

## Overview

The modern web authentication and authorization ecosystem is built on a foundation of interconnected specifications. Understanding how these specifications relate to and depend on each other is crucial for developers implementing secure authentication systems. This diagram visualizes these relationships in an easy-to-understand format.

**Why does this project exist?** Read more about the [motivation behind this project](docs/motivation.md).

## What's Included

The diagram shows the dependency relationships between:

- **Discovery and Metadata**: Resource discovery protocols
- **OAuth 2.0 RFCs**: Core authorization framework and extensions
- **JOSE/JWT Standards**: Cryptographic foundations for secure tokens
- **OpenID Connect**: Identity layer built on top of OAuth 2.0
- **UMA (User-Managed Access)**: User-controlled authorization for resource sharing

Each node in the graph is clickable and links directly to the official specification document.

## Specification Categories

### Discovery and Metadata

- **RFC 7033** - WebFinger: Protocol for discovering information about people and resources, used by OpenID Connect Discovery

### OAuth 2.0 Foundation

- **RFC 6749** - OAuth 2.0 Authorization Framework: The core OAuth 2.0 specification
- **OAuth 2.1 Authorization Framework (Draft)**: Consolidates OAuth 2.0 and related best practices into a single document, mandating PKCE, eliminating implicit flow, and incorporating security improvements from RFC 8252
- **RFC 6750** - Bearer Token Usage: Defines how to use bearer tokens in HTTP requests
- **RFC 6819** - OAuth 2.0 Threat Model and Security Considerations: Comprehensive analysis of OAuth 2.0 security threats and countermeasures
- **RFC 7521** - Assertion Framework for OAuth 2.0 Client Authentication and Authorization Grants: Common framework for using assertions with OAuth 2.0
- **RFC 7522** - SAML 2.0 Profile for OAuth 2.0: Defines how SAML 2.0 assertions can be used for client authentication and authorization grants
- **RFC 7523** - JWT Profile for OAuth 2.0 Client Authentication and Authorization Grants: Defines how JWTs can be used for client authentication and authorization grants
- **RFC 7636** - PKCE: Proof Key for Code Exchange, security extension for public clients
- **RFC 7591** - Dynamic Client Registration: Allows clients to register themselves with authorization servers
- **RFC 7592** - Dynamic Client Registration Management Protocol: Defines how clients can manage their dynamically registered OAuth 2.0 client configurations
- **RFC 7662** - OAuth 2.0 Token Introspection: Defines a method for resource servers to query an authorization server about the state and metadata of an OAuth 2.0 token
- **RFC 8252** - OAuth 2.0 for Native Apps: Best practices for OAuth 2.0 in native applications, including mobile and desktop apps
- **RFC 8414** - Authorization Server Metadata: Standardizes discovery of authorization server capabilities
- **RFC 8628** - OAuth 2.0 Device Authorization Grant: Defines an OAuth grant type for browserless and input-constrained devices
- **RFC 8693** - OAuth 2.0 Token Exchange: Defines a protocol for exchanging security tokens, enabling delegation and impersonation scenarios
- **RFC 8705** - OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens: Defines mutual TLS for client authentication and methods for binding access tokens to client certificates
- **RFC 8707** - OAuth 2.0 Resource Indicators: Allows clients to specify target resource servers when requesting access tokens
- **RFC 9126** - OAuth 2.0 Pushed Authorization Requests: Allows clients to push authorization request parameters directly to the authorization server before redirecting the user
- **RFC 9207** - OAuth 2.0 Authorization Server Issuer Identification: Provides a mechanism to prevent mix-up attacks by requiring authorization servers to identify themselves in authorization responses
- **RFC 9396** - OAuth 2.0 Rich Authorization Requests: Enables clients to specify fine-grained authorization data using structured syntax for complex authorization scenarios
- **RFC 9449** - OAuth 2.0 Demonstrating Proof of Possession (DPoP): Mechanism for sender-constraining OAuth tokens using proof-of-possession at the application layer
- **RFC 9470** - OAuth 2.0 Step Up Authentication Challenge Protocol: Defines a mechanism for resource servers to signal to clients that additional authentication is required to access protected resources
- **RFC 9700** - OAuth 2.0 Token Revocation: Defines a mechanism for clients to notify authorization servers that a token is no longer needed
- **OAuth 2.0 Multiple Response Type Encoding Practices**: Defines encoding for multiple response types in OAuth 2.0 authorization responses
- **OAuth 2.0 Attestation-Based Client Authentication (Draft)**: Enables client instances to authenticate using attestations bound to client instance keys, supporting both traditional and platform-specific attestation mechanisms
- **OAuth 2.0 for Browser-Based Applications (Draft)**: Best practices and security considerations for OAuth 2.0 applications running entirely in the browser, including guidance on using authorization code flow with PKCE
- **Encoding claims in the OAuth 2 state parameter using a JWT (Draft)**: Defines how to encode claims in the OAuth 2.0 state parameter as a JWT, enabling secure passing of additional information between authorization request and response

### JOSE/JWT Security

- **RFC 7515** - JSON Web Signature (JWS): Digital signature format for JSON
- **RFC 7516** - JSON Web Encryption (JWE): Encryption format for JSON
- **RFC 7517** - JSON Web Key (JWK): Format for representing cryptographic keys in JSON
- **RFC 7518** - JSON Web Algorithms (JWA): Cryptographic algorithms for JOSE
- **RFC 7519** - JSON Web Token (JWT): Compact, URL-safe means of representing claims
- **RFC 8725** - JSON Web Token Best Current Practices: Security best practices and recommendations for JWT implementations
- **RFC 9068** - JWT Profile for OAuth 2.0 Access Tokens: Standardizes JWT-based access tokens
- **RFC 9728** - JWT Profile for OAuth 2.0 Authorization Server Issuer Identification: Defines how to prevent mix-up attacks by including issuer identification in JWT responses

### OpenID Connect Identity Layer

- **OpenID Connect Core 1.0**: Main specification defining the identity layer on top of OAuth 2.0
- **OpenID Connect Discovery 1.0**: Mechanism for discovering OpenID Connect provider configuration
- **OpenID Connect Dynamic Client Registration 1.0**: Extension for dynamic client registration in OIDC context

### UMA (User-Managed Access)

- **UMA 2.0 Grant for OAuth 2.0**: Defines an OAuth grant type for party-to-party authorization
- **UMA 2.0 Federated Authorization**: Profile for federated authorization using UMA, enabling users to control access to their resources

## Understanding the Dependencies

The arrows in the diagram show how specifications build upon each other:

1. **OAuth 2.0 Forms the Base**: Most specifications extend or reference RFC 6749
2. **JOSE Provides Cryptographic Foundations**: JWT and related specs depend on JOSE for security
3. **OpenID Connect Builds on Both**: OIDC uses OAuth 2.0 for authorization and JWT for identity tokens
4. **UMA Extends OAuth for User-Controlled Authorization**: UMA builds on OAuth 2.0 and Bearer tokens to enable party-to-party resource sharing
5. **Modern Extensions**: Newer specifications like RFC 9068 integrate multiple existing standards

## Usage

This diagram is useful for:

- **Developers** implementing OAuth 2.0 or OpenID Connect
- **Security architects** designing authentication systems
- **Students** learning about web authentication standards
- **Technical writers** documenting authentication flows

## Viewing the Diagram

The diagram renders automatically on GitHub. For local viewing or editing:

1. Use any Mermaid-compatible viewer or editor
2. Copy the Mermaid code into [Mermaid Live Editor](https://mermaid.live/)
3. Use VS Code with the Mermaid extension for local editing

## Contributing

If you notice missing specifications or incorrect dependencies, please open an issue or submit a pull request. When adding new specifications, please:

1. Verify the dependency relationships by reading the actual specification documents
2. Add clickable links to official specification sources
3. Update the specification categories section in this README

## License

This repository is available under The Unlicense. See the [LICENSE](LICENSE) file for details.

## Additional Resources

- [OAuth 2.0 Security Best Current Practice](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-security-topics)
- [OpenID Connect Documentation](https://openid.net/connect/)
- [IANA OAuth Parameters Registry](https://www.iana.org/assignments/oauth-parameters/oauth-parameters.xhtml)
