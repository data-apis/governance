# Consortium Process

> This document describes the Consortium for Python Data API Standards process.

The Consortium for Python Data API Standards ("Consortium") is responsible for evolving the standards governing Python data APIs and authoring the associated specifications. The Consortium operates by consensus and has discretion to alter the specification as needed. However, the general process for making changes to the specification is as follows.

## Overview

The purpose of this document is to provide a clearly defined sequence for evolving an idea to a fully specified feature, complete with compliance tests and multiple implementations. The process intends to address the needs of three stakeholders.

1.  **authors**: specification authors requiring guidance on proposal tasks and expectations.
2.  **implementors**: specification implementors requiring guidance regarding direction and expected implementation compliance.
3.  **end users**: specification consumers (e.g., downstream users) requiring time-line and consumption expectations (e.g., when and how can an API be consumed).

## Stages

The process is comprised of five stages: a strawperson stage and four "maturity" stages. The Consortium must approve acceptance for each stage.

Strawperson proposals are open to individuals outside of the Consortium as a means to solicit broader community input. The Consortium should own staged (1-4) proposals.

0.  **Strawperson**

    > **Note**: a strawperson proposal can be considered an "idea" stage, where an idea may or may not have technical merit. This is left to the Consortium to evaluate and indicate acceptance for moving to stage 1.

    -   **purpose**: allow specification input.

    -   **entrance criteria**: none.

    -   **acceptance signifies**: (N/A).

    -   **spec quality**: (N/A).

    -   **post-acceptance changes expected**: (N/A).
    
    -   **implementation types expected**: (N/A).

    > **Example**: an API for evaluating the standard error of the mean should be added to the array API specification. Rationale: because the measure is commonly used in statistics.

1.  **Proposal**

    -   **purpose**

        -   to make the case for the addition
        -   to describe the shape of a solution
        -   to identify potential challenges

    -   **entrance criteria**

        -   one or more Consortium members must identify as "champions" who will advance the proposal

        -   a written outline of the problem and the general shape of a solution

            > **Example**: TensorFlow, Torch, and NumPy all have API `foo` which enjoys significant downstream usage, thus demonstrating the value of `foo`; however, each of the aforementioned libraries provides a slightly different signature (and/or semantics) for `foo` which introduces friction among array library consumers and downstream library authors.

        -   illustrative examples of usage (i.e., how is the API being used in the "wild")

        -   a proposed high-level API 

        -   discussion of key semantics

        -   identification of potential challenges, complexity, and cross-cutting concerns

            > **Example**: requiring support for an `out` keyword for `foo` may impose an undue burden on array libraries supporting whole graph optimization and lazy evaluation.

        -   a publicly available document for the proposal that captures the above requirements

    -   **acceptance signifies**: the Consortium expects to devote time to examining the problem space, solutions, and cross-cutting concerns.

    -   **spec quality**: none.

    -   **post-acceptance changes expected**: major changes.

    -   **implementation types expected**: real-world library implementations (at least `2`).

1.  **Draft**

    -   **purpose**: to precisely describe the syntax and semantics according to specification standards.

    -   **entrance criteria**

        -   everything in Stage 1
        -   initial specification text

    -   **acceptance signifies**: the Consortium expects the addition to be developed and eventually included in the standard.

    -   **spec quality**: a draft which includes the API signature and all major semantics covered, but TODOs, placeholders, and editorial issues are expected.

    -   **post-acceptance changes expected**: incremental.

    -   **implementation types expected**: libraries may begin writing experimental implementations in order to test and gather proposal feedback.

        > **Note**: this document advocates that experimental APIs should **not** be included in official array library versions. Instead, array libraries may offer experimental APIs only under experimental flags, bleeding edge versions, or on particular branches, in order to allow experimentation without any guarantees as to API stability or backward compatibility.

1.  **Candidate**

    -   **purpose**: to indicate that further refinement will require feedback from implementations and users.

    -   **entrance criteria**

        -   everything in Stage 2
        -   complete specification text
        -   designated Consortium reviewers have signed off on the current specification text

    -   **acceptance signifies**: the solution is complete and no further work is possible without implementation experience, significant usage, and external feedback.

    -   **spec quality**: a completed text with all semantics, syntax, and signature described.

    -   **post-acceptance changes expected**: limited, where only those changes having been deemed critical based on implementation experience are expected.

    -   **implementation types expected**: specification compliant.

        > **Note**: this document advocates that Stage 3 proposals should still **not** be included in official publicly released standard compliant library versions. Instead, these additions should remain behind experimental flags, bleeding edge versions, or on particular branches in order to allow continued experimentation without guarantees as to API stability or backward compatibility.

1.  **Finished**

    -   **purpose**: to indicate that the addition is ready for inclusion in the official API standard.

    -   **entrace criteria**

        -   everything in Stage 3
        -   compliance tests written and merged
        -   a quorum (TODO: to be determined/articulated) of compliant library implementations which pass compliance tests
        -   significant real-world experience with shipping implementations (e.g., such as that provided by an array library designed for CPU-based computation and by another array library designed for accelerators)
        -   a pull request submitted against the repository containing the API with the specification text
        -   a majority of Consortium members have approved the pull request

    -   **acceptance signifies**: the addition will be included in the next standard revision.

    -   **spec quality**: a completed and finalized text with all changes as a result of implementation experience having been integrated.

    -   **post-acceptance changes expected**: none.

    -   **implementation types expected**: shipping.

        > **Note**: this means that, so long as a proposal has reached Stage 4, standard compliant libraries can begin shipping (as part of public releases) the proposed addition(s), without having to wait for the next standard revision.

## Input into the Process

Ideas for evolving Python data APIs are accepted in any form. Any discussion, idea, or proposal for a change or addition which has not been submitted as a formal proposal shall be considered a "strawperson" (stage 0) and has no acceptance requirements.

## Status of Additions

The Consortium maintains a list of in-process additions, along with the current maturity stage of each, on GitHub.

## Reviewers

Any Consortium member is allowed to be a reviewer and to submit feedback on an in-process addition. Once a proposal reaches Stage 2, the Consortium should identify designated reviewers who must sign-off on the proposal before acceptance to Stage 3. These reviewers should not be authors of the proposal and should have expertise applicable to the subject matter. Designated reviewers must be chosen by the Consortium, not by the proposal's champion.

## Implementation and Feedback

When an addition is accepted at the "candidate" (stage 3) maturity level, the Consortium is signifying that it believes design work is complete and further refinement will require implementation experience, significant usage, and external feedback.

## Tests

During stage 3, specification tests should be authored and submitted via pull request. Once the pull request has been appropriately reviewed, the tests should be merged to aid implementors in providing expected feedback.

## Editors

In-process specification additions will likely be authored by a champion or Consortium member who is not also a specification editor. Specification editors are responsible for the overall structure and coherence of the respective specification, and their role entails providing guidance and feedback to specification text authors in order to ensure quality and completeness as the proposed addition improves. Editors are responsible for integrating additions which have progressed to "finished" (stage 4) as a new revision of the specification.