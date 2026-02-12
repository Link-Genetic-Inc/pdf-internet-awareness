# Internet-Aware Content Representation in PDF

**Discussion Draft for PDF Technical Working Group**

---

## 1. Purpose

This document is intended to initiate a structured technical discussion on whether the PDF content model should support explicit, machine-readable representation of internet-related entities embedded in document content.

It does not propose a specific solution or mandate changes to ISO 32000-2.

---

## 2. Background and Motivation

PDF is widely used as an internet-distributed document format and is routinely consumed by:

- search engines and indexing systems
- compliance and audit tooling
- digital preservation and archival systems
- knowledge management platforms
- automated processing pipelines and AI systems

Despite this, internet-related information embedded in PDF content is generally treated as undifferentiated text unless explicitly converted into annotations.

---

## 3. Observed Limitation

Empirical investigation across multiple PDF processing toolchains indicates that:

- domain names, URLs, and email addresses embedded in content are structurally invisible
- identification requires heuristic approaches (e.g. regex, layout analysis)
- hyperlink functionality is available only via annotations
- no PDF-level structure exists to inventory or govern internet-related references

This limitation persists regardless of the quality or maturity of PDF generators or SDKs.

---

## 4. Scope Clarification

This discussion explicitly excludes:

- viewer auto-linking behavior
- UI or rendering considerations
- mandatory clickability
- browser-style navigation
- deprecation of existing annotation mechanisms

The focus is strictly on **content representation**, not interaction.

---

## 5. Conceptual Distinction

The discussion benefits from separating three concerns that are currently conflated:

1. **Recognition**  
   Identifying that a segment of content represents an internet-related entity.

2. **Representation**  
   Structurally expressing that information in a machine-readable way within the content model.

3. **Interaction**  
   Defining optional behaviors such as navigation or activation.

PDF currently provides standardized mechanisms primarily for interaction (via annotations), while recognition and representation are left to tooling heuristics.

---

## 6. Internet-Related Content Entities (Informal)

For discussion purposes, internet-related entities may include:

- domain names
- URLs / URIs
- email addresses
- resolver-based identifiers

These entities are not required to be hyperlinks.

---

## 7. Design Considerations (Non-Normative)

Any future exploration in this area should aim to be:

- backward compatible
- optional and non-intrusive
- independent of viewer behavior
- interoperable across generators and consumers
- suitable for archival and compliance use cases

---

## 8. Open Questions

This draft intentionally raises questions rather than prescribing answers:

1. Is the absence of explicit content-level representation for internet-related entities an intentional design choice or a historical artifact?
2. Should the PDF content model be able to express that certain text represents an internet-related entity independently of annotations?
3. Could existing mechanisms (e.g. marked content, structure tree, metadata) be clarified or leveraged?
4. Would guidance, profiles, or application notes be an appropriate first step?

---

## 9. Possible Next Steps (Non-Binding)

Depending on feedback, future exploration could include:

- a PDF Association Application Note
- clarification of existing specification mechanisms
- a scoped technical exploration within a working group
- confirmation that the current model is considered sufficient

---

## 10. Conclusion

This document does not argue that PDF is deficient, but that its content model reflects assumptions from an earlier era in which explicit representation of internet-related entities was not a primary concern.

Given modern usage patterns, it may be valuable to re-examine this area in a structured, non-disruptive way.
