
## Technical Committee

The Video.js project is jointly governed by a Technical Steering Committee (TSC)
which is responsible for high-level guidance of the project.

The TSC has final authority over this project including:

* Technical direction
* Project governance and process (including this policy)
* Contribution policy
* GitHub repository hosting
* Conduct guidelines
* Maintaining the list of additional Collaborators

Initial membership invitations to the TSC were given to individuals who
had been active contributors to Node.js, and who have significant
experience with the management of the Node.js project. Membership is
expected to evolve over time according to the needs of the project.

For the current list of TSC members, see the project
[README.md](https://github.com/videojs/video.js/blob/master/README.md#tsc-members).

## Collaborators

The [videojs/video.js](https://github.com/videojs/video.js) GitHub repository is
maintained by the TC and additional Collaborators who are added by the
TC on an ongoing basis.

Individuals making significant and valuable contributions are made
Collaborators and given commit-access to the project. These
individuals are identified by the TC and their addition as
Collaborators is discussed during the weekly TC meeting.

_Note:_ If you make a significant contribution and are not considered
for commit-access, log an issue or contact a TC member directly and it
will be brought up in the next TC meeting.

Modifications of the contents of the videojs/video.js repository are made on
a collaborative basis. Anybody with a GitHub account may propose a
modification via pull request and it will be considered by the project
Collaborators. All pull requests must be reviewed and accepted by a
Collaborator with sufficient expertise who is able to take full
responsibility for the change. In the case of pull requests proposed
by an existing Collaborator, an additional Collaborator is required
for sign-off. Consensus should be sought if additional Collaborators
participate and there is disagreement around a particular
modification. See _Consensus Seeking Process_ below for further detail
on the consensus model used for governance.

Collaborators may opt to elevate significant or controversial
modifications, or modifications that have not found consensus to the
TC for discussion by assigning the ***tsc-agenda*** tag to a pull
request or issue. The TC should serve as the final arbiter where
required.

For the current list of Collaborators, see the project
[README.md](https://github.com/videojs/video.js/blob/master/README.md#current-project-team-members).

A guide for Collaborators is maintained in
[COLLABORATOR_GUIDE.md](https://github.com/videojs/video.js/blob/master/COLLABORATOR_GUIDE.md).

## TC Membership

TC seats are not time-limited.  There is no fixed size of the TC.
However, the expected target is between 6 and 12, to ensure adequate
coverage of important areas of expertise, balanced with the ability to
make decisions efficiently.

There is no specific set of requirements or qualifications for TC
membership beyond these rules.

The TC may add additional members to the TC by a standard TC motion.

A TC member may be removed from the TC by voluntary resignation, or by
a standard TC motion.

Changes to TC membership should be posted in the agenda, and may be
suggested as any other agenda item (see "TC Meetings" below).

No more than 1/3 of the TC members may be affiliated with the same
employer.  If removal or resignation of a TC member, or a change of
employment by a TC member, creates a situation where more than 1/3 of
the TC membership shares an employer, then the situation must be
immediately remedied by the resignation or removal of one or more TC
members affiliated with the over-represented employer(s).

## TC Meetings

The TC meets bi-weekly on a Google Hangout On Air. The meeting is run by
a designated moderator approved by the TC. Each meeting should be
published to YouTube.

Items are added to the TC agenda which are considered contentious or
are modifications of governance, contribution policy, TC membership,
or release process.

The intention of the agenda is not to approve or review all patches.
That should happen continuously on GitHub and be handled by the larger
group of Collaborators.

Any community member or contributor can ask that something be added to
the next meeting's agenda by logging a GitHub Issue. Any Collaborator,
TC member or the moderator can add the item to the agenda by adding
the ***tsc-agenda*** tag to the issue.

Prior to each TC meeting, the moderator will share the Agenda with
members of the TC. TC members can add any items they like to the
agenda at the beginning of each meeting. The moderator and the TC
cannot veto or remove items.

The TC may invite persons or representatives from certain projects to
participate in a non-voting capacity.

The moderator is responsible for summarizing the discussion of each
agenda item and sending it as a pull request after the meeting.

## Consensus Seeking Process

The TC follows a
[Consensus Seeking](http://en.wikipedia.org/wiki/Consensus-seeking_decision-making)
decision making model.

When an agenda item has appeared to reach a consensus, the moderator
will ask "Does anyone object?" as a final call for dissent from the
consensus.

If an agenda item cannot reach a consensus, a TC member can call for
either a closing vote or a vote to table the issue to the next
meeting. The call for a vote must be approved by a majority of the TC
or else the discussion will continue. Simple majority wins.

# Additional Process and Role Descriptions 

*Adopted and slightly modified from [0MQ C4.1](http://rfc.zeromq.org/spec:22))*

- A "Contributor" is a person who wishes to provide a patch, being a set of commits that solve some clearly identified problem.
- A "Collaborator" (a.k.a. "Maintainer") is a person who merges patches to the project. **Collaborators are not required to be developers**; their job is to enforce process.
- Contributors SHALL NOT have commit access to the repository unless they are also Collaborators.
- Collaborators SHALL have commit access to the repository.
- Everyone, without distinction or discrimination, SHALL have an equal right to become a Contributor under the terms of this contract.

## Licensing and Ownership

- All contributions to the project source code ("patches") SHALL use the same license as the project.
- All patches are owned by their authors. There SHALL NOT be any copyright assignment process.
- The copyrights in the project SHALL be owned collectively by all its Contributors.
- Each Contributor SHALL be responsible for identifying themselves in the project Contributor list.

## Patch Requirements

- Collaborators and Contributors MUST have a Platform account and SHOULD use their real names or a well-known alias.
- A patch SHOULD be a minimal and accurate answer to exactly one identified and agreed problem.
- A patch MUST adhere to the code style guidelines of the project if these are defined.
- A patch MUST adhere to the "Evolution of Public Contracts" guidelines defined below.
- A patch SHALL NOT include non-trivial code from other projects unless the Contributor is the original author of that code.
- A patch MUST compile cleanly and pass project self-tests on at least the principle target platform.
- A patch commit message SHOULD consist of a single short (less than 50 character) line summarizing the change, optionally followed by a blank line and then a more thorough description.
- A "Correct Patch" is one that satisfies the above requirements.

## Development Process

- Change on the project SHALL be governed by the pattern of accurately identifying problems and applying minimal, accurate solutions to these problems.
- To request changes, a user SHOULD log an issue on the project Platform issue tracker.
- The user or Contributor SHOULD write the issue by describing the problem they face or observe.
- The user or Contributor SHOULD seek consensus on the accuracy of their observation, and the value of solving the problem.
- To work on an issue, a Contributor SHALL fork the project repository and then work on their forked repository.
- To submit a patch, a Contributor SHALL create a Platform pull request back to the project.
- A Contributor SHALL NOT commit changes directly to the project.
- If the Platform implements pull requests as issues, a Contributor MAY directly send a pull request without logging a separate issue.
- To discuss a patch, people MAY comment on the Platform pull request, on the commit, or elsewhere.
- (needs discussion) To accept or reject a patch, a Collaborator SHALL use the Platform interface.
- Collaborators SHOULD NOT merge their own patches except in exceptional cases, such as non-responsiveness from other Collaborators for an extended period (more than 1-2 days).
- Collaborators SHALL NOT make value judgments on correct patches.
- Collaborators SHALL merge correct patches from other Contributors rapidly.
- The user who created an issue SHOULD close the issue after checking the patch is successful.
- Collaborators SHOULD ask for improvements to incorrect patches and SHOULD reject incorrect patches if the Contributor does not respond constructively.
- Any Contributor who has value judgments on a correct patch SHOULD express these via their own patches.
- Collaborators MAY commit changes to non-source documentation directly to the project.

## Evolution of Public Contracts

- All Public Contracts (APIs or protocols) SHOULD be documented.
- All Public Contracts SHOULD have space for extensibility and experimentation.
- A patch that modifies a stable Public Contract SHOULD not break existing applications unless there is overriding consensus on the value of doing this.
- A patch that introduces new features to a Public Contract SHOULD do so using new names.
- Old names SHOULD be deprecated in a systematic fashion by marking new names as "experimental" until they are stable, then marking the old names as "deprecated".
- When sufficient time has passed, old deprecated names SHOULD be marked "legacy" and eventually removed.
- Old names SHALL NOT be reused by new features.
- When old names are removed, their implementations MUST provoke an exception (assertion) if used by applications.

## Technical Steering Committee (a.k.a Project Administration)

- The project founders SHALL act as Administrators to manage the set of project Collaborators.
- The Administrators SHALL ensure their own succession over time by promoting the most effective Collaborators.
- A new Contributor who makes a correct patch SHALL be invited to become a Collaborator.
- Administrators MAY remove Collaborators who are inactive for an extended period of time, or who repeatedly fail to apply this process accurately.
- Administrators SHOULD block or ban "bad actors" who cause stress and pain to others in the project. This should be done after public discussion, with a chance for all parties to speak. A bad actor is someone who repeatedly ignores the rules and culture of the project, who is needlessly argumentative or hostile, or who is offensive, and who is unable to self-correct their behavior when asked to do so by others.
