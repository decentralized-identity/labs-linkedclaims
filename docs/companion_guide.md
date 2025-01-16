# LinkedClaims Companion Guide

**Status**: Draft

### Chairs
- Golda Velez
- Phil Long

### Authors
- Agnes Koinange
- Golda Velez
- Orjiene Kenechukwu

### Contributors
- Agnes Koinange
- Golda Velez
- Orjiene Kenechukwu
  
### Github


## 1. Getting Started
### Introduction
 This companion guide serves as a practical resource for implementing the LinkedClaims pattern. While the LinkedClaims specification defines the requirements for creating verifiable, interconnected claims, this guide provides implementation guidance, best practices, and real-world examples. It helps developers and users to understand how to create and use claims that meet the core requirements: having a URI identifier, referencing a subject via URI, and including cryptographic signatures. While the formal specification defines the technical requirements for LinkedClaims, this guide shows you how to put those requirements into practice in real-world systems. Through examples and practical advice, this guide demonstrates how to implement these requirements and build trust networks across different platforms.

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
| **attest.sh** | Blockchain Attestation | Ethereum | Schema.org + Custom | On-chain attestations with evidence linking | [attest.sh](https://attest.org/) |
| Trustgraph.net | Graph Database | Neo4j | Atoms | Trust network with linked claims | [Trustgraph.net](https://trustgraph.net/) |
| **Issuer Registries** | Registry | Various | W3C VC | Issuer verification chains | [Issuer Registries](https://credentialengine.org/resources/issuer-registries-establishing-trust-privacy-and-efficiency-in-verifying-credential-issuers/) |
| **Proof of Humanity** | Identity Verification | Ethereum | Custom | Human verification with vouching chains | [PoH](https://proofofhumanity.id) |
| **Krebit** | Social Verification | IPFS/Ceramic | JSON-LD | Verifiable experience claims | [Krebit](https://krebit.id/) |
| **Orange Protocol** | Trust Framework | Graph Protocol | Trust Schema | Reputation attestations | [Docs](https://www.orangeprotocol.io/) |
| **uPort**           | Self-Sovereign Identity | Ethereum               | JSON-LD, W3C VC            | Identity claims with cryptographic verification        | [uPort](https://www.uport.me/)     |
| **DIDComm**         | Secure Communication   | Aries Framework         | JSON-LD, DID Documents     | Peer-to-peer verifiable claims exchange                | [DIDComm](https://didcomm.org/)    |
| **Veramo**          | Verifiable Credential  | Node.js Framework       | JSON-LD, W3C VC            | Decentralized identity and verifiable credential APIs  | [Veramo](https://veramo.io/)       |
| **Ceramic**         | Decentralized Data Streams | IPFS/Ceramic          | JSON-LD, IDX Protocol      | Linked, updateable claims with decentralized storage   | [Ceramic](https://ceramic.network/) |
| **BrightID**        | Decentralized Identity | Custom                  | Custom                     | Proof of uniqueness for trust building                 | [BrightID](https://brightid.org/)  |
| **Serto**           | Decentralized Identity | JSON-LD, W3C VC         | W3C Verifiable Credentials | Linked claims for interoperable identity               | [Serto](https://www.serto.id/)     |
| **Clerk**           | Authentication Platform | REST APIs, SDKs         | OAuth, OpenID Connect      | User authentication and management flows                    | [Clerk](https://clerk.dev/)        |


---

## 5. Implementation Guide

### **Best Practices for Implementing LinkedClaims**

#### **1. Claim Construction Approach**
Creating meaningful and verifiable claims is the foundation of LinkedClaims. The provided input schema provides **one example** of how to structure claims, which ensures consistency and facilitates the verification process.

- **Example Schema**: This schema represents a robust approach to structuring claims:
  ```json
  {
    "stars": 0,
    "amt": 0,
    "confidence": 0.8,
    "name": "string",
    "subject": "string",
    "statement": "string",
    "sourceURI": "string",
    "howKnown": "FIRST_HAND",
    "effectiveDate": "2025-01-13T17:04:02.864Z",
    "claimAddress": "string",
    "aspect": "string",
    "images": [
      {
        "metadata": {
          "captian": "string",
          "description": "string"
        },
        "effectiveDate": "2025-01-13T17:04:02.864Z",
        "digestMultibase": "string"
      }
    ],
    "claim": "string",
    "object": "string"
  }
  ```

> **Note**: While this schema is effective for certain use cases, other valid approaches to structuring LinkedClaims may exist.

- **Fields Explanation**:
  - **Core Data**:
    - `name`: Name of the claim.
    - `statement`: Description or assertion made by the claim.
    - `subject`: The entity or object the claim is about.
    - `aspect`: A specific dimension of the subject being asserted (e.g., "skill" or "identity").
  - **Verification and Source**:
    - `sourceURI`: A URI to a resource or evidence supporting the claim.
    - `howKnown`: The method or relationship through which the claim is known (e.g., "FIRST_HAND").
    - `effectiveDate`: When the claim takes effect.
  - **Scoring and Confidence**:
    - `stars`: A user-provided rating for the claim.
    - `confidence`: The confidence level associated with the claim.
    - `amt`: A quantifiable measure tied to the claim (e.g., transaction amount).
  - **Images**:
    - Use the `images` array to include multimedia evidence, with fields for metadata, effective date, and cryptographic digests (`digestMultibase`).
  - **Object Relationship**:
    - `claimAddress` and `object` link the claim to specific identifiers or objects for additional context.

---

#### **2. Evidence Integration Methods**
Proper integration of evidence strengthens the credibility and authenticity of claims.

- **Images as Evidence**: Include multimedia elements in the `images` array:
  - **Metadata**: Use `captian` and `description` fields to describe the image's context.
  - **Cryptographic Integrity**: Ensure the integrity of the image using `digestMultibase` to store a cryptographic digest of the file.
  - **Effective Date**: Timestamp the evidence with the `effectiveDate` field to track when it became relevant.
- **Source Attribution**: Add a `sourceURI` for external references or evidence. Ensure the URI is accessible and verifiable.

---

#### **3. Trust Relationship Building**
Establishing trust relationships helps create a web of interconnected claims, enhancing the system’s reliability.

- **Progressive Validation**:
  - Use the `confidence` field to stake the credibility of the issuer on the claim. This reflects how much confidence the issuer has in the claim’s accuracy, enabling flexibility when incorporating claims from external sources.
  - Use `stars` for user-generated feedback and ratings, distinct from the issuer's confidence level.
- **Aspect Categorization**: Use the `aspect` field to group claims into specific categories or domains for better trust assessment.
- **Linked Evidence**: Build strong associations between claims using `claimAddress` and `object` fields.

---

#### **4. Verification Systems Usage and Evidence Chains**
Verification systems provide the foundation for independently validating claims.

- **Cryptographic Proofs**:
  - Use `digestMultibase` for images to ensure the content’s integrity.
  - Validate external resources using `sourceURI`.
- **Reproducible Evidence Chains**:
  - Start with a base claim linked to an external source or media.
  - Ensure all linked resources are verifiable and follow a clear validation path.
- **Standardized Processes**:
  - Define clear guidelines for validating claims, such as matching `effectiveDate` timestamps or verifying the cryptographic digest of multimedia files.

---

### **Implementation Workflow**
1. **Construct the Claim**:
   - Fill core fields like `name`, `subject`, and `statement`.
   - Add context with `howKnown`, `aspect`, and `effectiveDate`.

2. **Integrate Evidence**:
   - Use the `images` array to attach multimedia evidence.
   - Ensure each image includes metadata, a cryptographic digest, and a timestamp.

3. **Build Trust Relationships**:
   - Use `confidence` to reflect the issuer’s stake in the claim's credibility.
   - Use `stars` for user-generated ratings and feedback.

4. **Implement Verification**:
   - Validate cryptographic digests in `digestMultibase`.
   - Confirm the accessibility and credibility of `sourceURI`.

5. **Iterate and Update**:
   - Allow claims to evolve by updating fields like `confidence`, `stars`, and `amt` as new evidence or feedback is received.

---

### **Implementation Workflow**
1. **Construct the Claim**:
   - Populate essential fields like `name`, `statement`, `subject`, and `howKnown`.
   - Include multimedia evidence, source URIs, and timestamps.

2. **Integrate Evidence**:
   - Attach multimedia evidence in the `images` array.
   - Ensure all evidence is timestamped and cryptographically verified.

3. **Build Trust Relationships**:
   - Use `confidence` to stake the issuer's credibility on the claim and `stars` to reflect user feedback.

4. **Verify Claims**:
   - Validate cryptographic digests and ensure source URIs are accessible.

---

### **Positioning of This Implementation**
This guide represents **one implementation** of LinkedClaims, designed with robustness and semantic clarity in mind. It demonstrates how addressability, evidence integration, and trust relationships can be operationalized effectively. However, LinkedClaims is a flexible framework, and other valid implementations may differ based on specific needs and contexts.

---

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
- Are there industry standards that LinkedClaims complies with?


## 8. Reference Implementations
- OpenCreds implementation-https://opencreds.net/
- Other- community implementations
- Example code repositories
