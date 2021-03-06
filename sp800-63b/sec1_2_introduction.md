<a name="sec1"></a>

## 1. Purpose

_This section is informative._

This document and its companion documents, [SP 800-63-3](sp800-63-3.html), [SP 800-63A](sp800-63a.html), and [SP 800-63C](sp800-63c.html), provide technical guidelines to agencies for the implementation of digital authentication.

<a name="sec2"></a>

## 2. Introduction

_This section is informative._

Digital identity is the unique representation of a subject engaged in an online transaction. A digital identity is always unique in the context of a digital service, but does not necessarily need to uniquely identify the subject. In other words, accessing a digital service may not mean that the physical representation of the underlying subject is known. Identity proofing establishes that a subject is actually who they claim to be. Digital authentication is the process of determining the validity of one or more authenticators used to claim a digital identity. Authentication establishes a subject attempting to access a digital service is in control of the technologies used to authenticate.  For services in which return visits are applicable, successfully authenticating provides reasonable risk-based assurances that the subject that is accessing the service today is the same as that which accessed the service yesterday. Digital identity presents a technical challenge because this process often involves the proofing of individuals over an open network, and always involves the authentication of individual subjects over an open network to access digital government services. Of which exists multiple opportunities for impersonation and other attacks to fraudulently claim another subjects digital identity.

The ongoing authentication of subscribers is central to this process. Subscriber authentication is performed by verifying that the claimant controls one or more *authenticators* (called *tokens* in earlier editions of SP 800-63) associated with a given subscriber. A successful authentication results in the assertion of an identifier, either pseudonymous or non-pseudonymous, and optionally other identity information, to the relying party (RP).

This document provides guidelines on types of authentication processes, including choices of authenticators, that may be used at various *Authenticator Assurance Levels* (AALs). It also provides guidelines on the lifecycle of authenticators, including revocation in the event of loss or theft.

This technical guideline applies to digital authentication of subjects to systems over a network. It does not primarily address the authentication of a person who is physically present, for example, for access to buildings, although some credentials that are used remotely may also be used in local authentication. This technical guideline also establishes requirements that Federal systems and service providers participating in authentication protocols be authenticated to subscribers.

The strength of an authentication transaction is characterized by an ordinal measurement known as the AAL. Stronger authentication (a higher AAL) requires a higher level of capabilities or resources on the part of an attacker in order to successfully authenticate, effectively reducing the risk of an authentication error.  A high-level summary of the technical requirements for each of the authenticator assurance levels is provided below; see [Section 4](#sec4) and [5](#sec5) of this document for specific normative requirements.

**Authenticator Assurance Level 1** - AAL 1 provides some assurance that the claimant controls an authenticator registered to the subscriber. AAL 1 requires single-factor authentication using a wide range of available authentication technologies. Successful authentication requires that the claimant prove possession and control of the authenticator through a secure authentication protocol.

**Authenticator Assurance Level 2** – AAL 2 provides high confidence that the claimant controls authenticator(s) registered to the subscriber. Proof of possession and control of two different authentication factors is required through a secure authentication protocol. Approved cryptographic techniques are required at AAL 2 and above.

**Authenticator Assurance Level 3** – AAL 3 provides very high confidence that the claimant controls authenticator(s) registered to the subscriber. Authentication at AAL 3 is based on proof of possession of a key through a cryptographic protocol. AAL 3 is like AAL 2 but also requires a "hard" cryptographic authenticator that provides verifier impersonation resistance.
