# GoCreate Honey RFCs

This repo is a place to propose and track major upcoming changes to [GoCreate Honey] and
other related projects. It also is a great place to learn about the current and
future state of the libraries and to discover projects for contribution.

**Jump to**: [What is an RFC?](#what-is-an-rfc) |
[When to submit?](#when-to-submit-an-rfc) |
[RFC Process](#rfc-process) |
[RFC Life Cycle](#the-rfc-life-cycle)

<!--BEGIN_TABLE-->
\#|Title|Owner|Status
---|-----|-----|------
[2](https://github.com/gocreateio/honey-rfcs/issues/2)|[Reminders](https://github.com/gocreateio/honey-rfcs/blob/master/text/0002-reminders.md)||❓unknown
<!--END_TABLE-->

## What is an RFC?

An RFC is a document that proposes and details a change or addition to the [GoCreate Honey] and other related tooling.
It also is a process for reviewing and discussing the proposal and tracking its implementation. "Request for Comments"
means a request for discussion and oversight about the future of the [GoCreate Honey] from contributors and users.
It is an open forum for suggestions, questions, and feedback.

The process is intended to be as lightweight and reasonable as possible for the
present circumstances. As usual, we are trying to let the process be driven by
consensus and community norms, not impose more structure than necessary.

The RFC process itself is subject to changes as dictated by the core team and
the community. Proposals can include proposed changes to the RFC process itself
to better serve contributors.

## When to submit an RFC?

You should consider using this process if you intend to make "substantial"
changes to [GoCreate Honey] or related tools. Some examples that would
benefit from an RFC are:

- Any change to existing APIs that could break existing code.
- The removal of existing features or public APIs.
- The introduction of new idiomatic usage or conventions, even if they do not
  include code changes to [GoCreate Honey].
- Changes to the documented contribution workflow.
- Features that cross multiple construct libraries.
- Additions or changes to framework capabilities.
- Additions or changes to formal specifications like cloud assembly, tree.json, etc.

The RFC process is a great opportunity to get more eyeballs on your proposal
before it becomes a part of a released version of [GoCreate Honey]. Quite often, even
proposals that seem "obvious" can be significantly improved once a wider group
of interested people have a chance to weigh in.

The RFC process can also be helpful to encourage discussions about a proposed
feature as it is being designed, and incorporate important constraints into the
design while it's easier to change, before the design has been fully
implemented.

If you submit a pull request to implement a new major feature without going
through the RFC process, it may be closed with a polite request to submit an RFC
first.

Some changes do not require an RFC:

- Bugfixes for known issues.
- Additions only likely to be _noticed by_ other developers of [GoCreate Honey], invisible to users of [GoCreate Honey].
- Additions of missing L1 or L2 constructs. Unless the service and/or constructs
  are especially complex or intentionally diverge from existing api design best
  practices.

If you're not sure whether your change requires an RFC, feel free to create an
issue and ask.

## RFC Process

In short, to get a major feature added to [GoCreate Honey], one usually writes an RFC
as a markdown file and gets it approved and merged into the RFC repo. At that point the RFC is
'approved' and may be implemented into [GoCreate Honey].

1. [Create a **tracking
   issue**](https://github.com/gocreateio/honey-rfcs/issues/new?template=tracking-issue.md)
   for the proposed feature if one doesn't already exist. Use the tracking issue
   template as a guide. If a tracking issue already exists, make sure to update
   it and assign it to let others know you're working on a proposal.
2. Fork the [RFC repo](https://github.com/gocreateio/honey-rfcs).
3. Copy `0000-template.md` to `text/<rfc#>-<my-feature>.md` where <rfc#> is the
   tracking issue number and `<my-feature>` is the rfc title.
4. Fill in the RFC. Put care into the details: **We welcome all honest efforts
   to contribute.**.
5. Submit a **pull request** with the title `RFC: ### <title>` where ### is the
   tracking issue number and title is the name of the proposal. As a pull
   request the RFC will receive design feedback from the core team and the
   larger community, and the author should be prepared to make revisions in
   response.
6. Update the tracking issue with a link to the RFC PR.
7. **Advertise** your RFC amongst stakeholders via social channels (e.g.
   twitter) and your team. Build consensus and integrate feedback. RFCs that
   have broad support are much more likely to make progress than those that
   don't receive any comments.
8. Eventually, the team will decide whether the RFC is a candidate for inclusion
   in [GoCreate Honey].
9. RFCs that are candidates for inclusion in [GoCreate Honey] will enter a "**final comment
   period**" lasting 3 calendar days. The beginning of this period will be signaled
   by a team member adding a comment and label on the RFCs pull request.
10. An RFC can be modified based upon feedback from the team and community.
    Significant modifications may trigger a new final comment period. An RFC can
    also be modified after it has been merged and approved, in which case a new
    PR will be submitted with the modification, like any other code.
11. An RFC may be **rejected** by the team after public discussion has settled
    and comments have been made summarizing the rationale for rejection. A
    member of the team will then close the PR and issue.
12. An RFC may be **accepted** at the close of its final comment period. A team
    member will merge the RFCs associated pull request, at which point the RFC
    will become 'approved'.
13. At some point, someone will pick up the RFC for implementation. For major
    features this usually requires devising a detailed implementation plan. To
    that end, submit an **additional PR** on the RFC doc that either fills in
    the "Implementation Plan" section or references a separate document or
    GitHub Project Board which includes the plan.
14. Once this PR is approved, the RFC will move to the 'implementing' state.
    Usually we track implementation using GitHub projects.
15. Once implementation is complete, the RFC moves to 'done', and it's issue is
    closed.

> If the submitter is someone from our [GoCreate Honey] community (i.e., not core team member),
a core team member will be assigned to 'shepherd' each proposal. They will
generally be the ones updating the RFCs state in the tracking issue as it moves
through the process. They can decide when a final comment period is triggered.
>
> On the other hand, if the submitter is a core team member, they will identify
another core team member, with consent, as their 'shepherd'. The shepherd would
be the first contact for brainstorming, process and reviews. The core team
would defer to the shepherd to do the first few rounds of reviews, after which
the rest of the team should be engaged.

## RFC Life Cycle

![rfc-states](./images/lifecycle.png)

<!--
digraph states {
    node [shape=ellipse];
    edge [color=gray, fontsize=12]
    
    idea [label = "Idea", shape = plaintext]
    proposed [label = "Proposed"];
    review [label = "In Review"];
    fcp [label = "Final Comment Period"];
    approved [label = "Approved"];
    planning [label = "Planning"];
    implementing [label = "Implementing"];
    done [label = "Done"];
    rejected [label = "Rejected"];
    
    idea -> proposed [label = "github issue created"]
    proposed -> review [label = "pull request with rfc doc created"];
    review -> review [label = "doc revisions"];
    review -> fcp [label = "shepherd approved"];
    review -> rejected [label = "rejected"];
    fcp -> review [label = "revision requested"];
    fcp -> approved [label = "pull request approved and merged"];
    fcp -> rejected [label = "rfc rejected"];
    approved -> planning [label = "pull request with implementation plan created"];
    planning -> implementing [label = "rfc with implementation plan approved and merged"];
    implementing -> done [label = "implementation completed"];
}  
-->

1. **Proposed** - A tracking issue has been created with a basic outline of the
   proposal.
2. **Review** - An RFC document has been written with a detailed design and a PR is
   under review. At this point the PR will be assigned a **shepherd** from the core
   team.
3. **Final Comment Period** - The shepherd has approved the RFC PR, and announces
   that the RFC enters a period for final comments before it will be approved (~1wk).
   At this stage, if major issues are raised, the RFC may return to **Review**.
4. **Approved** - The RFC PR is approved and merged to `master`, and the RFC is now
   ready to be implemented.
5. **Planning** - A PR is created with the **Implementation Plan** section of the RFC.
6. **Implementing** - Implementation plan is approved, merged, and the RFC is actively
   being implemented.
7. **Done** - Implementation is complete and merged across appropriate
   repositories.
8. **Rejected** - During the review period, the RFC may be rejected and then it will
   be marked as such.

---

GoCreate Honey RFC process owes its inspiration to the [AWS CDK RFC Process].

[AWS CDK RFC Process]: https://github.com/aws/aws-cdk-rfcs
[GoCreate Honey]: https://github.com/gocreateio/honey
