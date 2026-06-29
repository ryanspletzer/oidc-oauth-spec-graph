# OpenID Connect and OAuth Specification Graph

```mermaid
graph LR

  %% --- OpenID Connect ---
  subgraph OpenID_Connect
    OIDC_Core["OpenID Connect Core 1.0"]
    OIDC_Discovery["OpenID Connect Discovery 1.0"]
    OIDC_Reg["OpenID Connect Dynamic Client Registration 1.0"]
    OIDC_Session["OpenID Connect Session Management 1.0"]
    OIDC_FrontLogout["OpenID Connect Front-Channel Logout 1.0"]
    OIDC_BackLogout["OpenID Connect Back-Channel Logout 1.0"]
    OIDC_RPLogout["OpenID Connect RP-Initiated Logout 1.0"]
    OIDC_TokenBound["OpenID Connect Token Bound Authentication 1.0"]
    OIDC_IDA["OpenID Connect for Identity Assurance 1.0"]
    OIDC_IDA_Schema["OpenID Identity Assurance Schema Definition 1.0"]
    OIDC_IDA_Claims["OpenID Connect for Identity Assurance Claims Registration 1.0"]
    OIDC_UnmetAuthReq["OpenID Connect Core Error Code unmet_authentication_requirements"]
    OIDC_PromptCreate["Initiating User Registration via OpenID Connect 1.0"]
    OIDC_SSF["OpenID Shared Signals Framework 1.0"]
    OIDC_CAEP["OpenID Continuous Access Evaluation Profile 1.0"]
    OIDC_RISC_Spec["OpenID RISC Profile Specification 1.0"]
    OIDC_RISC_Profile["OpenID RISC Profile of IETF Security Events 1.0"]
    OIDC_RISC_Events["OpenID RISC Event Types 1.0"]
    OID4VCI["OpenID for Verifiable Credential Issuance 1.0"]
    OID4VP["OpenID for Verifiable Presentations 1.0"]
    SIOPv2["Self-Issued OpenID Provider v2 (Draft)"]
  end

  %% --- OAuth 2.0 RFCs ---
  subgraph OAuth_2_0_RFCs
    RFC6749["OAuth 2.0 Authorization Framework (RFC 6749)"]
    OAuth2_1["OAuth 2.1 Authorization Framework (Draft)"]
    RFC6750["Bearer Token Usage (RFC 6750)"]
    RFC6755["An IETF URN Sub-Namespace for OAuth (RFC 6755)"]
    RFC6819["OAuth 2.0 Threat Model and Security Considerations (RFC 6819)"]
    RFC7521["Assertion Framework for OAuth 2.0 (RFC 7521)"]
    RFC7522["SAML 2.0 Profile for OAuth 2.0 (RFC 7522)"]
    RFC7523["JWT Profile for OAuth 2.0 Client Authentication and Authorization Grants (RFC 7523)"]
    OAuth2_Kerberos["Kerberos V5 Profile for OAuth 2.0 (Draft)"]
    RFC7636["PKCE for OAuth 2.0 (RFC 7636)"]
    RFC7628["SASL OAuth Mechanisms (RFC 7628)"]
    RFC7009["OAuth 2.0 Token Revocation (RFC 7009)"]
    RFC7591["Dynamic Client Registration (RFC 7591)"]
    RFC7592["Dynamic Client Registration Management (RFC 7592)"]
    OAuth2_ClientIDMeta["OAuth Client ID Metadata Document (Draft)"]
    OAuth2_ClientIDScheme["OAuth 2.0 Client ID Scheme (Draft)"]
    RFC7662["OAuth 2.0 Token Introspection (RFC 7662)"]
    RFC9701["JWT Response for OAuth Token Introspection (RFC 9701)"]
    RFC8252["OAuth 2.0 for Native Apps (RFC 8252)"]
    RFC8414["Authorization Server Metadata (RFC 8414)"]
    OAuth2_ASDiscovery["OAuth 2.0 Authorization Server Discovery Metadata (Draft)"]
    RFC8417["Security Event Token (SET) (RFC 8417)"]
    RFC8628["OAuth 2.0 Device Authorization Grant (RFC 8628)"]
    RFC8935["Push-Based Security Event Token (SET) Delivery Using HTTP (RFC 8935)"]
    RFC8936["Poll-Based Security Event Token (SET) Delivery Using HTTP (RFC 8936)"]
    SET_StreamMgmt["Management API for SET Event Streams (Draft)"]
    RISC_UseCases["Security Events RISC Use Cases (Draft)"]
    RFC9493["Subject Identifiers for Security Event Tokens (RFC 9493)"]
    RFC8693["OAuth 2.0 Token Exchange (RFC 8693)"]
    RFC8705["OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens (RFC 8705)"]
    RFC8707["OAuth 2.0 Resource Indicators (RFC 8707)"]
    RFC9101["OAuth 2.0 JWT-Secured Authorization Request (JAR) (RFC 9101)"]
    RFC9126["OAuth 2.0 Pushed Authorization Requests (RFC 9126)"]
    OAuth2_JARM["JWT Secured Authorization Response Mode for OAuth 2.0 (JARM)"]
    RFC9207["OAuth 2.0 Authorization Server Issuer Identification (RFC 9207)"]
    OAuth2_MixUpMit["OAuth 2.0 Mix-Up Mitigation (Draft)"]
    OAuth2_IncrAuthz["OAuth 2.0 Incremental Authorization (Draft)"]
    RFC9396["OAuth 2.0 Rich Authorization Requests (RFC 9396)"]
    RFC9449["OAuth 2.0 Demonstrating Proof of Possession (RFC 9449)"]
    RFC9635["Grant Negotiation and Authorization Protocol (GNAP) (RFC 9635)"]
    RFC9470["OAuth 2.0 Step Up Authentication Challenge Protocol (RFC 9470)"]
    OAuth2_PoPArch["OAuth 2.0 Proof-of-Possession (PoP) Security Architecture (Draft)"]
    OAuth2_PoPKeyDist["OAuth 2.0 Proof-of-Possession: Authorization Server to Client Key Distribution (Draft)"]
    OAuth2_SignedHTTP["A Method for Signing HTTP Requests for OAuth (Draft)"]
    RFC9200["ACE-OAuth Framework for Constrained Environments (RFC 9200)"]
    RFC9201["Additional OAuth Parameters for ACE (RFC 9201)"]
    RFC9700["OAuth 2.0 Security Best Current Practice (RFC 9700)"]
    OAuth2_MultiResp["OAuth 2.0 Multiple Response Type Encoding Practices"]
    OAuth2_FormPost["OAuth 2.0 Form Post Response Mode"]
    OAuth2_AttestAuth["OAuth 2.0 Attestation-Based Client Authentication (Draft)"]
    OAuth2_BrowserApps["OAuth 2.0 for Browser-Based Applications (Draft)"]
    OAuth2_JWTState["Encoding claims in the OAuth 2 state parameter using a JWT (Draft)"]
    OAuth2_TokenBinding["OAuth 2.0 Token Binding (Draft)"]
    UMA_Profile["User-Managed Access (UMA) Profile of OAuth 2.0 (Draft)"]
    OAuth2_IdentityChaining["OAuth Identity and Authorization Chaining Across Domains (Draft)"]
    OAuth2_IdentityAssertion["Identity Assertion JWT Authorization Grant (Draft)"]
    OAuth2_AIAgents["OAuth 2.0 On-Behalf-Of User Authorization for AI Agents (Draft)"]
  end

  %% --- JOSE / JWT ---
  subgraph JOSE_JWT
    RFC7515["JSON Web Signature (JWS) (RFC 7515)"]
    RFC7516["JSON Web Encryption (JWE) (RFC 7516)"]
    RFC7517["JSON Web Key (JWK) (RFC 7517)"]
    RFC7518["JSON Web Algorithms (JWA) (RFC 7518)"]
    RFC7519["JSON Web Token (JWT) (RFC 7519)"]
    RFC7800["Proof-of-Possession Key Semantics for JWTs (RFC 7800)"]
    RFC8176["Authentication Method Reference Values (RFC 8176)"]
    RFC7638["JSON Web Key (JWK) Thumbprint (RFC 7638)"]
    RFC9278["JWK Thumbprint URI (RFC 9278)"]
    RFC8725["JSON Web Token Best Current Practices (RFC 8725)"]
    RFC9068["JWT Profile for OAuth 2.0 Access Tokens (RFC 9068)"]
    RFC9901["Selective Disclosure for JSON Web Tokens (RFC 9901)"]
    SDJWT_VC["SD-JWT-based Verifiable Credentials (Draft)"]
  end

  %% --- Discovery / Metadata ---
  subgraph Discovery_Metadata
    RFC7033["WebFinger (RFC 7033)"]
    RFC9728["OAuth 2.0 Protected Resource Metadata (RFC 9728)"]
  end

  %% --- UMA (User-Managed Access) ---
  subgraph UMA
    UMA_Grant["UMA 2.0 Grant for OAuth 2.0"]
    UMA_FedAuthz["UMA 2.0 Federated Authorization"]
  end

  %% ---- Edges: OAuth 2.0 internal references ----
  OAuth2_1 --> RFC6749
  OAuth2_1 --> RFC6750
  OAuth2_1 --> RFC8252
  OAuth2_1 --> RFC9207
  OAuth2_1 --> RFC9700

  RFC6819 --> RFC6749
  RFC6819 --> RFC6750
  RFC7009 --> RFC6749

  RFC7523 --> RFC7518
  RFC7523 --> RFC7519
  RFC7523 --> RFC7521

  RFC7636 --> RFC6749

  RFC7628 --> RFC6749
  RFC7628 --> RFC6750
  RFC7628 --> RFC7591

  RFC7591 --> RFC6749
  RFC7591 --> RFC7515
  RFC7591 --> RFC7519
  RFC7592 --> RFC6749
  RFC7592 --> RFC6750
  RFC7592 --> RFC7591

  OAuth2_ClientIDMeta --> RFC6749
  OAuth2_ClientIDMeta --> RFC7591
  OAuth2_ClientIDMeta --> RFC8414
  OAuth2_ClientIDMeta --> RFC9700
  OAuth2_ClientIDScheme --> RFC6749
  OAuth2_ClientIDScheme --> RFC7515
  OAuth2_ClientIDScheme --> RFC8414
  RFC7662 --> RFC6749
  RFC7662 --> RFC7519
  RFC9701 --> RFC7515
  RFC9701 --> RFC7516
  RFC9701 --> RFC7518
  RFC9701 --> RFC7519
  RFC9701 --> RFC7591
  RFC9701 --> RFC7662
  RFC9701 --> RFC8414
  RFC9701 --> RFC9700
  RFC8252 --> RFC6749
  RFC8414 --> RFC6749
  RFC8414 --> RFC7033
  RFC8414 --> RFC7515
  RFC8414 --> RFC7516
  RFC8414 --> RFC7517
  RFC8414 --> RFC7519
  RFC8414 --> RFC7591
  RFC8414 --> RFC7636
  RFC8414 --> RFC7662
  RFC8417 --> RFC6749
  RFC8417 --> RFC7515
  RFC8417 --> RFC7519
  RFC8628 --> RFC6749
  RFC8628 --> RFC6755
  RFC8935 --> RFC7515
  RFC8935 --> RFC7519
  RFC8935 --> RFC8417
  RFC8936 --> RFC7515
  RFC8936 --> RFC7519
  RFC8936 --> RFC8417
  RFC8936 --> RFC8935
  RFC9493 --> RFC7519
  RFC9493 --> RFC8417
  SET_StreamMgmt --> RFC7519
  SET_StreamMgmt --> RFC8417
  SET_StreamMgmt --> RFC8935
  SET_StreamMgmt --> RFC8936
  RFC8693 --> RFC6749
  RFC8693 --> RFC7519
  RFC8693 --> RFC7662
  RFC8705 --> RFC6749
  RFC8705 --> RFC6750
  RFC8705 --> RFC7519
  RFC8705 --> RFC7591
  RFC8705 --> RFC7662
  RFC8705 --> RFC8414
  RFC8707 --> RFC6749
  RFC9101 --> RFC6749
  RFC9101 --> RFC6750
  RFC9101 --> RFC7515
  RFC9101 --> RFC7516
  RFC9101 --> RFC7518
  RFC9101 --> RFC7519
  RFC9101 --> RFC8414
  RFC9126 --> RFC6749
  RFC9126 --> RFC8414
  RFC9126 --> RFC9101
  OAuth2_JARM --> RFC6749
  OAuth2_JARM --> RFC7515
  OAuth2_JARM --> RFC7516
  OAuth2_JARM --> RFC7519
  OAuth2_JARM --> OAuth2_MultiResp
  OAuth2_JARM --> OAuth2_FormPost
  RFC9207 --> RFC6749
  RFC9207 --> RFC8414
  OAuth2_MixUpMit --> RFC6749
  OAuth2_MixUpMit --> RFC7519

  OAuth2_IncrAuthz --> RFC6749
  OAuth2_IncrAuthz --> RFC8414

  RFC9396 --> RFC7519
  RFC9396 --> RFC8414

  RFC9449 --> RFC6749
  RFC9449 --> RFC6750
  RFC9449 --> RFC7515
  RFC9449 --> RFC7517
  RFC9449 --> RFC7519
  RFC9449 --> RFC7638

  RFC9635 --> RFC6749
  RFC9635 --> RFC6750
  RFC9635 --> RFC7515
  RFC9635 --> RFC7517
  RFC9635 --> RFC8705

  RFC9470 --> RFC6749
  RFC9470 --> RFC6750

  OAuth2_PoPArch --> RFC6749
  OAuth2_PoPArch --> RFC7519
  OAuth2_PoPArch --> RFC7662
  OAuth2_PoPArch --> RFC7800
  OAuth2_PoPArch --> OAuth2_PoPKeyDist
  OAuth2_PoPArch --> OAuth2_SignedHTTP

  OAuth2_PoPKeyDist --> RFC6749
  OAuth2_PoPKeyDist --> RFC7515
  OAuth2_PoPKeyDist --> RFC7517
  OAuth2_PoPKeyDist --> RFC7518
  OAuth2_PoPKeyDist --> RFC7519
  OAuth2_PoPKeyDist --> RFC7800

  OAuth2_SignedHTTP --> RFC6749
  OAuth2_SignedHTTP --> RFC6750
  OAuth2_SignedHTTP --> RFC7515
  OAuth2_SignedHTTP --> RFC7519
  OAuth2_SignedHTTP --> RFC7662
  OAuth2_SignedHTTP --> OAuth2_PoPArch
  OAuth2_SignedHTTP --> OAuth2_PoPKeyDist

  RFC9200 --> RFC6749
  RFC9200 --> RFC6750
  RFC9200 --> RFC7252
  RFC9200 --> RFC7519
  RFC9200 --> RFC7662
  RFC9200 --> RFC8392
  RFC9200 --> RFC8152
  RFC9201 --> RFC6749
  RFC9201 --> RFC8705
  RFC9201 --> RFC9200
  RFC9201 --> RFC8747

  RFC9700 --> RFC6749
  RFC9700 --> RFC6750
  RFC9700 --> RFC8252
  RFC9700 --> RFC8414
  RFC9700 --> RFC8705

  OAuth2_MultiResp --> RFC6749
  OAuth2_FormPost --> RFC6749
  OAuth2_FormPost --> OAuth2_MultiResp

  OAuth2_AttestAuth --> RFC6750
  OAuth2_AttestAuth --> RFC7515
  OAuth2_AttestAuth --> RFC7519
  OAuth2_AttestAuth --> RFC7591
  OAuth2_AttestAuth --> RFC7800
  OAuth2_AttestAuth --> RFC8414
  OAuth2_AttestAuth --> RFC8725
  OAuth2_AttestAuth --> RFC9126
  OAuth2_AttestAuth --> RFC9449
  OAuth2_AttestAuth --> RFC9728

  OAuth2_BrowserApps --> RFC6749
  OAuth2_BrowserApps --> RFC6750
  OAuth2_BrowserApps --> RFC7636
  OAuth2_BrowserApps --> RFC9700

  OAuth2_JWTState --> RFC6749
  OAuth2_JWTState --> RFC7515
  OAuth2_JWTState --> RFC7519

  OAuth2_TokenBinding --> RFC6749
  OAuth2_TokenBinding --> RFC7519
  OAuth2_TokenBinding --> RFC7591
  OAuth2_TokenBinding --> RFC7662
  OAuth2_TokenBinding --> RFC8414

  UMA_Profile --> RFC6749

  OAuth2_IdentityChaining --> RFC6749
  OAuth2_IdentityChaining --> RFC7521
  OAuth2_IdentityChaining --> RFC7523
  OAuth2_IdentityChaining --> RFC8414
  OAuth2_IdentityChaining --> RFC8693
  OAuth2_IdentityChaining --> RFC8707
  OAuth2_IdentityChaining --> RFC9700
  OAuth2_IdentityChaining --> RFC9728

  OAuth2_IdentityAssertion --> RFC6749
  OAuth2_IdentityAssertion --> RFC7519
  OAuth2_IdentityAssertion --> RFC7521
  OAuth2_IdentityAssertion --> RFC7523
  OAuth2_IdentityAssertion --> RFC8414
  OAuth2_IdentityAssertion --> RFC8693
  OAuth2_IdentityAssertion --> RFC8707
  OAuth2_IdentityAssertion --> RFC8725
  OAuth2_IdentityAssertion --> RFC9396
  OAuth2_IdentityAssertion --> RFC9493
  OAuth2_IdentityAssertion --> OAuth2_IdentityChaining

  OAuth2_AIAgents --> RFC6749
  OAuth2_AIAgents --> RFC7519
  OAuth2_AIAgents --> RFC7636
  OAuth2_AIAgents --> RFC8693
  OAuth2_AIAgents --> RFC9068

  %% ---- Edges: OIDC depending on OAuth / JWT ----
  OIDC_Core --> RFC6749
  OIDC_Core --> RFC6750
  OIDC_Core --> RFC7515
  OIDC_Core --> RFC7516
  OIDC_Core --> RFC7518
  OIDC_Core --> RFC7519
  OIDC_Core --> RFC8176
  OIDC_Core --> OAuth2_MultiResp

  OIDC_Discovery --> RFC6749
  OIDC_Discovery --> RFC7033
  OIDC_Discovery --> RFC7515
  OIDC_Discovery --> RFC7517
  OIDC_Discovery --> RFC7518
  OIDC_Discovery --> RFC7519

  OIDC_Reg --> RFC6749
  OIDC_Reg --> RFC6750
  OIDC_Reg --> RFC7515
  OIDC_Reg --> RFC7516
  OIDC_Reg --> RFC7517
  OIDC_Reg --> RFC7518
  OIDC_Reg --> RFC7519
  %% RFC 7591 explicitly references OIDC Dynamic Client Registration
  RFC7591 --> OIDC_Reg

  %% ---- Edges: OIDC internal references ----
  OIDC_Core --> OIDC_Discovery
  OIDC_Core --> OIDC_Reg

  OIDC_Discovery --> OIDC_Core

  OIDC_Reg --> OIDC_Core
  OIDC_Reg --> OIDC_Discovery

  OIDC_Session --> OIDC_Core
  OIDC_Session --> OIDC_Discovery
  OIDC_Session --> OIDC_FrontLogout
  OIDC_Session --> OIDC_BackLogout
  OIDC_Session --> OIDC_RPLogout
  OIDC_Session --> RFC6749

  OIDC_FrontLogout --> OIDC_Core
  OIDC_FrontLogout --> OIDC_Discovery
  OIDC_FrontLogout --> OIDC_Reg
  OIDC_FrontLogout --> OIDC_Session
  OIDC_FrontLogout --> OIDC_BackLogout
  OIDC_FrontLogout --> OIDC_RPLogout
  OIDC_FrontLogout --> RFC6749

  OIDC_BackLogout --> OIDC_Core
  OIDC_BackLogout --> OIDC_Discovery
  OIDC_BackLogout --> OIDC_Reg
  OIDC_BackLogout --> OIDC_Session
  OIDC_BackLogout --> OIDC_FrontLogout
  OIDC_BackLogout --> OIDC_RPLogout
  OIDC_BackLogout --> RFC6749
  OIDC_BackLogout --> RFC7519

  OIDC_RPLogout --> OIDC_Core
  OIDC_RPLogout --> OIDC_Discovery
  OIDC_RPLogout --> OIDC_Reg
  OIDC_RPLogout --> OIDC_Session
  OIDC_RPLogout --> OIDC_FrontLogout
  OIDC_RPLogout --> OIDC_BackLogout
  OIDC_RPLogout --> RFC6749

  OIDC_TokenBound --> OIDC_Core
  OIDC_TokenBound --> OIDC_Discovery
  OIDC_TokenBound --> OIDC_Reg
  OIDC_TokenBound --> RFC6749
  OIDC_TokenBound --> RFC7519
  OIDC_TokenBound --> RFC7800
  OIDC_TokenBound --> RFC8414

  OIDC_IDA --> OIDC_Core
  OIDC_IDA --> OIDC_Discovery
  OIDC_IDA --> OIDC_IDA_Schema
  OIDC_IDA --> OIDC_IDA_Claims

  OIDC_IDA_Schema --> OIDC_Core
  OIDC_IDA_Schema --> RFC7519

  OIDC_IDA_Claims --> OIDC_Core
  OIDC_IDA_Claims --> OIDC_IDA
  OIDC_IDA_Claims --> RFC7519

  OIDC_UnmetAuthReq --> OIDC_Core
  OIDC_UnmetAuthReq --> RFC6749

  OIDC_PromptCreate --> OIDC_Core
  OIDC_PromptCreate --> OIDC_Discovery
  OIDC_PromptCreate --> RFC6749
  OIDC_PromptCreate --> RFC9101

  OIDC_SSF --> RFC6749
  OIDC_SSF --> RFC7519
  OIDC_SSF --> RFC8417
  OIDC_SSF --> RFC8935
  OIDC_SSF --> RFC8936
  OIDC_SSF --> RFC9493

  OIDC_CAEP --> OIDC_Core
  OIDC_CAEP --> OIDC_SSF

  OIDC_RISC_Spec --> RFC8417
  OIDC_RISC_Spec --> OIDC_SSF
  OIDC_RISC_Spec --> OIDC_CAEP

  OIDC_RISC_Profile --> RFC6749
  OIDC_RISC_Profile --> RFC6750
  OIDC_RISC_Profile --> RFC7517
  OIDC_RISC_Profile --> RFC7519
  OIDC_RISC_Profile --> RFC8414
  OIDC_RISC_Profile --> RFC8417
  OIDC_RISC_Profile --> RFC8935
  OIDC_RISC_Profile --> RFC8936
  OIDC_RISC_Profile --> OIDC_Core

  OIDC_RISC_Events --> OIDC_RISC_Profile
  OIDC_RISC_Events --> RFC8417

  OID4VCI --> RFC6749
  OID4VCI --> RFC6750
  OID4VCI --> RFC7515
  OID4VCI --> RFC7516
  OID4VCI --> RFC7517
  OID4VCI --> RFC7518
  OID4VCI --> RFC7519
  OID4VCI --> RFC7591
  OID4VCI --> RFC7636
  OID4VCI --> RFC8414
  OID4VCI --> RFC8707
  OID4VCI --> RFC8725
  OID4VCI --> RFC9126
  OID4VCI --> RFC9396
  OID4VCI --> RFC9449
  OID4VCI --> RFC9700
  OID4VCI --> OIDC_Core
  OID4VCI --> SDJWT_VC

  OID4VP --> RFC6749
  OID4VP --> RFC7515
  OID4VP --> RFC7516
  OID4VP --> RFC7518
  OID4VP --> RFC7519
  OID4VP --> RFC7591
  OID4VP --> RFC7800
  OID4VP --> RFC8414
  OID4VP --> RFC9101
  OID4VP --> RFC9207
  OID4VP --> RFC9700
  OID4VP --> OAuth2_MultiResp
  OID4VP --> OIDC_Core
  OID4VP --> SDJWT_VC
  OID4VP --> SIOPv2

  SIOPv2 --> RFC6749
  SIOPv2 --> RFC7515
  SIOPv2 --> RFC7517
  SIOPv2 --> RFC7519
  SIOPv2 --> RFC7638
  SIOPv2 --> RFC9101
  SIOPv2 --> RFC9278
  SIOPv2 --> OAuth2_MultiResp
  SIOPv2 --> OIDC_Core
  SIOPv2 --> OIDC_Discovery
  SIOPv2 --> OIDC_Reg
  SIOPv2 --> OID4VP

  %% ---- Edges: JOSE internal references ----
  RFC7515 --> RFC7518
  RFC7516 --> RFC7518
  RFC7517 --> RFC7518
  RFC7517 --> RFC7515
  RFC7517 --> RFC7516

  %% ---- Edges: JWT depending on JOSE ----
  RFC7519 --> RFC7515
  RFC7519 --> RFC7516
  RFC7519 --> RFC7518

  RFC8725 --> RFC7519
  RFC8725 --> RFC7515
  RFC8725 --> RFC7516
  RFC8725 --> RFC7518

  RFC7800 --> RFC7519
  RFC7800 --> RFC7517
  RFC7800 --> RFC7516

  RFC8176 --> RFC7519
  RFC8176 --> RFC6749
  RFC8176 --> OIDC_Core

  RFC7638 --> RFC7515
  RFC7638 --> RFC7517
  RFC7638 --> RFC7518
  RFC9278 --> RFC7638

  %% ---- Edges: newer JWT/OAuth profile referencing others ----
  RFC9068 --> RFC6749
  RFC9068 --> RFC7519
  RFC9068 --> RFC7515
  RFC9068 --> RFC7518
  RFC9068 --> RFC8414
  RFC9068 --> RFC8693
  RFC9068 --> RFC8707
  RFC9068 --> RFC8725
  RFC9068 --> OIDC_Core
  RFC9068 --> OIDC_Discovery

  RFC9728 --> RFC6749
  RFC9728 --> RFC6750
  RFC9728 --> RFC8414
  RFC9728 --> RFC7519

  RFC9901 --> RFC7519
  RFC9901 --> RFC7515
  RFC9901 --> RFC7516
  RFC9901 --> RFC7800
  RFC9901 --> RFC8725

  SDJWT_VC --> RFC9901
  SDJWT_VC --> RFC7515
  SDJWT_VC --> RFC7517
  SDJWT_VC --> RFC7519
  SDJWT_VC --> RFC7800

  %% ---- Edges: UMA depending on OAuth / JWT ----
  UMA_Grant --> RFC6749
  UMA_Grant --> RFC6750
  UMA_Grant --> RFC7591
  UMA_Grant --> RFC8414
  UMA_Grant --> UMA_FedAuthz
  UMA_FedAuthz --> RFC6749
  UMA_FedAuthz --> RFC6750
  UMA_FedAuthz --> RFC7591
  UMA_FedAuthz --> RFC7662
  UMA_FedAuthz --> RFC8414
  UMA_FedAuthz --> UMA_Grant

  %% ---- Clickable links for each node ----
  click RFC7033 "https://datatracker.ietf.org/doc/html/rfc7033" "WebFinger (RFC 7033)"

  click RFC6749 "https://datatracker.ietf.org/doc/html/rfc6749" "OAuth 2.0 Authorization Framework (RFC 6749)"
  click OAuth2_1 "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-1-15" "OAuth 2.1 Authorization Framework (Draft)"
  click RFC6750 "https://datatracker.ietf.org/doc/html/rfc6750" "Bearer Token Usage (RFC 6750)"
  click RFC6755 "https://datatracker.ietf.org/doc/html/rfc6755" "An IETF URN Sub-Namespace for OAuth (RFC 6755)"
  click RFC6819 "https://datatracker.ietf.org/doc/html/rfc6819" "OAuth 2.0 Threat Model and Security Considerations (RFC 6819)"
  click RFC7009 "https://datatracker.ietf.org/doc/html/rfc7009" "OAuth 2.0 Token Revocation (RFC 7009)"
  click RFC7521 "https://datatracker.ietf.org/doc/html/rfc7521" "Assertion Framework for OAuth 2.0 (RFC 7521)"
  click RFC7522 "https://datatracker.ietf.org/doc/html/rfc7522" "SAML 2.0 Profile for OAuth 2.0 (RFC 7522)"
  click RFC7523 "https://datatracker.ietf.org/doc/html/rfc7523" "JWT Profile for OAuth 2.0 Client Authentication and Authorization Grants (RFC 7523)"
  click OAuth2_Kerberos "https://datatracker.ietf.org/doc/html/draft-hardjono-oauth-kerberos-01" "Kerberos V5 Profile for OAuth 2.0 (Draft)"
  click RFC7636 "https://datatracker.ietf.org/doc/html/rfc7636" "PKCE for OAuth 2.0 (RFC 7636)"
  click RFC7628 "https://datatracker.ietf.org/doc/html/rfc7628" "SASL OAuth Mechanisms (RFC 7628)"
  click RFC7591 "https://datatracker.ietf.org/doc/html/rfc7591" "Dynamic Client Registration (RFC 7591)"
  click RFC7592 "https://datatracker.ietf.org/doc/html/rfc7592" "Dynamic Client Registration Management (RFC 7592)"
  click OAuth2_ClientIDMeta "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-client-id-metadata-document-00" "OAuth Client ID Metadata Document (Draft)"
  click OAuth2_ClientIDScheme "https://datatracker.ietf.org/doc/html/draft-parecki-oauth-client-id-scheme-01" "OAuth 2.0 Client ID Scheme (Draft)"
  click RFC7662 "https://datatracker.ietf.org/doc/html/rfc7662" "OAuth 2.0 Token Introspection (RFC 7662)"
  click RFC9701 "https://datatracker.ietf.org/doc/html/rfc9701" "JWT Response for OAuth Token Introspection (RFC 9701)"
  click RFC8252 "https://datatracker.ietf.org/doc/html/rfc8252" "OAuth 2.0 for Native Apps (RFC 8252)"
  click RFC8414 "https://datatracker.ietf.org/doc/html/rfc8414" "Authorization Server Metadata (RFC 8414)"
  click OAuth2_ASDiscovery "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-discovery-02" "OAuth 2.0 Authorization Server Discovery Metadata (Draft)"
  click RFC8417 "https://datatracker.ietf.org/doc/html/rfc8417" "Security Event Token (SET) (RFC 8417)"
  click RFC8628 "https://datatracker.ietf.org/doc/html/rfc8628" "OAuth 2.0 Device Authorization Grant (RFC 8628)"
  click RFC8935 "https://datatracker.ietf.org/doc/html/rfc8935" "Push-Based Security Event Token (SET) Delivery Using HTTP (RFC 8935)"
  click RFC8936 "https://datatracker.ietf.org/doc/html/rfc8936" "Poll-Based Security Event Token (SET) Delivery Using HTTP (RFC 8936)"
  click SET_StreamMgmt "https://datatracker.ietf.org/doc/html/draft-scurtescu-secevent-event-stream-mgmt-api-00" "Management API for SET Event Streams (Draft)"
  click RISC_UseCases "https://datatracker.ietf.org/doc/html/draft-scurtescu-secevent-risc-use-cases-00" "Security Events RISC Use Cases (Draft)"
  click RFC9493 "https://datatracker.ietf.org/doc/html/rfc9493" "Subject Identifiers for Security Event Tokens (RFC 9493)"
  click RFC8693 "https://datatracker.ietf.org/doc/html/rfc8693" "OAuth 2.0 Token Exchange (RFC 8693)"
  click RFC8705 "https://datatracker.ietf.org/doc/html/rfc8705" "OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens (RFC 8705)"
  click RFC8707 "https://datatracker.ietf.org/doc/html/rfc8707" "OAuth 2.0 Resource Indicators (RFC 8707)"
  click RFC9101 "https://datatracker.ietf.org/doc/html/rfc9101" "OAuth 2.0 JWT-Secured Authorization Request (JAR) (RFC 9101)"
  click RFC9126 "https://datatracker.ietf.org/doc/html/rfc9126" "OAuth 2.0 Pushed Authorization Requests (RFC 9126)"
  click OAuth2_JARM "https://openid.net/specs/oauth-v2-jarm-final.html" "JWT Secured Authorization Response Mode for OAuth 2.0 (JARM)"
  click RFC9207 "https://datatracker.ietf.org/doc/html/rfc9207" "OAuth 2.0 Authorization Server Issuer Identification (RFC 9207)"
  click OAuth2_MixUpMit "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-mix-up-mitigation-01" "OAuth 2.0 Mix-Up Mitigation (Draft)"
  click OAuth2_IncrAuthz "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-incremental-authz-04" "OAuth 2.0 Incremental Authorization (Draft)"
  click RFC9396 "https://datatracker.ietf.org/doc/html/rfc9396" "OAuth 2.0 Rich Authorization Requests (RFC 9396)"
  click RFC9449 "https://datatracker.ietf.org/doc/html/rfc9449" "OAuth 2.0 Demonstrating Proof of Possession (RFC 9449)"
  click RFC9635 "https://datatracker.ietf.org/doc/html/rfc9635" "Grant Negotiation and Authorization Protocol (GNAP) (RFC 9635)"
  click RFC9470 "https://datatracker.ietf.org/doc/html/rfc9470" "OAuth 2.0 Step Up Authentication Challenge Protocol (RFC 9470)"
  click OAuth2_PoPArch "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-pop-architecture-08" "OAuth 2.0 Proof-of-Possession (PoP) Security Architecture (Draft)"
  click OAuth2_PoPKeyDist "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-pop-key-distribution-07" "OAuth 2.0 Proof-of-Possession: Authorization Server to Client Key Distribution (Draft)"
  click OAuth2_SignedHTTP "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-signed-http-request-03" "A Method for Signing HTTP Requests for OAuth (Draft)"
  click RFC9200 "https://datatracker.ietf.org/doc/html/rfc9200" "ACE-OAuth Framework for Constrained Environments (RFC 9200)"
  click RFC9201 "https://datatracker.ietf.org/doc/html/rfc9201" "Additional OAuth Parameters for ACE (RFC 9201)"
  click RFC9700 "https://datatracker.ietf.org/doc/html/rfc9700" "OAuth 2.0 Security Best Current Practice (RFC 9700)"
  click OAuth2_MultiResp "https://openid.net/specs/oauth-v2-multiple-response-types-1_0.html" "OAuth 2.0 Multiple Response Type Encoding Practices"
  click OAuth2_FormPost "https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html" "OAuth 2.0 Form Post Response Mode"
  click OAuth2_AttestAuth "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-attestation-based-client-auth-09" "OAuth 2.0 Attestation-Based Client Authentication (Draft)"
  click OAuth2_BrowserApps "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-browser-based-apps-26" "OAuth 2.0 for Browser-Based Applications (Draft)"
  click OAuth2_JWTState "https://datatracker.ietf.org/doc/html/draft-bradley-oauth-jwt-encoded-state-09" "Encoding claims in the OAuth 2 state parameter using a JWT (Draft)"
  click OAuth2_TokenBinding "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-token-binding-08" "OAuth 2.0 Token Binding (Draft)"
  click UMA_Profile "https://datatracker.ietf.org/doc/html/draft-hardjono-oauth-umacore-14" "User-Managed Access (UMA) Profile of OAuth 2.0 (Draft)"
  click OAuth2_IdentityChaining "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-identity-chaining-16" "OAuth Identity and Authorization Chaining Across Domains (Draft)"
  click OAuth2_IdentityAssertion "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-identity-assertion-authz-grant-04" "Identity Assertion JWT Authorization Grant (Draft)"
  click OAuth2_AIAgents "https://datatracker.ietf.org/doc/html/draft-oauth-ai-agents-on-behalf-of-user-02" "OAuth 2.0 On-Behalf-Of User Authorization for AI Agents (Draft)"

  click RFC7515 "https://datatracker.ietf.org/doc/html/rfc7515" "JSON Web Signature (JWS) (RFC 7515)"
  click RFC7516 "https://datatracker.ietf.org/doc/html/rfc7516" "JSON Web Encryption (JWE) (RFC 7516)"
  click RFC7517 "https://datatracker.ietf.org/doc/html/rfc7517" "JSON Web Key (JWK) (RFC 7517)"
  click RFC7518 "https://datatracker.ietf.org/doc/html/rfc7518" "JSON Web Algorithms (JWA) (RFC 7518)"
  click RFC7519 "https://datatracker.ietf.org/doc/html/rfc7519" "JSON Web Token (JWT) (RFC 7519)"
  click RFC7800 "https://datatracker.ietf.org/doc/html/rfc7800" "Proof-of-Possession Key Semantics for JWTs (RFC 7800)"
  click RFC8176 "https://datatracker.ietf.org/doc/html/rfc8176" "Authentication Method Reference Values (RFC 8176)"
  click RFC7638 "https://datatracker.ietf.org/doc/html/rfc7638" "JSON Web Key (JWK) Thumbprint (RFC 7638)"
  click RFC8725 "https://datatracker.ietf.org/doc/html/rfc8725" "JSON Web Token Best Current Practices (RFC 8725)"
  click RFC9278 "https://datatracker.ietf.org/doc/html/rfc9278" "JWK Thumbprint URI (RFC 9278)"
  click RFC9068 "https://datatracker.ietf.org/doc/html/rfc9068" "JWT Profile for OAuth 2.0 Access Tokens (RFC 9068)"
  click RFC9728 "https://datatracker.ietf.org/doc/html/rfc9728" "OAuth 2.0 Protected Resource Metadata (RFC 9728)"
  click RFC9901 "https://datatracker.ietf.org/doc/html/rfc9901" "Selective Disclosure for JSON Web Tokens (RFC 9901)"
  click SDJWT_VC "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-sd-jwt-vc-16" "SD-JWT-based Verifiable Credentials (Draft)"

  click OIDC_Core "https://openid.net/specs/openid-connect-core-1_0.html" "OpenID Connect Core 1.0"
  click OIDC_Discovery "https://openid.net/specs/openid-connect-discovery-1_0.html" "OpenID Connect Discovery 1.0"
  click OIDC_Reg "https://openid.net/specs/openid-connect-registration-1_0.html" "OpenID Connect Dynamic Client Registration 1.0"
  click OIDC_Session "https://openid.net/specs/openid-connect-session-1_0.html" "OpenID Connect Session Management 1.0"
  click OIDC_FrontLogout "https://openid.net/specs/openid-connect-frontchannel-1_0.html" "OpenID Connect Front-Channel Logout 1.0"
  click OIDC_BackLogout "https://openid.net/specs/openid-connect-backchannel-1_0.html" "OpenID Connect Back-Channel Logout 1.0"
  click OIDC_RPLogout "https://openid.net/specs/openid-connect-rpinitiated-1_0.html" "OpenID Connect RP-Initiated Logout 1.0"
  click OIDC_TokenBound "https://openid.net/specs/openid-connect-token-bound-authentication-1_0.html" "OpenID Connect Token Bound Authentication 1.0"
  click OIDC_IDA "https://openid.net/specs/openid-connect-4-identity-assurance-1_0.html" "OpenID Connect for Identity Assurance 1.0"
  click OIDC_IDA_Schema "https://openid.net/specs/openid-ida-verified-claims-1_0-final.html" "OpenID Identity Assurance Schema Definition 1.0"
  click OIDC_IDA_Claims "https://openid.net/specs/openid-connect-4-ida-claims-1_0-final.html" "OpenID Connect for Identity Assurance Claims Registration 1.0"
  click OIDC_UnmetAuthReq "https://openid.net/specs/openid-connect-unmet-authentication-requirements-1_0.html" "OpenID Connect Core Error Code unmet_authentication_requirements"
  click OIDC_PromptCreate "https://openid.net/specs/openid-connect-prompt-create-1_0.html" "Initiating User Registration via OpenID Connect 1.0"
  click OIDC_SSF "https://openid.net/specs/openid-sharedsignals-framework-1_0.html" "OpenID Shared Signals Framework 1.0"
  click OIDC_CAEP "https://openid.net/specs/openid-caep-1_0.html" "OpenID Continuous Access Evaluation Profile 1.0"
  click OIDC_RISC_Spec "https://openid.net/specs/openid-risc-1_0-final.html" "OpenID RISC Profile Specification 1.0"
  click OIDC_RISC_Profile "https://openid.net/specs/openid-risc-profile-1_0.html" "OpenID RISC Profile of IETF Security Events 1.0"
  click OIDC_RISC_Events "https://openid.net/specs/openid-risc-event-types-1_0.html" "OpenID RISC Event Types 1.0"
  click OID4VCI "https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html" "OpenID for Verifiable Credential Issuance 1.0"
  click OID4VP "https://openid.net/specs/openid-4-verifiable-presentations-1_0.html" "OpenID for Verifiable Presentations 1.0"
  click SIOPv2 "https://openid.net/specs/openid-connect-self-issued-v2-1_0-13.html" "Self-Issued OpenID Provider v2 (Draft)"

  click UMA_Grant "https://docs.kantarainitiative.org/uma/wg/rec-oauth-uma-grant-2.0.html" "UMA 2.0 Grant for OAuth 2.0"
  click UMA_FedAuthz "https://docs.kantarainitiative.org/uma/wg/rec-oauth-uma-federated-authz-2.0.html" "UMA 2.0 Federated Authorization"
```
