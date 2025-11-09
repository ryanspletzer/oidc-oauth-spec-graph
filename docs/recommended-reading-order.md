# Recommended Reading Order for OAuth and OpenID Connect Specifications

Learning the OAuth 2.0 and OpenID Connect ecosystem can be overwhelming
given the number of interconnected specifications.
This guide provides a recommended reading order based on practical learning experience,
starting with high-level concepts and progressively diving into foundational and advanced topics.

## Learning Philosophy

The approach recommended here is to **start with OpenID Connect** (the identity layer),
which provides a complete authentication solution
and naturally references the underlying OAuth 2.0 and JWT specifications.
This top-down approach helps you understand the "why" before diving into the "how" of the foundational specs.

## Phase 1: Start with Identity (OpenID Connect)

### 1. OpenID Connect Core 1.0

**Why start here:** OpenID Connect provides a complete, real-world authentication solution
that's easier to grasp than starting with abstract OAuth 2.0 concepts.
It shows you what a full implementation looks like.

**What to focus on:**

- Basic authentication flow (authorization code flow)
- ID tokens and their structure
- UserInfo endpoint
- The relationship between OAuth 2.0 and OIDC

**Don't worry about:** Every grant type detail or edge case - you'll come back to those.

### References will lead you to foundational specs

As you read OpenID Connect Core, you'll encounter references to:

- RFC 6749 (OAuth 2.0) - for the authorization framework
- RFC 7519 (JWT) - for token format
- JOSE specs (JWS, JWE, JWK, JWA) - for cryptographic operations

## Phase 2: OAuth 2.0 Foundations

Now that you understand what OpenID Connect builds on top of, dive into the OAuth 2.0 core.

### 2. RFC 6749 - OAuth 2.0 Authorization Framework

**Why now:** With OpenID Connect context, OAuth 2.0's abstract concepts make more sense.

**What to focus on:**

