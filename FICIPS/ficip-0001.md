---
ficip: 0001
title: FICIP Purpose and Guidelines
status: Active
type: Organizational
author: Whyrusleeping <whyrusleeping@protocol.ai> 
        https://github.com/filecash/FICIPs/blob/main/FICIPS/ficip-0001.md
created: 2019-04-02
---

## What is a FICIP?

FICIP stands for Filecash Improvement Proposal. A FICIP is a design document providing information to the Filecash community, or describing a new feature for Filecash or its processes or environment. The FICIP should provide a concise technical specification of the feature and a rationale for its adoption. The FICIP author is responsible for building consensus within the community and documenting dissenting opinions.

## FICIP Rationale

We intend FICIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Filecash. Because the FICIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

However, we also require that, where appropriate, Technical FICIPs are also reflected in the protocol's specification, which is the primary source of reference for other developers. The [Filecash Spec site](https://spec.file.cash) will in turn point back to the FICIPs that have changed some part of the protocol, as well as the FICIP's revision history.

For Filecash implementers, FICIPs are a convenient way to track the progress of their implementation. Ideally, each implementation maintainer would list the FICIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## FICIP Types

There are three main types of FICIPs:

1. A **Technical FICIP** (Filecash Technical Proposal or **FICTP**) describes any change that affects most or all Filecash implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Filecash. Technical FICIPs consist of three parts: a design document, an implementation, and, if warranted, an update to the [formal specification](https://spec.file.cash). Furthermore, technical FICIPs can be broken down into the following categories:
   - **Core** - improvements requiring a consensus upgrade, as well as changes that are not necessarily consensus critical but may be relevant to future consensus upgrades.
   - **Networking** - includes improvements to data propagation, or any of the Filecash network protocols (see [Network Interface](https://spec.file.cash) in the spec for a full listing). 
   - **Interface** - includes improvements around client [API/RPC](https://spec.file.cash) specifications and standards, and also certain language-level standards like method names. 
   - **Informational** - describes a Filecash design issue, or provides general guidelines or information to the Filecash community, but does not propose a new feature. Informational FICTPs do not necessarily represent Filecash community consensus or a recommendation, so users and implementers are free to ignore Informational FICTPs or follow their advice.

2. An **Organizational FICIP** (Filecash Organizational Proposal or **FICOP**) describes a process surrounding Filecash or proposes a change to (or an event in) a process. Process FICIPs are like Standards Track FICIPs but apply to areas other than the Filecash protocol itself. They may propose an implementation, but not to Filecash's codebase; they often require community consensus; unlike Informational FICIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, changes to the FICIP process, and changes to the tools or environment used in Filecash development.

3. A **Recovery FICIP** (Filecash Recovery Proposal or **FICRP**) proposes a state change that is necessary and that cannot be addressed using the standard protocol. FICRPs are only valid under a limited, clearly-defined set of criteria (e.g., in the case of protocol bugs destroying network value). The FICRP should describe the issue to be corrected, explain why an irregular state change is necessary and justified, and demonstrate that the proposed actions will achieve the FICRP's objectives.

It is highly recommended that a single FICIP contain a single key proposal or new idea. The more focused the FICIP, the more successful it tends to be. A change to one client doesn't require a FICIP; a change that affects multiple implementations, or defines a standard for multiple clients to use, does.

A FICIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## FICIP Work Flow

Parties involved in the process are you, the champion or *FICIP author*, the [*FICIP editors*](#ficip-editors), and the *Filecash Core Developers*.

:warning: Before you begin, vet your idea, this will save you time. Ask the Filecash community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Filecash is used. Examples of appropriate public forums to gauge interest around your FICIP include [the Issues section of this repository](https://github.com/filecash/FICIPs/issues), [the Filecash Discourse Forum](https://discuss.file.cash/). In particular, [the Issues section of this repository](https://github.com/filecash/FICIPs/issues) is an excellent place to discuss your proposal with the community and start creating more formalized language around your FICIP.

Your role as the champion is to write the FICIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful FICIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the FICIP author and reviewed by the FICIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your FICIP. The FICIP editors will process these requests as per the conditions below.

* **Active** -- Some Informational and Organizational FICIPs may also have a status of “Active” if they are never meant to be completed. E.g. FICIP-1 (this FICIP).
* **Work in progress (WIP)** -- Once the champion has asked the Filecash community whether an idea has any chance of support, they will write a draft FICIP as a [pull request](https://github.com/filecash/FICIPs/pulls). Consider including an implementation if this will aid people in studying the FICIP.
  * :arrow_right: Draft -- If agreeable, FICIP editor will assign the FICIP a number and merge your pull request. The FICIP editor will not unreasonably deny a FICIP.
  * :x: Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the [Filecash improvement principles](https://github.com/filecash/FICIPs/blob/main/README.md).
* **Draft** -- After the first draft is merged, you may still submit follow-up pull requests with further changes until you believe the FICIP to be mature and ready to proceed to the next status. A FICIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core FICIPs).
  * :arrow_right: Last Call -- If agreeable, the FICIP editor will assign Last Call status and set a review end date (`review-period-end`), normally 14 days later.
  * :x: Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that FICIPs only enter Last Call once, so as to avoid unnecessary noise.
* **Last Call** -- This FICIP will be listed prominently on the Filecash website
  * :x: -- A Last Call which results in material changes or substantial unaddressed technical complaints will cause the FICIP to revert to Draft.
  * :arrow_right: Accepted (Core FICIPs only) -- A successful Last Call without material changes or unaddressed technical complaints will become Accepted.
  * :arrow_right: Final (Not core FICIPs) -- A successful Last Call without material changes or unaddressed technical complaints will become Final.
* **Accepted (Core FICIPs only)** -- This FICIP is in the hands of the Filecash implementation developers.  Their process for deciding whether to encode it into their clients as part of a consensus upgrade is not part of the FICIP process.
  * :arrow_right: Final -- Standards Track Core FICIPs must be implemented in at least two viable Filecash clients before they can be considered Final. A Pull Request to the [Filecash Specification repository](https://spec.file.cash) updating the text of the spec to describe the protocol changes should also be submitted before the FICIP can proceed to the Final status. When the implementation is complete and adopted by the community, the status will be changed to “Final”.
* **Final** -- This FICIP represents the current state-of-the-art. A Final FICIP should only be updated to correct errata.

Other exceptional statuses include:

* **Deferred** -- This is for core FICIPs that have been put off for a future consensus upgrade.
* **Rejected** -- A FICIP that is fundamentally broken or a Core FICIP that was rejected by the Core Devs and will not be implemented.
* **Active** -- This is similar to Final, but denotes a FICIP which may be updated without changing its FICIP number.
* **Superseded** -- A FICIP which was previously final but is no longer considered state-of-the-art. Another FICIP will be in Final status and reference the Superseded FICIP.

## What belongs in a successful FICIP?

Each FICIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the FICIP, including the FICIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See below for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the FICIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional*) - The motivation is critical for FICIPs that want to change the Filecash protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the FICIP solves. FICIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature or process. Technical specifications should be detailed enough to allow competing, interoperable implementations for any of the current Filecash platforms.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All FICIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The FICIP must explain how the author proposes to deal with these incompatibilities. FICIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for FICIPs that are affecting consensus changes. Other FICIPs can choose to include links to test cases if applicable.
- Security Considerations - All FICIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. FICIP submissions missing the "Security Considerations" section will be rejected. A FICIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.
- Implementations - The implementations must be completed before any FICIP is given status “Final”, but it need not be completed before the FICIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All FICIPs must be in the public domain. See the bottom of this FICIP for an example copyright waiver.

## FICIP Formats and Templates

FICIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format.
Image files should be included in a subdirectory of the `assets` folder for that FICIP as follow: `assets/ficip-X` (for ficip **X**). When linking to an image in the FICIP, use relative links such as `../assets/ficip-X/image.png`.

## FICIP Header Preamble

Each FICIP must begin with an RFC 822 style header preamble, preceded and followed by three hyphens (`---`). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` ficip:` \<FICIP number\> (this is determined by the FICIP editor)

` title:` \<FICIP title\>

` author:` \<a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.\>

` * discussions-to:` \<a url pointing to the official discussion thread\>

` status:` \<Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded\>

`* review-period-end:` \<date review period ends\>

` type:` \<Technical (Core, Networking, Interface, FRC) | Organizational | Recovery\>

` * category:` \<Core | Networking | Interface | FRC\>

` created:` \<date created on\>

`spec-sections:` A list of Spec sections that the FICIP is updating.

`spec-pr:` The URL for the PR updating the Spec.

` * updated:` \<comma separated list of dates\>

` * requires:` \<FICIP number(s)\>

` * replaces:` \<FICIP number(s)\>

` * superseded-by:` \<FICIP number(s)\>

` * resolution:` \<a url pointing to the resolution of this FICIP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the FICIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `resolution` header

The `resolution` header is required for Standards Track FICIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the FICIP is made.

#### `discussions-to` header

While a FICIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the FICIP is being discussed. As mentioned above, examples for places to discuss your FICIP include the [Filecash Forum on Discourse](https://discuss.file.cash/) or an issue in this repo. 

No `discussions-to` header is necessary if the FICIP is being discussed privately with the author. 

As a single exception, `discussions-to` cannot point to GitHub pull requests.

#### `type` header

The `type` header specifies the type of FICIP: Technical, Organizational, or Recovery. If the track is Technical please include the subcategory (core, networking, interface, or informational).

#### `category` header

The `category` header specifies the FICIP's category. This is required for technical FICIPs only.

#### `created` header

The `created` header records the date that the FICIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `spec-sections`

Spec sections that the FICIP is updating, each section has an ID that can be found in the Spec website under each section "three dot" menu.

Example:
```yaml 
spec-sections:
  - section-intro
  - section-libraries.libp2p
  - section-systems.filecoin_markets.storage_market.deal-flow
  ```

#### `updated` header

The `updated` header records the date(s) when the FICIP was updated with "substantional" changes. This header is only valid for FICIPs of Draft and Active status.

#### `requires` header

FICIPs may have a `requires` header, indicating the FICIP numbers that this FICIP depends on.

#### `superseded-by` and `replaces` headers

FICIPs may also have a `superseded-by` header indicating that a FICIP has been rendered obsolete by a later document; the value is the number of the FICIP that replaces the current document. The newer FICIP must have a `replaces` header containing the number of the FICIP that it rendered obsolete.

## Auxiliary Files

FICIPs may include auxiliary files such as diagrams. Such files must be named FICIP-XXXX-Y.ext, where “XXXX” is the FICIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring FICIP Ownership

It occasionally becomes necessary to transfer ownership of FICIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred FICIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the FICIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the FICIP. We try to build consensus around a FICIP, but if that's not possible, you can always submit a competing FICIP.

If you are interested in assuming ownership of a FICIP, send a message asking to take over, addressed to both the original author and the FICIP editor. If the original author doesn't respond to email in a timely manner, the FICIP editor will make a unilateral decision (which can be reversed).

## FICIP Editors

The current FICIP editors are

` * Whyrusleeping (@whyrusleeping)`

` * Friedel Ziegelmayer (@dignifiedquire)`

` * Molly Mackinlay (@momack2)`

` * Aayush Rajasekaran (@arajasek)`

` * Jennifer Wang (@jennijuju)`

## FICIP Editor Responsibilities

For each new FICIP that comes in, an editor does the following:

- Read the FICIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the FICIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the FICIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the FICIP is ready for the repository, the FICIP editor will:

- Assign a FICIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this FICIP)

- Merge the corresponding pull request

- Check whether the FICIP needs to be accompanied by an update to the specification and if so, make sure that a PR to spec repository has been submitted and that the text that updates the spec is reflecting the changes that the FICIP proposes.

- Send a message back to the FICIP author with the next step.

Many FICIPs are written and maintained by developers with write access to the Filecash codebase. The FICIP editors monitor FICIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on FICIPs. They merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1](https://github.com/ethereum/EIPs) written by Martin Becze and Hudson Jameson, which was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki, which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/). In many places text was simply copied and modified. The authors of the previous texts on which this process is based are not responsible for the Filecash Improvement Process and should not be bothered with questions. Please direct all comments to the FICIP editors.

April 2, 2019: FICIP-1 created from EIP-1

See [the revision history for further details](https://github.com/filecash/FICIPs/blob/main/FICIPS/ficip-0001.md), which is also available by clicking on the History button in the top right of the FICIP.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
