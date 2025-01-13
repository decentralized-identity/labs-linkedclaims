# LinkedClaims Companion Guide

**Status**: Draft

### Chairs
- Golda Velez
- Phil Long

### Authors
- Agnes Koinange
- Golda Velez

### Contributors
- Agnes Koinange
- Golda Velez
  
### Github


## 1. Getting Started
### Introduction
 This companion guide serves as a practical resource for implementing the LinkedClaims pattern. While the LinkedClaims specification defines the requirements for creating verifiable, interconnected claims, this guide provides implementation guidance, best practices, and real-world examples. It helps developers and users to understand how to create and use claims that meet the core requirements: having a URI identifier, referencing a subject via URI, and including cryptographic signatures. While the formal specification defines the technical requirements for LinkedClaims, this guide shows you how to put those requirements into practice in real-world systems. Through examples and practical advice, this guide demonstrates how to implement these requirements and build trust networks across different platforms.

 Throughout the decentralized identity and web of trust ecosystem, various projects have developed ways to connect and verify claims. Some, like attest.sh and Trustgraph.net (see [Related Projects](#4-related-existing-projects)), already implement key aspects of what we define as LinkedClaims. Others may fulfill the minimum requirements while implementing additional features. This guide helps you understand these existing implementations and how to work with or create systems that follow the LinkedClaims pattern.

 LinkedClaims iteslf  is a pattern for creating verifiable, interconnected claims in decentralized systems. It provides a foundation for building trust networks by enabling claims to be linked, verified, and trusted across different platforms and implementations. The standard requires that each claim must have its own URI identifier, must reference a subject via URI, and must be cryptographically signed. This allows claims to be connected together to form verifiable chains of trust while maintaining flexibility in implementation.

 Our goal is to help you move from understanding what LinkedClaims requires to knowing how to fulfill those requirements effectively in your own systems. Whether you're building a new implementation, integrating with existing ones or using LinkedClaims, this guide will provide the practical insights you need.
 
### Importance
  This companion guide helps you navigate the implementation and use of LinkedClaims in practical settings. Whether you're new to LinkedClaims or looking to better understand existing implementations, this guide provides clear explanations, real-world examples, and best practices from existing projects.

 LinkedClaims addresses the fundamental challenge of establishing trust in decentralized environments by providing a standardized way to connect and verify claims across different systems. It enables organizations to build trust networks that are interoperable, verifiable, and privacy-preserving. By supporting creation of claims about any subject, it allows for flexible trust models that can evolve over time through progressive attestation building.

 Through this guide, you'll find solutions to common challenges, guidance for different use cases, and practical insights drawn from real implementations. Our goal is to bridge the gap between the formal specification and practical application, helping you understand not just what LinkedClaims is, but how to effectively use it in your own context.

### Core concepts
- **Claims**: Structured, signed documents making assertions about subjects

- **Links**: Connections between claims enabling trust chains

- **Evidence**: Supporting documentation or proof for claims

- **Verification**: Methods to validate claims and their relationships

- **URI Addressing**: Each claim is uniquely identifiable

- **Cryptographic Signatures**: Claims are signed by issuers

### Disclaimer
  This guide serves as a practical resource for understanding and implementing LinkedClaims. Drawing from actual implementations in humanitarian aid tracking and community impact verification, we share insights and approaches that have worked in real situations.
While we offer recommendations and best practices, this document is not a technical specification. Users should view these suggestions as starting points rather than strict requirements. Every implementation is unique, and organizations should adapt these practices to their specific needs and circumstances.
We encourage readers to combine these insights with other resources, expert advice, and their own experience to create the most effective solutions for their use cases.


### Target Audience 
Developers who intend to implement the LinkedClaims specification, technical community that is committed to building a more decentralized and open web trust

### Guide Structure

## 2.Technology Comparison
Will show where LinkedClaims fits, help in decision-making, clarifiy unique value proposition and demonstrates key differentiators


## 3.  Real-World Examples
- Humanitarian aid tracking
- Community impact verification
- OpenCreds skills attestations and verifications

## 4. Related Existing Projects

| Project | Type | Implementation | Vocabulary | Pattern Match | Links |
|---------|------|----------------|------------|---------------|---------------------|
| attest.sh | Blockchain Attestation | Ethereum | Schema.org + Custom | On-chain attestations with evidence linking |  |
| Trustgraph.net | Graph Database | Neo4j | Atoms | Trust network with linked claims | [Trustgraph.net](https://trustgraph.net/) |
| Issuer Registries | Registry | Various | W3C VC | Issuer verification chains | [Issuer Registries](https://credentialengine.org/resources/issuer-registries-establishing-trust-privacy-and-efficiency-in-verifying-credential-issuers/) |
| Proof of Humanity | Identity Verification | Ethereum | Custom | Human verification with vouching chains | [PoH](https://proofofhumanity.id) |
| Krebit | Social Verification | IPFS/Ceramic | JSON-LD | Verifiable experience claims | [Krebit](https://krebit.id/) |
| Orange Protocol | Trust Framework | Graph Protocol | Trust Schema | Reputation attestations | [Docs](https://www.orangeprotocol.io/) |


## 5. Implementation Guide
Best practices
- Claim Construction approach
- Evidence Integration methods
- Trust Relationships building
- Verification Systems usageand evidence chains


## 6. Practical Considerations
- Scaling solutions 
- Security practices 
- Common challenges 
- Solutions 


## 7. Q&A
- How does LinkedClaims differ from VCs?
- When should I use LinkedClaims vs other solutions?
- How do I handle private claims?
- What are the storage requirements?


## 8. Reference Implementations
- OpenCreds implementation-https://opencreds.net/
- Other- community implementations
- Example code repositories