- The four roles (resource owner, client, authorization server, resource server)
- Authorization code flow (you've seen this in OIDC)
- Client authentication methods
- Access tokens and refresh tokens

**What to skim:** Implicit flow (deprecated), Resource Owner Password Credentials flow (legacy)

### 3. RFC 6750 - Bearer Token Usage

**Why now:** You need to understand how to actually use the access tokens OAuth 2.0 provides.

**What to focus on:**

- How to send bearer tokens in HTTP requests
- Token security considerations

### 4. RFC 7636 - PKCE (Proof Key for Code Exchange)

**Why now:** Essential modern security extension that you'll use in almost every implementation.

**What to focus on:**

- Why PKCE is needed (authorization code interception)
- How code challenge and verifier work
- When to use PKCE (always, for all client types)

## Phase 3: Token Format and Cryptography

You've been reading about tokens - now understand their structure and security.

### 5. RFC 7519 - JSON Web Token (JWT)

**Why now:** You've seen JWTs referenced everywhere; time to understand their structure.

**What to focus on:**

- JWT structure (header, payload, signature)
- Claims and their meaning
- Signed vs encrypted tokens

### 6. RFC 7515 - JSON Web Signature (JWS)

**Why now:** Understand how JWTs are signed and verified.

**What to focus on:**

- Signature formats (compact serialization)
- How signature verification works

### 7. RFC 7517 - JSON Web Key (JWK)

**Why now:** Learn how keys are represented and shared.

**What to focus on:**

- JWK structure
- JWK Sets (used in discovery endpoints)

### 8. RFC 7518 - JSON Web Algorithms (JWA)

**Reference material:** Skim this to understand available algorithms. Deep-dive when implementing specific algorithms.

## Phase 4: Discovery and Dynamic Configuration

Now that you understand the protocols, learn how systems discover each other.

### 9. OpenID Connect Discovery 1.0

**Why now:** Learn how clients automatically discover provider capabilities.

**What to focus on:**

- Discovery endpoint (/.well-known/openid-configuration)
- Metadata format
- How this simplifies client configuration

### 10. RFC 8414 - OAuth 2.0 Authorization Server Metadata

**Why now:** The OAuth 2.0 version of discovery, referenced by OIDC Discovery.

**What to focus on:**

- Metadata parameters
- Differences from OIDC Discovery

### 11. RFC 7591 - OAuth 2.0 Dynamic Client Registration

**Why now:** Understand how clients can register themselves programmatically.

**What to focus on:**

- Registration endpoint
- Client metadata
- Dynamic vs static registration

### 12. OpenID Connect Dynamic Client Registration 1.0

**Why now:** OIDC-specific extensions to dynamic registration.

## Phase 5: Modern Security and Best Practices

You now have the foundations - time to learn modern security practices.

### 13. RFC 8252 - OAuth 2.0 for Native Apps

**Why important:** Essential if building mobile or desktop applications.

**What to focus on:**

- Why embedded web views are problematic
- Using system browsers
- Custom URL schemes vs claimed HTTPS URLs
- Loopback interface for desktop apps

### 14. RFC 9700 - OAuth 2.0 Security Best Current Practice

**Why critical:** Consolidated security guidance based on years of lessons learned.

**What to focus on:**

- Mandatory recommendations
- Deprecated patterns to avoid
- Modern security requirements

### 15. RFC 8725 - JWT Best Current Practices

**Why critical:** Security best practices specifically for JWT usage.

**What to focus on:**

- Common JWT vulnerabilities
- Algorithm selection
- Claim validation

### 16. OAuth 2.1 Authorization Framework (Draft)

**Why now:** See how OAuth is evolving to incorporate security best practices by default.

**What to focus on:**

- What's changed from OAuth 2.0
- Mandatory PKCE
- Removed flows (implicit, password)

## Phase 6: Advanced Flows and Extensions

With solid foundations, explore specialized use cases and extensions.

### 17. RFC 7662 - Token Introspection

**Use case:** Resource servers need to validate opaque tokens.

### 18. RFC 7009 - Token Revocation

**Use case:** Need to invalidate tokens before expiration.

### 19. RFC 8693 - Token Exchange

**Use case:** Delegation and impersonation scenarios in microservices.

### 20. RFC 9449 - DPoP (Demonstrating Proof of Possession)

**Use case:** Binding tokens to clients using proof-of-possession.

### 21. RFC 8705 - Mutual TLS Client Authentication

**Use case:** Certificate-based client authentication and token binding.

### 22. RFC 9126 - Pushed Authorization Requests (PAR)

**Use case:** Enhanced security by pushing parameters directly to authorization server.

### 23. RFC 8628 - Device Authorization Grant

**Use case:** Input-constrained devices (smart TVs, IoT devices).

## Phase 7: Specialized Topics

Explore these based on your specific needs.

### Identity and Access Tokens

- **RFC 9068** - JWT Profile for OAuth 2.0 Access Tokens: Standardized JWT-based access tokens
- **RFC 9728** - JWT Profile for OAuth 2.0 Authorization Server Issuer Identification: Mix-up attack prevention

### Enterprise Scenarios

- **RFC 7521, 7522, 7523** - Assertion frameworks: Using SAML or JWT assertions for authentication
- **RFC 8707** - Resource Indicators: Specifying target resource servers
- **RFC 9396** - Rich Authorization Requests: Complex authorization scenarios

### Additional Security

- **RFC 9207** - Authorization Server Issuer Identification: Mix-up attack prevention
- **RFC 9470** - Step Up Authentication: Requesting additional authentication dynamically

### User-Managed Access

- **UMA 2.0 Grant** - Party-to-party authorization
- **UMA 2.0 Federated Authorization** - User-controlled resource sharing

### Browser-Based Applications

- **OAuth 2.0 for Browser-Based Applications (Draft)** - SPA-specific guidance

## Tips for Success

1. **Don't read linearly:** Jump between specs as references guide you
2. **Implement as you learn:** Build simple implementations to solidify understanding
3. **Use the specification graph:** The [main graph](../graph.md) shows dependencies between specs
4. **Focus on understanding, not memorization:** Specs are reference material
5. **Revisit earlier specs:** Your understanding deepens as you learn more
6. **Join the community:** Follow the OAuth working group, read security advisories
7. **Skim first, deep-dive later:** Get the big picture before diving into details

## What to Skip Initially

- **RFC 6819** - Threat Model: Read this after understanding the basics, as context improves comprehension
- **Implicit Flow details:** This flow is deprecated
- **Resource Owner Password Credentials flow:** Legacy and generally discouraged
- **RFC 7516 (JWE):** Only needed if you're implementing encrypted tokens (less common)

## Learning Resources Beyond Specifications

- **oauth.net** - Community resources and libraries
- **OpenID Connect playground** - Interactive testing
- **jwt.io** - JWT debugging and validation
- **OAuth 2.0 Simplified** by Aaron Parecki - Practical guide
- **IETF OAuth working group discussions** - See real-world discussions

## Common Learning Pitfalls

1. **Trying to read RFC 6749 first without context** - Start with OIDC instead
2. **Ignoring security specs** - RFC 9700 and RFC 8725 are essential, not optional
3. **Implementing deprecated flows** - Skip implicit flow, it's deprecated
4. **Not using PKCE** - PKCE should be used for all OAuth flows
5. **Treating specs as tutorials** - They're reference documents, use guides alongside them

## Conclusion

Learning OAuth 2.0 and OpenID Connect is a journey.
Start with the high-level identity layer (OpenID Connect),
follow references to understand the foundations (OAuth 2.0 and JWT),
then explore discovery mechanisms, modern security practices, and specialized extensions based on your needs.

The key is to build understanding incrementally while maintaining context for why each specification exists.
Use this reading order as a guide, but don't hesitate to jump around as your curiosity and needs dictate.

Happy learning!
