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
- **RFC 6755** - An IETF URN Sub-Namespace for OAuth: Establishes a URN sub-namespace for OAuth-related parameter names and values
- **RFC 6819** - OAuth 2.0 Threat Model and Security Considerations: Comprehensive analysis of OAuth 2.0 security threats and countermeasures
- **RFC 7009** - OAuth 2.0 Token Revocation: Defines a mechanism for clients to notify authorization servers that a token is no longer needed
- **RFC 7521** - Assertion Framework for OAuth 2.0 Client Authentication and Authorization Grants: Common framework for using assertions with OAuth 2.0
- **RFC 7522** - SAML 2.0 Profile for OAuth 2.0: Defines how SAML 2.0 assertions can be used for client authentication and authorization grants
- **RFC 7523** - JWT Profile for OAuth 2.0 Client Authentication and Authorization Grants: Defines how JWTs can be used for client authentication and authorization grants
- **Kerberos V5 Profile for OAuth 2.0 (Draft)**: Defines how Kerberos V5 tickets can be used for client authentication and authorization grants in OAuth 2.0
- **RFC 7636** - PKCE: Proof Key for Code Exchange, security extension for public clients
- **RFC 7628** - SASL OAuth Mechanisms: Defines SASL mechanisms (OAUTHBEARER and OAUTH10A) for using OAuth in non-HTTP-based protocols like IMAP and SMTP
- **RFC 7591** - Dynamic Client Registration: Allows clients to register themselves with authorization servers
- **RFC 7592** - Dynamic Client Registration Management Protocol: Defines how clients can manage their dynamically registered OAuth 2.0 client configurations
- **OAuth Client ID Metadata Document (Draft)**: Defines a method for clients to publish metadata about themselves at a well-known location, enabling authorization servers and resource servers to discover client configuration
- **OAuth 2.0 Client ID Scheme (Draft)**: Defines a mechanism for encoding client type and metadata directly in the client identifier, enabling authorization servers to derive client properties without additional lookups
- **RFC 7662** - OAuth 2.0 Token Introspection: Defines a method for resource servers to query an authorization server about the state and metadata of an OAuth 2.0 token
- **RFC 9701** - JWT Response for OAuth Token Introspection: Extends the token introspection endpoint with the capability to return responses as signed and optionally encrypted JWTs, providing stronger assurance for resource servers
- **RFC 8252** - OAuth 2.0 for Native Apps: Best practices for OAuth 2.0 in native applications, including mobile and desktop apps
- **RFC 8414** - Authorization Server Metadata: Standardizes discovery of authorization server capabilities
- **OAuth 2.0 Authorization Server Discovery Metadata (Draft)**: Extends RFC 8414 with additional metadata for authorization server discovery and capabilities advertisement
- **RFC 8417** - Security Event Token (SET): Defines a JWT-based data structure for representing security and identity-related events, such as token revocations, logout events, and state changes
- **RFC 8628** - OAuth 2.0 Device Authorization Grant: Defines an OAuth grant type for browserless and input-constrained devices
- **RFC 8935** - Push-Based Security Event Token (SET) Delivery Using HTTP: Defines how SETs can be delivered to recipients using HTTP POST over TLS for push-based event distribution
- **RFC 8936** - Poll-Based Security Event Token (SET) Delivery Using HTTP: Defines how recipients can poll for SETs using HTTP POST, providing an alternative delivery method where recipients initiate requests to check for and retrieve security events
- **Management API for SET Event Streams (Draft)** - Defines a simple control plane for configuring Security Event Token transmitters and recipients, including creating, pausing, and deleting event streams that use the delivery models from RFC 8935 and RFC 8936 while relying on the SET structure defined in RFC 8417
- **Security Events RISC Use Cases (Draft)** - Illustrates practical adoption patterns for the RISC profile by mapping common account security scenarios to the SET framework in RFC 8417 and its HTTP delivery mechanisms in RFC 8935 and RFC 8936, highlighting coordination needs between transmitters and recipients
- **RFC 9493** - Subject Identifiers for Security Event Tokens: Formalizes Subject Identifiers as JSON objects for identifying subjects in SETs and JWTs, defining identifier formats (email, phone, issuer/subject, opaque, account, DID, URI, aliases) and the JWT "sub_id" claim
- **RFC 8693** - OAuth 2.0 Token Exchange: Defines a protocol for exchanging security tokens, enabling delegation and impersonation scenarios
- **RFC 8705** - OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens: Defines mutual TLS for client authentication and methods for binding access tokens to client certificates
- **RFC 8707** - OAuth 2.0 Resource Indicators: Allows clients to specify target resource servers when requesting access tokens
- **RFC 9101** - OAuth 2.0 JWT-Secured Authorization Request (JAR): Enables passing authorization request parameters as signed and/or encrypted JWTs for enhanced security
- **RFC 9126** - OAuth 2.0 Pushed Authorization Requests: Allows clients to push authorization request parameters directly to the authorization server before redirecting the user
- **JWT Secured Authorization Response Mode for OAuth 2.0 (JARM)**: Defines a response mode that enables authorization responses to be encoded as signed and/or encrypted JWTs for enhanced security
- **RFC 9207** - OAuth 2.0 Authorization Server Issuer Identification: Provides a mechanism to prevent mix-up attacks by requiring authorization servers to identify themselves in authorization responses
- **OAuth 2.0 Mix-Up Mitigation (Draft)**: Defines security mechanisms to prevent mix-up attacks in OAuth 2.0 implementations where multiple authorization servers are used
- **OAuth 2.0 Incremental Authorization (Draft)**: Allows clients to request additional scopes from users over time without requiring re-authentication
- **RFC 9396** - OAuth 2.0 Rich Authorization Requests: Enables clients to specify fine-grained authorization data using structured syntax for complex authorization scenarios
- **RFC 9635** - Grant Negotiation and Authorization Protocol (GNAP): A next-generation authorization protocol designed to address limitations of OAuth 2.0, enabling flexible grant negotiation and advanced delegation scenarios
- **RFC 9449** - OAuth 2.0 Demonstrating Proof of Possession (DPoP): Mechanism for sender-constraining OAuth tokens using proof-of-possession at the application layer
- **RFC 9470** - OAuth 2.0 Step Up Authentication Challenge Protocol: Defines a mechanism for resource servers to signal to clients that additional authentication is required to access protected resources
- **OAuth 2.0 Proof-of-Possession (PoP) Security Architecture (Draft)**: Provides architectural guidance and security considerations for implementing proof-of-possession mechanisms in OAuth 2.0
- **OAuth 2.0 Proof-of-Possession: Authorization Server to Client Key Distribution (Draft)**: Defines how authorization servers can securely distribute keys to clients for proof-of-possession token binding
- **A Method for Signing HTTP Requests for OAuth (Draft)**: Defines a method for signing HTTP requests using OAuth credentials, enabling request integrity and authenticity verification
- **RFC 9200** - ACE-OAuth Framework for Constrained Environments: Adapts OAuth 2.0 for IoT and constrained devices, defining an authentication and authorization framework (ACE) using CoAP, CBOR, COSE, and CWT for resource-constrained environments
- **RFC 9201** - Additional OAuth Parameters for ACE: Defines additional parameters for OAuth 2.0 token and introspection endpoints when used with ACE, including proof-of-possession key parameters (req_cnf, cnf, rs_cnf)
- **RFC 9700** - OAuth 2.0 Security Best Current Practice: Comprehensive security guidelines and best practices for OAuth 2.0 implementations, consolidating lessons learned and security considerations
- **OAuth 2.0 Multiple Response Type Encoding Practices**: Defines encoding for multiple response types in OAuth 2.0 authorization responses
- **OAuth 2.0 Form Post Response Mode**: Defines an OAuth 2.0 response mode that enables authorization responses to be delivered via an HTML form POST to the client, providing enhanced security for response data transmission
- **OAuth 2.0 Attestation-Based Client Authentication (Draft)**: Enables client instances to authenticate using attestations bound to client instance keys, supporting both traditional and platform-specific attestation mechanisms
- **OAuth 2.0 for Browser-Based Applications (Draft)**: Best practices and security considerations for OAuth 2.0 applications running entirely in the browser, including guidance on using authorization code flow with PKCE
- **Encoding claims in the OAuth 2 state parameter using a JWT (Draft)**: Defines how to encode claims in the OAuth 2.0 state parameter as a JWT, enabling secure passing of additional information between authorization request and response
- **OAuth 2.0 Token Binding (Draft)**: Defines how to apply Token Binding protocol to OAuth 2.0, enabling cryptographic binding of security tokens to TLS connections to prevent token export and replay attacks
- **User-Managed Access (UMA) Profile of OAuth 2.0 (Draft)**: Defines an OAuth-based access management protocol that enables resource owners to control access to their protected resources by creating authorization policies at an authorization server

