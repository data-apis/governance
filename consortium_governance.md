# Consortium governance

The purpose of this document is to describe the governance process used by
the Consortium for Python Data API Standards (Consortium), clarifying how
decisions are made, how to gain membership, and how we see the relationship
with related open source projects and the wider community.

_Note: the Consortium is still early in its formation process, with repositories being open sourced and initial standards documents being drafted. We expect the main principles and overall structure of governance to evolve over the next year._


## Principles

The main principles of Consortium governance are:

- an inclusive, multi-stakeholder based approach
- openness and transparency
- seeking consensus


## Membership

Consortium projects are developed by Contributors and Members. Contributors
are individuals who have contributed code, documentation, designs, feedback
or other work to a project. Members are individuals who, in addition to being
Contributors, act collectively to:

- Make decisions about the overall scope, vision and direction of the Consortium.
- Make decisions about specific technical and organizational issues.
- Sign off on releases of API standards.
- Make decisions when regular community discussion doesn’t produce consensus on an issue in a reasonable time frame.
- Update policy documents such as this one.

Membership in the Consortium can be gained by invitation from the existing membership body. Members can represent:

- A relevant open source project, that falls under the scope of a Consortium
  API standard (existing or being developed). Currently this includes
  array/tensor and dataframe libraries. What "relevant" means is hard to
  quantify in a metric, this will be decided upon by the existing Members.
- A Consortium Sponsor (see next section).

The initial set of Members has been put together with the following approach:

- We considered the most popular array and dataframe libraries.
- We then divided those up into community-driven and company-backed.
  _This is mostly clear based on project governance, but there is some grey area - in those cases we erred on the side of considering those projects community-driven._
- We have made sure to invite at least one key contributor from each community-driven project.
- We engaged all company-backed projects on an equal basis, asking them to
  become a Sponsor and join the Consortium.

See [this document](https://github.com/pydata-apis/governance/blob/master/sponsors_and_members.md)
for a listing of the current Consortium Members.

_To decide later: membership renewal/expiration_


### Sponsors

Developing API standards requires a significant amount of engineering work
and technical writing, which in turn requires funding. Sponsors provide that
funding. Sponsors will nominate up to three representatives as Members.
Sponsors will be publicly acknowledged on the Consortium website. At this
time there are no other Sponsor benefits - in case that changes, those
benefits will be documented in this governance document.

See [this document](https://github.com/pydata-apis/governance/blob/master/sponsors_and_members.md)
for a listing of the current Consortium Sponsors.


## Decision making

We aim to take decisions by consensus of all interested Contributors. An API
standard only has value if it is widely adopted, and decisions taken without
consensus lower the chance of adoption. Contributors should strive for
consensus, and if they have serious concerns about a proposal they should
articulate both the reason for that concern and what the proposer can do to
address the concern.

If consensus cannot be reached and a decision must be taken, Members will
decide by a simple majority vote on the mailing list, with a one week window
for casting votes. The vote proposer will be responsible for documenting
the outcome of the vote on the relevant GitHub issue or pull request. Members
are urged to keep in mind the value of consensus, and consider all reasonable
alternatives - decisions taken with significant dissent are likely to run
into similar concerns in the future.

### Changes to this governance document

Decision making on governance changes will follow the decision making procedure
described above (striving for consensus, voting if necessary), except that a
change proposal requires 80% of the votes to be accepted.


## Organization

### Roles

The Consortium has a Chair, who is responsible for organizing Members
meetings and ensuring the Consortium assets (e.g. GitHub org, website) are
managed effectively.


### Meetings

Members meetings are held weekly as video conference calls. At least ten
Members must be present in a meeting for making decisions. Meeting minutes
are kept in a document that can be collaboratively edited during the meeting,
and stored in a public GitHub repository afterwards.


### Relationship with Quansight Labs

Quansight Labs is the public benefit division of Quansight, with a mission to
support and improve projects in and community around the PyData ecosystem. It
acts as a steward for the Consortium assets and funding, and will be
accountable to Sponsors for received funding.
