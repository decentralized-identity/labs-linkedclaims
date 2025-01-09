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


## 1. Understanding LinkedClaims
### What it is
 LinkedClaims is a pattern for creating verifiable, interconnected claims in decentralized systems. It provides a foundation for building trust networks by enabling claims to be linked, verified, and trusted across different platforms and implementations. The standard requires that each claim must have its own URI identifier, must reference a subject via URI, and must be cryptographically signed. This allows claims to be connected together to form verifiable chains of trust while maintaining flexibility in implementation.
 
### Why use it
 LinkedClaims addresses the fundamental challenge of establishing trust in decentralized environments by providing a standardized way to connect and verify claims across different systems. It enables organizations to build trust networks that are interoperable, verifiable, and privacy-preserving. By supporting creation of claims about any subject, it allows for flexible trust models that can evolve over time through progressive attestation building.

### Core concepts
- **Claims**: Structured, signed documents making assertions about subjects

- **Links**: Connections between claims enabling trust chains

- **Evidence**: Supporting documentation or proof for claims

- **Verification**: Methods to validate claims and their relationships

- **URI Addressing**: Each claim is uniquely identifiable

- **Cryptographic Signatures**: Claims are signed by issuers

### Benefits
 It provides a flexible yet robust foundation for building decentralized trust systems. Its architecture enables seamless interoperability between different platforms while maintaining strong security through cryptographic verification. The system supports creating claims about any subject, making it suitable for a wide range of use cases from public attestations to private credentials. Its progressive trust building capability allows relationships to develop naturally over time through linked attestations.

### Disclaimer
  This guide serves as a practical resource for understanding and implementing LinkedClaims. Drawing from actual implementations in humanitarian aid tracking and community impact verification, we share insights and approaches that have worked in real situations.
While we offer recommendations and best practices, this document is not a technical specification. Users should view these suggestions as starting points rather than strict requirements. Every implementation is unique, and organizations should adapt these practices to their specific needs and circumstances.
We encourage readers to combine these insights with other resources, expert advice, and their own experience to create the most effective solutions for their use cases.


### Target Audience 
Developers who intend to implement the LinkedClaims specification, technical community that is committed to building a more decentralized and open web trust

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