### JOSE/JWT Security

- **RFC 7515** - JSON Web Signature (JWS): Digital signature format for JSON
- **RFC 7516** - JSON Web Encryption (JWE): Encryption format for JSON
- **RFC 7517** - JSON Web Key (JWK): Format for representing cryptographic keys in JSON
- **RFC 7518** - JSON Web Algorithms (JWA): Cryptographic algorithms for JOSE
- **RFC 7519** - JSON Web Token (JWT): Compact, URL-safe means of representing claims
- **RFC 7800** - Proof-of-Possession Key Semantics for JWTs: Defines how to declare in a JWT that the presenter possesses a particular proof-of-possession key and how recipients can cryptographically confirm possession
- **RFC 8176** - Authentication Method Reference Values: Establishes a registry for "amr" (Authentication Methods References) claim values and defines standard identifiers for authentication methods such as biometrics, passwords, OTP, multi-factor authentication, and hardware keys
- **RFC 8725** - JSON Web Token Best Current Practices: Security best practices and recommendations for JWT implementations
- **RFC 9278** - JWK Thumbprint URI: Defines a URI format for representing JWK Thumbprint values, enabling JWK Thumbprints to be used as key identifiers in contexts requiring URIs (e.g., as subject identifiers in Self-Issued OpenID Provider v2)
- **RFC 9068** - JWT Profile for OAuth 2.0 Access Tokens: Standardizes JWT-based access tokens
- **RFC 9728** - JWT Profile for OAuth 2.0 Authorization Server Issuer Identification: Defines how to prevent mix-up attacks by including issuer identification in JWT responses
- **RFC 9901** - Selective Disclosure for JSON Web Tokens (SD-JWT): Defines a mechanism for selective disclosure of JWT claims enabling minimal disclosure and privacy-preserving credential presentations

