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
    OIDC_IDA["OpenID Connect for Identity Assurance 1.0"]
    OIDC_SSF["OpenID Shared Signals Framework 1.0"]
    OIDC_RISC_Profile["OpenID RISC Profile of IETF Security Events 1.0"]
    OIDC_RISC_Events["OpenID RISC Event Types 1.0"]
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
    RFC7636["PKCE for OAuth 2.0 (RFC 7636)"]
    RFC7009["OAuth 2.0 Token Revocation (RFC 7009)"]
    RFC7591["Dynamic Client Registration (RFC 7591)"]
    RFC7592["Dynamic Client Registration Management (RFC 7592)"]
    OAuth2_ClientIDMeta["OAuth Client ID Metadata Document (Draft)"]
    RFC7662["OAuth 2.0 Token Introspection (RFC 7662)"]
    RFC8252["OAuth 2.0 for Native Apps (RFC 8252)"]
    RFC8414["Authorization Server Metadata (RFC 8414)"]
    OAuth2_ASDiscovery["OAuth 2.0 Authorization Server Discovery Metadata (Draft)"]
    RFC8417["Security Event Token (SET) (RFC 8417)"]
    RFC8628["OAuth 2.0 Device Authorization Grant (RFC 8628)"]
    RFC8935["Push-Based Security Event Token (SET) Delivery Using HTTP (RFC 8935)"]
    RFC8936["Poll-Based Security Event Token (SET) Delivery Using HTTP (RFC 8936)"]
    SET_StreamMgmt["Management API for SET Event Streams"]
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
    RFC9700["OAuth 2.0 Security Best Current Practice (RFC 9700)"]
    OAuth2_MultiResp["OAuth 2.0 Multiple Response Type Encoding Practices"]
    OAuth2_FormPost["OAuth 2.0 Form Post Response Mode"]
    OAuth2_AttestAuth["OAuth 2.0 Attestation-Based Client Authentication (Draft)"]
    OAuth2_BrowserApps["OAuth 2.0 for Browser-Based Applications (Draft)"]
    OAuth2_JWTState["Encoding claims in the OAuth 2 state parameter using a JWT (Draft)"]
    UMA_Profile["User-Managed Access (UMA) Profile of OAuth 2.0 (Draft)"]
  end

  %% --- JOSE / JWT ---
  subgraph JOSE_JWT
    RFC7515["JSON Web Signature (JWS) (RFC 7515)"]
    RFC7516["JSON Web Encryption (JWE) (RFC 7516)"]
    RFC7517["JSON Web Key (JWK) (RFC 7517)"]
    RFC7518["JSON Web Algorithms (JWA) (RFC 7518)"]
    RFC7519["JSON Web Token (JWT) (RFC 7519)"]
    RFC8725["JSON Web Token Best Current Practices (RFC 8725)"]
    RFC9068["JWT Profile for OAuth 2.0 Access Tokens (RFC 9068)"]
    RFC9728["JWT Profile for OAuth 2.0 Authorization Server Issuer Identification (RFC 9728)"]
  end

  %% --- Discovery / Metadata ---
  subgraph Discovery_Metadata
    RFC7033["WebFinger (RFC 7033)"]
  end

  %% --- UMA (User-Managed Access) ---
  subgraph UMA
    UMA_Grant["UMA 2.0 Grant for OAuth 2.0"]
    UMA_FedAuthz["UMA 2.0 Federated Authorization"]
  end

  %% ---- Edges: OAuth 2.0 internal references ----
  OAuth2_1 --> RFC6749
  OAuth2_1 --> RFC7636
  OAuth2_1 --> RFC8252
  RFC6750 --> RFC6749
  RFC6755 --> RFC6749
  RFC6819 --> RFC6749
  RFC6819 --> RFC6750
  RFC7009 --> RFC6749
  RFC7521 --> RFC6749
  RFC7522 --> RFC7521
  RFC7523 --> RFC7521
  RFC7523 --> RFC7519
  RFC7636 --> RFC6749
  RFC7591 --> RFC6749
  RFC7592 --> RFC7591
  OAuth2_ClientIDMeta --> RFC6749
  OAuth2_ClientIDMeta --> RFC7591
  RFC7662 --> RFC6749
  RFC7662 --> RFC6750
  RFC8252 --> RFC6749
  RFC8252 --> RFC7636
  RFC8414 --> RFC6749
  RFC8414 --> RFC7591
  OAuth2_ASDiscovery --> RFC8414
  RFC8417 --> RFC7519
  RFC8628 --> RFC6749
  RFC8935 --> RFC8417
  RFC8936 --> RFC8417
  RFC9493 --> RFC7519
  RFC9493 --> RFC8417
  SET_StreamMgmt --> RFC8417
  SET_StreamMgmt --> RFC8935
  SET_StreamMgmt --> RFC8936
  RFC8693 --> RFC6749
  RFC8693 --> RFC6750
  RFC8705 --> RFC6749
  RFC8705 --> RFC6750
  RFC8707 --> RFC6749
  RFC9101 --> RFC6749
  RFC9101 --> RFC7519
  RFC9126 --> RFC6749
  OAuth2_JARM --> RFC6749
  OAuth2_JARM --> RFC7519
  RFC9207 --> RFC6749
  OAuth2_MixUpMit --> RFC6749
  OAuth2_IncrAuthz --> RFC6749
  RFC9396 --> RFC6749
  RFC9449 --> RFC6749
  RFC9635 --> RFC6749
  RFC9449 --> RFC7519
  RFC9470 --> RFC6749
  RFC9470 --> RFC6750
  OAuth2_PoPArch --> RFC6749
  OAuth2_PoPKeyDist --> RFC6749
  OAuth2_PoPKeyDist --> RFC7519
  OAuth2_SignedHTTP --> RFC6749
  OAuth2_SignedHTTP --> RFC7519
  RFC9700 --> RFC6749
  RFC9700 --> RFC6750
  OAuth2_MultiResp --> RFC6749
  OAuth2_FormPost --> RFC6749
  OAuth2_AttestAuth --> RFC6749
  OAuth2_AttestAuth --> RFC7519
  OAuth2_BrowserApps --> RFC6749
  OAuth2_BrowserApps --> RFC7636
  OAuth2_JWTState --> RFC6749
  OAuth2_JWTState --> RFC7519
  UMA_Profile --> RFC6749
  UMA_Profile --> RFC6750

  %% ---- Edges: OIDC depending on OAuth / JWT ----
  OIDC_Core --> RFC6749
  OIDC_Core --> RFC7519

  OIDC_Discovery --> RFC6749
  OIDC_Discovery --> RFC8414
  OIDC_Discovery --> RFC7033

  OIDC_Reg --> RFC6749
  %% RFC 7591 explicitly references OIDC Dynamic Client Registration
  RFC7591 --> OIDC_Reg

  %% ---- Edges: OIDC internal references ----
  OIDC_Core --> OIDC_Discovery
  OIDC_Core --> OIDC_Reg
  OIDC_Session --> OIDC_Core
  OIDC_FrontLogout --> OIDC_Core
  OIDC_FrontLogout --> OIDC_Session
  OIDC_BackLogout --> OIDC_Core
  OIDC_BackLogout --> OIDC_Session
  OIDC_RPLogout --> OIDC_Core
  OIDC_RPLogout --> OIDC_Session
  OIDC_IDA --> OIDC_Core
  OIDC_SSF --> RFC8417
  OIDC_SSF --> OIDC_Core
  OIDC_RISC_Profile --> RFC8417
  OIDC_RISC_Profile --> RFC8935
  OIDC_RISC_Profile --> RFC8936
  OIDC_RISC_Events --> OIDC_RISC_Profile

  %% ---- Edges: JOSE internal references ----
  RFC7515 --> RFC7518
  RFC7516 --> RFC7518
  RFC7517 --> RFC7518
  RFC7517 --> RFC7515
  RFC7517 --> RFC7516

  %% ---- Edges: JWT depending on JOSE ----
  RFC7519 --> RFC7515
  RFC7519 --> RFC7516
  RFC7519 --> RFC7517
  RFC7519 --> RFC7518

  RFC8725 --> RFC7519
  RFC8725 --> RFC7515
  RFC8725 --> RFC7516

  %% ---- Edges: newer JWT/OAuth profile referencing others ----
  RFC9068 --> RFC6749
  RFC9068 --> RFC6750
  RFC9068 --> RFC7519
  RFC9068 --> OIDC_Core
  RFC9068 --> OIDC_Discovery

  RFC9728 --> RFC6749
  RFC9728 --> RFC8414
  RFC9728 --> RFC7519

  %% ---- Edges: UMA depending on OAuth / JWT ----
  UMA_Grant --> RFC6749
  UMA_Grant --> RFC6750
  UMA_FedAuthz --> RFC6749
  UMA_FedAuthz --> RFC6750
  UMA_FedAuthz --> UMA_Grant

  %% ---- Clickable links for each node ----
  click RFC7033 "https://datatracker.ietf.org/doc/html/rfc7033" "WebFinger (RFC 7033)"

  click RFC6749 "https://datatracker.ietf.org/doc/html/rfc6749" "OAuth 2.0 Authorization Framework (RFC 6749)"
  click OAuth2_1 "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-1" "OAuth 2.1 Authorization Framework (Draft)"
  click RFC6750 "https://datatracker.ietf.org/doc/html/rfc6750" "Bearer Token Usage (RFC 6750)"
  click RFC6755 "https://datatracker.ietf.org/doc/html/rfc6755" "An IETF URN Sub-Namespace for OAuth (RFC 6755)"
  click RFC6819 "https://datatracker.ietf.org/doc/html/rfc6819" "OAuth 2.0 Threat Model and Security Considerations (RFC 6819)"
  click RFC7009 "https://datatracker.ietf.org/doc/html/rfc7009" "OAuth 2.0 Token Revocation (RFC 7009)"
  click RFC7521 "https://datatracker.ietf.org/doc/html/rfc7521" "Assertion Framework for OAuth 2.0 (RFC 7521)"
  click RFC7522 "https://datatracker.ietf.org/doc/html/rfc7522" "SAML 2.0 Profile for OAuth 2.0 (RFC 7522)"
  click RFC7523 "https://datatracker.ietf.org/doc/html/rfc7523" "JWT Profile for OAuth 2.0 Client Authentication and Authorization Grants (RFC 7523)"
  click RFC7636 "https://datatracker.ietf.org/doc/html/rfc7636" "PKCE (RFC 7636)"
  click RFC7591 "https://datatracker.ietf.org/doc/html/rfc7591" "Dynamic Client Registration (RFC 7591)"
  click RFC7592 "https://datatracker.ietf.org/doc/html/rfc7592" "Dynamic Client Registration Management (RFC 7592)"
  click OAuth2_ClientIDMeta "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-client-id-metadata-document-00" "OAuth Client ID Metadata Document (Draft)"
  click RFC7662 "https://datatracker.ietf.org/doc/html/rfc7662" "OAuth 2.0 Token Introspection (RFC 7662)"
  click RFC8252 "https://datatracker.ietf.org/doc/html/rfc8252" "OAuth 2.0 for Native Apps (RFC 8252)"
  click RFC8414 "https://datatracker.ietf.org/doc/html/rfc8414" "Authorization Server Metadata (RFC 8414)"
  click OAuth2_ASDiscovery "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-discovery-02" "OAuth 2.0 Authorization Server Discovery Metadata (Draft)"
  click RFC8417 "https://datatracker.ietf.org/doc/html/rfc8417" "Security Event Token (SET) (RFC 8417)"
  click RFC8628 "https://datatracker.ietf.org/doc/html/rfc8628" "OAuth 2.0 Device Authorization Grant (RFC 8628)"
  click RFC8935 "https://datatracker.ietf.org/doc/html/rfc8935" "Push-Based Security Event Token (SET) Delivery Using HTTP (RFC 8935)"
  click RFC8936 "https://datatracker.ietf.org/doc/html/rfc8936" "Poll-Based Security Event Token (SET) Delivery Using HTTP (RFC 8936)"
  click SET_StreamMgmt "https://datatracker.ietf.org/doc/html/draft-scurtescu-secevent-simple-control-plane" "Management API for SET Event Streams (Draft)"
  click RFC9493 "https://datatracker.ietf.org/doc/html/rfc9493" "Subject Identifiers for Security Event Tokens (RFC 9493)"
  click RFC8693 "https://datatracker.ietf.org/doc/html/rfc8693" "OAuth 2.0 Token Exchange (RFC 8693)"
  click RFC8705 "https://datatracker.ietf.org/doc/html/rfc8705" "OAuth 2.0 Mutual-TLS Client Authentication and Certificate-Bound Access Tokens (RFC 8705)"
  click RFC8707 "https://datatracker.ietf.org/doc/html/rfc8707" "OAuth 2.0 Resource Indicators (RFC 8707)"
  click RFC9101 "https://datatracker.ietf.org/doc/html/rfc9101" "OAuth 2.0 JWT-Secured Authorization Request (JAR) (RFC 9101)"
  click RFC9126 "https://datatracker.ietf.org/doc/html/rfc9126" "OAuth 2.0 Pushed Authorization Requests (RFC 9126)"
  click OAuth2_JARM "https://openid.net/specs/oauth-v2-jarm-final.html" "JWT Secured Authorization Response Mode for OAuth 2.0 (JARM)"
  click RFC9207 "https://datatracker.ietf.org/doc/html/rfc9207" "OAuth 2.0 Authorization Server Issuer Identification (RFC 9207)"
  click OAuth2_MixUpMit "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-mix-up-mitigation-01" "OAuth 2.0 Mix-Up Mitigation (Draft)"
  click OAuth2_IncrAuthz "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-incremental-authz" "OAuth 2.0 Incremental Authorization (Draft)"
  click RFC9396 "https://datatracker.ietf.org/doc/html/rfc9396" "OAuth 2.0 Rich Authorization Requests (RFC 9396)"
  click RFC9449 "https://datatracker.ietf.org/doc/html/rfc9449" "OAuth 2.0 Demonstrating Proof of Possession (RFC 9449)"
  click RFC9635 "https://datatracker.ietf.org/doc/html/rfc9635" "Grant Negotiation and Authorization Protocol (GNAP) (RFC 9635)"
  click RFC9470 "https://datatracker.ietf.org/doc/html/rfc9470" "OAuth 2.0 Step Up Authentication Challenge Protocol (RFC 9470)"
  click OAuth2_PoPArch "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-pop-architecture-08" "OAuth 2.0 Proof-of-Possession (PoP) Security Architecture (Draft)"
  click OAuth2_PoPKeyDist "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-pop-key-distribution-02" "OAuth 2.0 Proof-of-Possession: Authorization Server to Client Key Distribution (Draft)"
  click OAuth2_SignedHTTP "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-signed-http-request-03" "A Method for Signing HTTP Requests for OAuth (Draft)"
  click RFC9700 "https://datatracker.ietf.org/doc/html/rfc9700" "OAuth 2.0 Security Best Current Practice (RFC 9700)"
  click OAuth2_MultiResp "https://openid.net/specs/oauth-v2-multiple-response-types-1_0.html" "OAuth 2.0 Multiple Response Type Encoding Practices"
  click OAuth2_FormPost "https://openid.net/specs/oauth-v2-form-post-response-mode-1_0.html" "OAuth 2.0 Form Post Response Mode"
  click OAuth2_AttestAuth "https://datatracker.ietf.org/doc/draft-ietf-oauth-attestation-based-client-auth/" "OAuth 2.0 Attestation-Based Client Authentication (Draft)"
  click OAuth2_BrowserApps "https://datatracker.ietf.org/doc/html/draft-ietf-oauth-browser-based-apps" "OAuth 2.0 for Browser-Based Applications (Draft)"
  click OAuth2_JWTState "https://datatracker.ietf.org/doc/draft-bradley-oauth-jwt-encoded-state/" "Encoding claims in the OAuth 2 state parameter using a JWT (Draft)"
  click UMA_Profile "https://datatracker.ietf.org/doc/html/draft-hardjono-oauth-umacore-14" "User-Managed Access (UMA) Profile of OAuth 2.0 (Draft)"

  click RFC7515 "https://datatracker.ietf.org/doc/html/rfc7515" "JSON Web Signature (JWS) (RFC 7515)"
  click RFC7516 "https://datatracker.ietf.org/doc/html/rfc7516" "JSON Web Encryption (JWE) (RFC 7516)"
  click RFC7517 "https://datatracker.ietf.org/doc/html/rfc7517" "JSON Web Key (JWK) (RFC 7517)"
  click RFC7518 "https://datatracker.ietf.org/doc/html/rfc7518" "JSON Web Algorithms (JWA) (RFC 7518)"
  click RFC7519 "https://datatracker.ietf.org/doc/html/rfc7519" "JSON Web Token (JWT) (RFC 7519)"
  click RFC8725 "https://datatracker.ietf.org/doc/html/rfc8725" "JSON Web Token Best Current Practices (RFC 8725)"
  click RFC9068 "https://datatracker.ietf.org/doc/html/rfc9068" "JWT Profile for OAuth 2.0 Access Tokens (RFC 9068)"
  click RFC9728 "https://datatracker.ietf.org/doc/html/rfc9728" "JWT Profile for OAuth 2.0 Authorization Server Issuer Identification (RFC 9728)"

  click OIDC_Core "https://openid.net/specs/openid-connect-core-1_0.html" "OpenID Connect Core 1.0"
  click OIDC_Discovery "https://openid.net/specs/openid-connect-discovery-1_0.html" "OpenID Connect Discovery 1.0"
  click OIDC_Reg "https://openid.net/specs/openid-connect-registration-1_0.html" "OpenID Connect Dynamic Client Registration 1.0"
  click OIDC_Session "https://openid.net/specs/openid-connect-session-1_0.html" "OpenID Connect Session Management 1.0"
  click OIDC_FrontLogout "https://openid.net/specs/openid-connect-frontchannel-1_0.html" "OpenID Connect Front-Channel Logout 1.0"
  click OIDC_BackLogout "https://openid.net/specs/openid-connect-backchannel-1_0.html" "OpenID Connect Back-Channel Logout 1.0"
  click OIDC_RPLogout "https://openid.net/specs/openid-connect-rpinitiated-1_0.html" "OpenID Connect RP-Initiated Logout 1.0"
  click OIDC_IDA "https://openid.net/specs/openid-connect-4-identity-assurance-1_0.html" "OpenID Connect for Identity Assurance 1.0"
  click OIDC_SSF "https://openid.net/specs/openid-sharedsignals-framework-1_0.html" "OpenID Shared Signals Framework 1.0"
  click OIDC_RISC_Profile "https://openid.net/specs/openid-risc-profile-1_0.html" "OpenID RISC Profile of IETF Security Events 1.0"
  click OIDC_RISC_Events "https://openid.net/specs/openid-risc-event-types-1_0.html" "OpenID RISC Event Types 1.0"

  click UMA_Grant "https://docs.kantarainitiative.org/uma/wg/rec-oauth-uma-grant-2.0.html" "UMA 2.0 Grant for OAuth 2.0"
  click UMA_FedAuthz "https://docs.kantarainitiative.org/uma/wg/rec-oauth-uma-federated-authz-2.0.html" "UMA 2.0 Federated Authorization"
```
