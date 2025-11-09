# Motivation

## The Problem: Specification Overload

When learning about or implementing OpenID Connect, OAuth 2.0, or related authentication and authorization technologies,
you quickly encounter a common challenge: **specification sprawl**.

### The Tab Explosion

Here's what typically happens:

1. You start reading the [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html) specification
2. It references [OAuth 2.0 (RFC 6749)](https://datatracker.ietf.org/doc/html/rfc6749), so you open that in a new tab
3. OAuth 2.0 mentions [Bearer Tokens (RFC 6750)](https://datatracker.ietf.org/doc/html/rfc6750), so you open another tab
4. OpenID Connect also references [JWT (RFC 7519)](https://datatracker.ietf.org/doc/html/rfc7519), so that's another tab
5. JWT depends on [JWS (RFC 7515)](https://datatracker.ietf.org/doc/html/rfc7515),
   [JWE (RFC 7516)](https://datatracker.ietf.org/doc/html/rfc7516), and
   [JWK (RFC 7517)](https://datatracker.ietf.org/doc/html/rfc7517)...
6. Before you know it, you have 10+ tabs open and you've lost track of:
   - Which specifications you still need to read
   - How they all relate to each other
   - Which ones are fundamental vs. optional extensions
   - Where to start and what order to read them in

### The Mental Load

Even experienced developers struggle with:

- **Understanding dependencies**: Which specs build on which foundations?
- **Finding the right spec**: Need to implement PKCE? Where does that fit in?
- **Avoiding missing pieces**: Did you consider all the relevant specifications for your use case?
- **Teaching others**: How do you explain this ecosystem to a colleague or team member?

## The Solution: Visual Specification Mapping

This project exists to solve these problems by providing a **visual dependency graph** that shows:

1. **All major specifications** in the OAuth/OpenID Connect ecosystem
2. **Their relationships** - which specs depend on or reference others
3. **Logical groupings** - OAuth foundation, JOSE/JWT security, OpenID Connect layer, etc.
4. **Direct links** - click any node to jump straight to the official specification

## Who This Helps

### Developers

- **Learning**: Understand the authentication/authorization landscape before diving deep
- **Implementation planning**: Identify which specifications you need for your use case
- **Debugging**: When something goes wrong, trace through the relevant specs systematically

### Security Architects

- **Design decisions**: See the full picture when choosing which standards to support
- **Gap analysis**: Ensure you haven't missed important related specifications
- **Documentation**: Use the graph as a reference when documenting your architecture

### Students and Educators

- **Teaching tool**: Show the relationships between specifications visually
- **Study guide**: Know which specs to read and in what order
- **Context building**: Understand how modern web authentication evolved

### Technical Writers

- **Accuracy**: Reference the correct specifications when documenting authentication flows
- **Completeness**: Ensure all relevant standards are mentioned
- **Clarity**: Help readers understand how different specs work together

## How It Works

Instead of getting lost in a maze of specification tabs, you can:

1. **Start with the graph** to see the big picture
2. **Identify your path** based on what you're trying to accomplish
3. **Follow dependencies** to understand what foundational knowledge you need
4. **Click through** to the official specs when you're ready to read the details

## Example Use Cases

### "I need to implement OpenID Connect"

Look at the graph and see that you'll need to understand:

- OAuth 2.0 (RFC 6749) - the foundation
- JWT (RFC 7519) - for identity tokens
- OpenID Connect Discovery - for provider configuration
- Possibly PKCE (RFC 7636) - for mobile/SPA security

### "I'm seeing JWT mentioned everywhere"

The graph shows you that JWT:

- Builds on JWS, JWE, JWK, and JWA (the JOSE specs)
- Is used by OpenID Connect for ID tokens
- Is used by RFC 9068 for OAuth access tokens
- Is used by RFC 7523 for client authentication

### "What's the difference between RFC 7522 and RFC 7523?"

The graph shows both build on RFC 7521 (the assertion framework),
with 7522 being the SAML profile and 7523 being the JWT profile.

## Beyond Tab Management

This project isn't just about avoiding browser tab chaos - it's about **building mental models**.
By seeing how specifications relate to each other visually, you develop a better understanding of:

- The **layered architecture** of modern authentication
- The **evolution** of standards (newer specs build on older foundations)
- The **modularity** of the ecosystem (pick the pieces you need)
- The **interconnected nature** of web security standards

## Contributing to Understanding

If you've found this helpful, consider contributing by:

- Suggesting additional specifications to include
- Identifying missing or incorrect dependencies
- Sharing how you've used this in your learning or teaching

The goal is to make the complex world of authentication and authorization specifications more accessible to everyone.

---

**Bottom line**: This project exists because understanding OAuth, OpenID Connect, and related specifications shouldn't
require a PhD in browser tab management. Sometimes the best way to understand complexity is to visualize it.