### OpenID Connect Identity Layer

- **OpenID Connect Core 1.0**: Main specification defining the identity layer on top of OAuth 2.0
- **OpenID Connect Discovery 1.0**: Mechanism for discovering OpenID Connect provider configuration
- **OpenID Connect Dynamic Client Registration 1.0**: Extension for dynamic client registration in OIDC context
- **OpenID Connect Session Management 1.0**: Defines how to monitor and manage authentication sessions between relying parties and OpenID providers
- **OpenID Connect Front-Channel Logout 1.0**: Defines a front-channel logout mechanism that allows relying parties to be notified when a user logs out
- **OpenID Connect Back-Channel Logout 1.0**: Defines a back-channel logout mechanism using direct server-to-server communication for logout notifications
- **OpenID Connect RP-Initiated Logout 1.0**: Defines how relying parties can initiate logout of the end-user at the OpenID provider
- **OpenID Connect for Identity Assurance 1.0**: Framework for exchanging verified identity claims with assurance levels and evidence of identity verification
- **OpenID Connect for Identity Assurance Claims Registration 1.0**: Specifies how OpenID Providers advertise and register verified claims metadata so relying parties can request Identity Assurance claims with aligned semantics
- **OpenID Identity Assurance Schema Definition 1.0**: Provides the reusable JSON schema components for representing verified claims content defined by OpenID Identity Assurance, enabling consistent data exchange across providers
- **OpenID Connect Core Error Code unmet_authentication_requirements**: Introduces an interoperable error signal for OIDC Core flows when stronger authentication is required, standardizing client handling of re-authentication prompts
- **Initiating User Registration via OpenID Connect 1.0**: Specifies the `prompt=create` parameter to let clients trigger user registration flows through standard OIDC authorization requests while retaining compatibility with existing providers
- **OpenID Shared Signals Framework 1.0**: Defines a framework for sharing signals and events between cooperating parties, enabling real-time security event distribution using Security Event Tokens (SETs)
- **OpenID Continuous Access Evaluation Profile 1.0**: Profiles the Shared Signals Framework to express continuous access evaluation events, mapping CAEP signal semantics onto Security Event Tokens so relying parties can adjust session state in near real time
- **OpenID RISC Profile Specification 1.0**: Establishes the OpenID Risk Incident Sharing and Coordination model, mapping RISC event semantics to Security Event Tokens and HTTP delivery so providers can exchange account and credential risk signals
- **OpenID RISC Profile of IETF Security Events 1.0**: Profiles RFC 8417 (SET), RFC 8935 (push delivery), and RFC 8936 (poll delivery) for Risk Incident Sharing and Coordination, defining subject identifiers, transmitter configuration discovery, and management APIs for event streams
- **OpenID RISC Event Types 1.0**: Defines specific event types for RISC including account security events (credential changes, account disabled/enabled, purged), identifier events (changed, recycled), opt-out management, recovery events, and session revocation

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
