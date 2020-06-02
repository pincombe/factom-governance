**FACTOM**

**COMMUNITY**

**Factom Testnet Governance**

**DOC 007**

Table of Contents

[Definitions](#definitions) 5

[Introduction](#_dyhln552kbki) 5

[Purpose and scope of this governance
document](#purpose-and-scope-of-this-governance-document) 6

[Purpose and value of the Factom Testnet](#_j5sxk66fdw79) 7

[Governance model for the Factom Testnet](#_sv9vw397n2rv) 8

[Roles and Responsibilities](#_7g8ju582zqeb) 9

[Standing of Role Holders](#_8tcbtxnxil2y) 11

[Election and removal of Testnet Administrator](#_4lyuct6239uy) 11

[Funding of Testnet](#funding-of-testnet) 12

[Appendix 1- Testnet reports](#appendix-1--testnet-reports) 13

[Appendix 2 - Application form to run a
node](#appendix-2---application-form-to-run-a-node) 14

[Appendix 3 - Minimum technical specification for a testnet
node](#appendix-3---minimum-technical-specification-for-a-testnet-node)
15

[Appendix 4 - Record of testnet nodes by
operator](#appendix-4---record-of-testnet-nodes-by-operator) 16

[Appendix 6 - Testnet operation
SLA](#appendix-6---testnet-operation-sla) 18

[Appendix 7 - Factom testnet administrator candidate
requirements](#appendix-7---factom-testnet-administrator-candidate-requirements)
19

[Appendix 8 - Testnet Administrator Election and Removal
Process](#appendix-8---testnet-administrator-election-and-removal-process)
20

+----------------+----------------+----------------+----------------+
| Document       |                |                |                |
| control        |                |                |                |
| matrix\*       |                |                |                |
+================+================+================+================+
| **ENT          | **PART OF      | **APPROVAL     | **APPROVAL     |
| ITY/ENTITIES** | DOCUMENT**     | TYPE**         | AUTHORITY FOR  |
|                |                |                | THIS           |
|                |                |                | DOCUMENT**     |
+----------------+----------------+----------------+----------------+
| Standing       | No highlight   | ⅘ guide        | Yes            |
| parties\*\*    |                | approval       |                |
|                |                |                |                |
|                |                | ⅗ ANO approval |                |
+----------------+----------------+----------------+----------------+
| Factom         | Text/tables    | ⅘ Guide        | No             |
| Guides\*\*     | highlighted:   | approval       |                |
|                | N/A            |                |                |
+----------------+----------------+----------------+----------------+
| Testnet        | Appendices 1-7 | Single entity  | Yes            |
| Administrator  |                | approval       |                |
+----------------+----------------+----------------+----------------+

> \* See [[Doc 002 - Administration of governance- and community
> documents]{.underline}](https://docs.google.com/document/d/12nvQVDOoLFNtmV_jqFEeWo1Ixx3R08z4KqLNVEbDoU4/edit?usp=sharing),
> Chapter 3.
>
> \*\* See [[Doc 001 - *Factom
> Governance*]{.underline}](https://docs.google.com/document/d/1RVaVR7lvfGgOBMG-7oca9TtpnR7qaEfr6XJVaZJwd3M/edit?usp=sharing),
> Definitions.

  VERSION   DRAFT DATE   DRAFT BY                          CHANGES                                                               APPROVED BY               APPROVED DATE
  --------- ------------ --------------------------------- --------------------------------------------------------------------- ------------------------- ---------------
  1.0       2019-08-26   Testnet Working Group/Cube3 LLC   First version                                                         Factom Standing Parties   2019-11-15
  1.1       2019-12-19   The 42nd Factoid AS               Amending Appendix 8 to include Guides voting in TA election/removal   Factom Standing Parties   2020-01-03

Definitions
===========

The definitions used in this document are those made in [[Factom
Governance Document (Doc
001)]{.underline}](https://docs.google.com/document/d/1RVaVR7lvfGgOBMG-7oca9TtpnR7qaEfr6XJVaZJwd3M/edit?usp=sharing)
except where expressly stated otherwise.

2.  Introduction
    ============

    1.  The Factom protocol needs to continue to evolve and develop but
        > also needs to be reliable and stable.

    2.  The way we seek to reconcile these two potentially conflicting
        > objectives is to run one or more separate network(s) of nodes
        > that perform similarly to Mainnet and where we can safely
        > experiment.

    3.  This network is designated Testnet. Individual testnets may be
        > operated provided that are approved by the Standing Parties.
        > They will be designated Testnet-suffix where the suffix is
        > unique and indicative of the purpose of a particular testnet.
        > The purpose of each individual testnet is to be shown in the
        > relevant section of the Factom protocol website. Hereafter in
        > this Doc any reference to Testnet includes the individual
        > testnets.

    4.  Running a Testnet is not easy or straightforward and Factom\'s
        > experience of doing this is that it is appreciated as a test
        > bed for new code and as a learning ground for new ANOs but is
        > underutilized, because of things like low specification nodes,
        > leading to a poor indication of Mainnet capability. This has
        > resulted in a number of drivers for change which have informed
        > this revised Governance Doc.

    5.  In order to run the Testnet more effectively we need an improved
        > operating framework. This document seeks to provide this
        > framework by which a distributed group of entities design,
        > implement, deploy, and execute the Testnet Network as an
        > integral part of overall Factom governance.

    6.  The way this document seeks to provide this governance framework
        > for the Testnet is by defining the value the Testnet brings to
        > the Factom protocol so that people see how critical it is and
        > participate accordingly. The focus is on the rigour required
        > to maintain the Testnet and the dependence on people playing
        > their roles.

3.  Purpose and scope of this governance document
    =============================================

    1.  Purpose

> Provide a governance framework for the Testnet, which is anchored into
> general Factom governance, which:

1.  Ensures proper administration with clear roles for administrators
    > and participants.

2.  Provides for the election of, and as necessary replacement of,
    > administrators and participants.

3.  Enables the following capabilities:

    1.  Smooth functioning.

    2.  Running a range of tests including load tests on core code and
        > 3rd party software.

    3.  Easy introduction of new participants to the workings of the
        > protocol.

    4.  Evaluation of potential ANOs.

```{=html}
<!-- -->
```
2.  Scope

> This document defines the purpose and value of the Factom Testnet. It
> describes how the Testnet will be governed in the context of the
> overall Factom Governance Model. The roles and responsibilities of
> those involved in operating and governing the Factom Testnet are
> specified.

4.  Purpose and value of the Factom Testnet
    =======================================

    1.  The basic purpose is to:

        1.  Test core code and new developments

        2.  Enable any party to test any hardware or software in a safe
            > environment

        3.  Run performance tests

        4.  Enable new ecosystem participants to practice running
            > server(s) in a safe test environment and experiment with
            > operations such as "brain swaps"

        5.  Approximate the Factom Mainnet so that all facets of Mainnet
            > operations can be tested and experimented with

    2.  The value of this is that we can:

        1.  Provide a playground for developers.

        2.  Keep the community involved and give the protocol the
            > ability to look ahead.

        3.  Demonstrate to ourselves, developers and users whether and
            > how things work.

        4.  Test the factomd codebase to uncover bugs.

        5.  Coach people in a safe, supportive environment, and provide
            > the standing parties a means to assess an applicant\'s
            > ability to reliably run an authority server, thus ensuring
            > basic competence before actually operating on the Factom
            > Mainnet.

        6.  Collectively compile testing scenarios for use under
            > different circumstances.

        7.  Conduct analysis and assessment of tests and provide a
            > service to people testing developments and applications.

        8.  Ensure consistent acceptance criteria for anything moving to
            > Mainnet in conjunction with the Core Code Committee.

5.  Governance model for the Factom Testnet
    =======================================

    1.  Testnet governance relates to Mainnet governance and any other
        > documents as follows:

        1.  Testnet governance is a subset of the overall governance
            > model for Factom.

        2.  Decision making about Testnet falls into line with decision
            > making by the community and is subject to the same
            > disciplines. The only exception to this is the decision
            > making authority delegated to the formally appointed
            > Testnet Administrator.

    2.  The principles for Testnet governance

        1.  Representative of Mainnet.

        2.  Serves the community by enabling structured, disciplined
            > testing of new core developments and new 3rd party
            > applications.

    3.  Administration

        1.  The Testnet Administrator administers and manages the
            > Testnet

        2.  The scope of administration is:

            1.  Facilitating smooth Testnet network operations
                > (including design, development and operation)

            2.  Defining standards (equipment and behavioural) for
                > Testnet participation

            3.  Supporting test activities

            4.  Onboarding new participants to the Testnet and
                > evaluating potential ANOs through objective assessment
                > of their competence in participating in Testnet

            5.  Defining clear roles/terms of reference for participants
                > and anyone or any working group providing support

            6.  Promoting active community engagement by managing a
                > dedicated channel for this purpose (e.g., Discord)

    4.  Testnet help/support

        1.  Given that a number of Testnet participants may be
            > inexperienced, the Tesnet administration will provide a
            > help desk as a support service.

    5.  Transparency and Integrity

        1.  All aspects of Testnet governance and operation will be
            > accessible via the Factom protocol website which will
            > hold:

            1.  Structure, organisation, responsibilities and means of
                > contact

            2.  An overview of the testnets being managed, with a clear
                > definition of the purpose of each testnet

            3.  Detailed information about each testnet:

                1.  Specifications and standards

                2.  Application forms and process

                3.  List of servers and participants

                4.  Status information

                5.  Links to Factomized records of overall performance
                    > and individual tests/results

6.  Roles and Responsibilities
    ==========================

> **Testnet Administrator**

1.  Responsibility for governance of the Factom Testnet

    1.  The responsibility for governance of the Factom Testnet(s)
        > resides with the appointed Testnet Administrator

    2.  Aspects of this may be delegated.

2.  The role of the Testnet Administrator is to:

    1.  Define the strategic purpose of the Testnet, as outlined in this
        > document.

    2.  In concert with the website committee, create and maintain the
        > relevant part of the Factom protocol website described in
        > section 5.5.1.

    3.  Implement the program of work for using and improving the Factom
        > Testnet as developed and agreed by the Core Committee.

    4.  Exercise budgetary control of the Testnet.

    5.  Manage and control the participants using the Factom Testnet.

    6.  Define and police the standards for use of the Factom Testnet.

    7.  Install appropriate measures of Factom Testnet use and
        > performance and publish these measures as regular reports.
        > (see Appendix 1 for frequency and content of regular reports)

    8.  Advise the standing parties about the use by, and performance
        > of, new participants using the Factom Testnet who wish to
        > become ANOs. The mechanism for this is primarily via the above
        > Testnet reports.

**Testnet authority node operators**

3.  Eligibility to run a Testnet node

    1.  Any ANO may apply to run a number of Testnet authority nodes

    2.  Any prospective ANO may apply to run a number of Testnet
        > authority nodes

    3.  No other party may apply to run a Testnet authority node

    4.  Approval to actually initially run a Testnet authority node and
        > continuing to run a Testnet authority node is granted by the
        > Testnet Administrator

    5.  Appeals against judgements by the Testnet Administrator will be
        > heard by the standing parties.

4.  Costs and Rewards for running a Testnet Authority Node

    1.  All costs for running a Testnet Node are borne by the operator
        > and are not reimbursable.

    2.  There are no rewards for running a Testnet Authority Node.
        > Running a Testnet Node is considered a gesture of support for
        > the Protocol, which may contribute to ANO standing.

5.  Responsibility of Testnet participants

    1.  Testnet participants are required to:

        1.  Apply formally to run a Testnet node. (See application form
            > in Appendix 2)

        2.  Meet a minimum technical standard for each node (See
            > specification in Appendix 3)

        3.  Record the number of Testnet nodes being operated on this
            > Google Sheet [[Google Sheet showing Testnet
            > nodes]{.underline}](https://docs.google.com/spreadsheets/d/1tXXIQM7FYAAJ0hCiUZJQIu9G4F8AAm0IOcyRTM8yJjw/edit?usp=sharing)
            > tab Current Authority Identities illustrated in Appendix 4

        4.  Maintain each node by updating Factomd as directed by the
            > Testnet Administrator, (Recording this on the [[Google
            > Sheet for recording Factomd testnet updates by
            > node]{.underline}](https://docs.google.com/spreadsheets/d/1tXXIQM7FYAAJ0hCiUZJQIu9G4F8AAm0IOcyRTM8yJjw/edit?usp=sharing)
            > tab Authority Set Updates illustrated in Appendix 5)

        5.  Be proactive in operating their node(s) including responding
            > promptly to Testnet stalls and being able to hotswap (in
            > accordance with the SLA specified in Appendix 6 )

        6.  Participate actively in the Discord Community Testnet
            > channel(s)

6.  Consequences of not running a Testnet node in line with the
    > guidelines

    1.  In the event of a Testnet node operator not running a node in
        > line with the guidelines the first recourse the Testnet
        > Administratorwill be to issue a warning.

    2.  Should such a warning not be heeded then the Testnet
        > Administrator will be able to suspend the operation of a
        > particular node, recording this status with the reason on the
        > testnet register publicly available via the Factom protocol
        > website. This will have the effect of demoting them from the
        > testnet authority set but still enables the running of a
        > Testnet node on which ANO standing depends. If a prospective
        > ANO they are therefore eligible to be elected. If an existing
        > ANO this does not automatically reduce standing. Such a ruling
        > can be overridden by the Standing Parties to whom any affected
        > Testnet participant can appeal only after full and proper
        > dialogue with the Testnet Administrator.

```{=html}
<!-- -->
```
7.  Standing of Role Holders
    ========================

    1.  Standing in the community is defined by Doc 001. This makes no
        > allowance for the Testnet Administrator or any other Testnet
        > role holder to have standing.

    2.  The Testnet Administrator is expected to operate independently
        > of Guides and Committees; they are accountable only to the
        > full Standing Parties.

8.  Election and removal of Testnet Administrator
    =============================================

    1.  It is anticipated that a Factom Testnet Administrator would
        > stand for a period of six months. The Factom Testnet
        > Administrator is elected by the standing parties.

    2.  The candidate requirements are outlined in Appendix 7.

    3.  Any candidate meeting these requirements may put themselves up
        > for election.

    4.  An election will be held using the process described in
        > Appendix 8.

    5.  The Factom Testnet Administrator can be removed in line with the
        > process described in Appendix 8.

9.  Funding of Testnet
    ==================

    1.  If a Testnet budget is required the Testnet Administrator will
        > be required to make a case via the Grant system which would
        > approve and fund it in the normal way.

    2.  If the Testnet is awarded funds then the Testnet administrator
        > is required to create and control a budget. The setting and
        > management of such a budget will be public with regular
        > updates.

    3.  Because of the value of the Factom Testnet Administrator role
        > they may be compensated for their time by the award of tokens
        > from the Grant Pool. This requested compensation should be
        > clearly announced in the Testnet Administrator Application. If
        > elected, the consecutive grants will be part of the ordinary
        > grant process, and the grants will have to be approved and
        > awarded by the standing parties.

Appendix 1- Testnet reports
===========================

Frequency

The frequency of Testnet reports should as a minimum be monthly.

Means of publication

The Testnet monthly reports will be published on the Factom protocol
website.

Contents

**Number of nodes**

> Number as leader
>
> Number as audit
>
> Number as follower

**Total uptime**

**Total downtime**

> Reasons for downtime

**Testing conducted**

> For each test a description and test results

**ANO Applicants**

Specific section about applicants operating on the Testnet which helps
the standing parties determine if applicants are worthy of their support
or not.

This section should be highly standardized/objective.

By applicant

-   Number of nodes

-   Update performance (if they have updated appropriately within 1 week
    > of updates being made available)

-   Any unexplained downtime etc.

Appendix 2 - Application form to run a node
===========================================

Application to run a node

This application form once approved will enable the applicant to run a
single node on the Factom Testnet.

Name of applicant

Contact details for applicant

Name of entity

Status of entity

Mainnet ANO

Applicant ANO

independent

Other

If other please specify here

If currently running other test net nodes please state which nodes

Description of the applicant entity\'s experience of server
administration

Combined length of entity\'s server administration experience

Technical specification of server

Number of CPU cores

Type of CPU and clock speed

Whether RAM is scalable

Whether memory is scalable

Storage disk size

Free storage space for databases

Connection/uplink speed

Please describe your purpose in running a node

How will you administer this node

How will you ensure timely response to the requirements to update your
node or restart your node

Please make any other comments relevant to your application here

Thank you for your application you will be notified of the success or
otherwise of your application via email to the address provided by you.

Appendix 3 - Minimum technical specification for a testnet node
===============================================================

**Hardware**

A modern CPU (minimum 4 cores)

4 GB RAM (recommended 8)

50 GB storage

20 MBit/s synchronous uplink

Up to 1TB / month data transfer

Static IP-address

**Software**

Nodes require to be monitored and need to be both on Portainer and have
the factomd opened to monitoring.

**Operational capability**

Up time measured in weeks and months, not days.

Appendix 4 - Record of testnet nodes by operator
================================================

![](.//media/image2.png){width="5.8125in" height="4.208333333333333in"}

 

Appendix 6 - Testnet operation SLA
==================================

Testnet Node Operators are expected to maintain their nodes at a level
that is consistent with a healthy network. These include but are not
limited to plans for hot backup/brainswap servers. (This allows critical
updates and network restarts to happen in a timely manner which is vital
for the stability and vitality of the testnet and therefore its value to
end users.)

Testnet operators would be expected to monitor their nodes and respond
as promptly as possible to any stalls.

Given that there is currently no formal means of alerting Testnet
authority node operators such notice would via the normal channels of
communication such as the Discord testnet announcements channel.

Checking in through the chosen communication channel would be the
appropriate first course of action.

Testnet operators must respond to any and all alerts within twenty four
(24) hours of the occurrences of the trigger events.

The Testnet Administrator and/or the Guides and/or the Core Code
Committee may contact Testnet node operators individually in order to
expedite responses to a stalled Testnet.

 

Appendix 7 - Factom testnet administrator candidate requirements
================================================================

The applicant should be a natural person, as distinct from an entity,
with the following characteristics:

1.  Deep knowledge of the Factom protocol

2.  Readiness and ability to engage with the community (via multiple
    > channels)

3.  Able to create and manage a plan and a budget

4.  Proven track record of server administration

5.  Able to succinctly and effectively report status (of Testnet(s))

6.  Good administrator able to maintain accurate operational records

7.  A self-starter who is able to work on their own initiative

8.  Somebody who is confident and articulate, able to initiate, explain
    > and promote/defend a course of action

 

Appendix 8 - Testnet Administrator Election and Removal Process
===============================================================

1.  Process

    1.  Testnet Administrator Election Process

        1.  The election process shall be hosted sufficiently in advance
            > and shall conclude at least one (1) month prior to the
            > commencement date of the terms to enable a smooth
            > transition between the departing Testnet Administrator and
            > the elected Testnet Administrator.

        2.  The current Guides are responsible for hosting Testnet
            > Administrator elections.

        3.  Upon commencement of a Testnet Administrator election, the
            > following process will be followed.

        4.  A temporary "Testnet Administrator Candidates" subforum will
            > be created on the community forum.

        5.  The current Guides will create a post in the community
            > Discord, the community Reddit, the community forum, and
            > any other important communication platforms for the Factom
            > Protocol to announce the upcoming election. The post will
            > contain:

            1.  A link to this document.

            2.  Information regarding current Testnet Administrator
                > compensation.

            3.  An announcement that candidates are welcome to announce
                > their candidacy by creating a thread within the
                > Testnet Administrator Candidates subforum.

                1.  The thread title will only contain the name of the
                    > candidate.If the candidate is an entity, the name
                    > should be the entity name.

                2.  The body of the thread will include the information
                    > the candidate wants to present to the community

            4.  The dates of the election in UTC time. Dates will
                > include:

                1.  Seven (7) days for candidates to post their
                    > candidacy in the forum.

                2.  Four (4) days for the Factom Community to ask the
                    > candidates questions.

                3.  Twenty-four (24) hours for the candidates to answer
                    > any last-minute questions.

                4.  Three (3) days for ANOs and Guides to vote for the
                    > new Administrator.

            5.  For the final vote, a single thread with a poll will be
                > created in the Governance Discussion forum on the
                > community forum.

                1.  All ANOs and Guides will be allowed to vote
                    > together.

                2.  The candidates will be listed in alphabetical order.

                3.  ANOs and Guides will be able to vote for as many
                    > candidates as they want.

                4.  The results will not be revealed until the poll
                    > closes.

                5.  If there is a tie, a runoff thread with a poll will
                    > be created immediately and only the candidates who
                    > are tied will be listed.

            6.  Notification of the runoff will be posted on all
                > communication platforms. The runoff vote will last for
                > three (3) days.

        6.  The Guides shall announce the results of the election on the
            > community platforms.

    2.  Testnet Administrator Removal Process

        1.  The removal procedure described in this document is intended
            > for removal of a Testnet Administrator for any reason that
            > ten percent (10%) of Authority Node Operators (ANOs) and
            > Guides deem worthy of initiating the process.

        2.  A Testnet Administrator shall not be removed under this
            > document unless the procedure set forth herein is strictly
            > followed.

        3.  The Testnet Administrator subject to the removal process is
            > hereinafter referred to as the "Subject Testnet
            > Administrator".

        4.  The removal process shall be commenced by an ANO or Guide
            > representing at least 10% of all the ANOs and Guides by
            > making a motion through a "Timed Thread" set as a "Major
            > Discussion", named "REMOVAL: \[Subject Testnet
            > Administrator's Name\]," in the Governance Discussion
            > forum at the Factom community forum (the "Removal Thread")
            > or other platform used by the community.

            1.  The number of ANOs and Guides required to make a removal
                > motion will be the smallest whole number of ANOs and
                > Guides that meet or exceed 10% of the total number of
                > ANOs and Guides.

> *Example: for 26 ANOs and Guides, 10% is 2.6 so the minimum number of
> the ANOs and Guides to make a removal motion is three (3).*

2.  The Removal Thread shall be public but can only be posted in and
    > voted on by ANOs and Guides.

3.  The Timed Thread will have a poll with the subject, "Should
    > \[Subject Testnet Administrator\] be Removed as a Testnet
    > Administrator?" with the options of "Yes", "No" and "Abstain". The
    > poll will not begin until the timed discussion ends.

4.  The initiator shall provide a link to this document, the names of
    > the other 10%+ ANOs and Guides supporting the removal motion, the
    > rationale behind the removal, and any supporting evidence in the
    > first post of the thread.

5.  The Subject Testnet Administrator may state their case in the
    > thread.

6.  There shall be a minimum of eight (8) days of open discussion
    > regarding the removal motion in order to give the Subject Testnet
    > Administrator a reasonable opportunity to answer and defend
    > themself. As such, discussion may not be ended early but may be
    > extended following the normal procedure for Major Timed
    > Discussions.

7.  After the discussion phase has ended a vote will be automatically
    > initiated. The voting period shall be three (3) days. The votes
    > will not be revealed until the poll closes.

8.  If a simple majority (more than 50% of the ANOs and Guides) vote
    > yes, the motion carries and the Testnet Administrator is removed.
    > If less than 50% of the ANOs and Guides vote yes, the motion fails
    > and the Subject Testnet Administrator maintains their position.

```{=html}
<!-- -->
```
5.  If the removal motion passes:

    1.  The Subject Testnet Administrator will be immediately removed
        > from the Testnet Administrator position and their access to
        > the community platforms associated with the Testnet
        > Administrator position shall be terminated.

    2.  An announcement with explanatory language agreed to by the
        > Guides will be posted on communication platforms for the
        > Factom Protocol.

    3.  The \'Testnet Administrator Election Process\' set forth in
        > Section 1.1 of this document will be initiated by the Guides
        > within seventy-two (72) hours.
