# FACTOM GOVERNANCE DOC 001

## Document control matrix

| ENTITY/ENTITIES | PART OF DOCUMENT | APPROVAL TYPE | APPROVAL AUTHORITY FOR THIS DOCUMENT |
| --- | --- | --- | --- |
| Standing Parties** | ⅘ guide approval | ⅗ ANO approval | Yes |
| Factom Guides** | Text/tables highlighted: ORANGE | ⅘ Guide approval | No |
| Not applicable | Not applicable | Single entity approval | No |

> \* See [<span class="underline">Doc 002 - Administration of
> governance- and community
> documents</span>](https://docs.google.com/document/d/12nvQVDOoLFNtmV_jqFEeWo1Ixx3R08z4KqLNVEbDoU4/edit?usp=sharing),
> Chapter 3.
>
> \*\* See [<span class="underline">Doc 001 - *Factom
> Governance*</span>](https://docs.google.com/document/d/1RVaVR7lvfGgOBMG-7oca9TtpnR7qaEfr6XJVaZJwd3M/edit?usp=sharing),
> Definitions.

| VERSION | DRAFT DATE | DRAFT BY | CHANGES | APPROVED BY | APPROVED DATE |
|---------|------------|----------|---------|-------------|---------------|
| 1.0     | N/A        | Factom Community | Final document for ratification | Factom Community | 2018-04-07 |
| 1.1     | N/A        | Factom Guides    | Version 1.1 | Factom Guides | 2018-04-17 |
| 1.2     | N/A        | Factom Guides    | Version 1.2 | Factom Guides | 2018-05-04 |
| 1.3     | N/A        | Factom Guides    | Version 1.3 | Factom Guides | 2018-06-17 |
| 1.4     | 2019-02-21 | Factom Guides    | Required changes to make document compatible with other community documents (Doc 100, Doc 101, Doc 002). Deleted text about guide initial roles. | Standing Parties | 2019-03-01 |
| 1.5     | 2019-04-22 | Factom Guides    | Assorted changes to section 2, 3 and 4. | Standing Parties | 2019-05-06 |
| 1.6     | 2019-10-28 | Factom Guides    | Authority Set removal section 3.3, Support Categories section 6.2 | Standing Parties | 2019-11-13 |

## Table of Contents

[<span class="underline">Definitions</span>](#definitions)

[<span class="underline">Guides</span>](#guides)

> [<span class="underline">Guide eligibility
> standards</span>](#guide-eligibility-standards)
>
> [<span class="underline">Guide
> responsibilities</span>](#guide-responsibilities)
>
> [<span class="underline">Guide Election and
> Removal</span>](#guide-election-and-removal)
>
> [<span class="underline">Guide
> remuneration</span>](#guide-remuneration)

[<span class="underline">Authority Set</span>](#authority-set)

> [<span class="underline">Elections</span>](#applications)
>
> [<span class="underline">Campaign document</span>](#_jqagr7fz3m9)
>
> [<span class="underline">Campaign factors</span>](#campaign-factors)
>
> [<span class="underline">Historical node
> reliability</span>](#testnet-participation)
>
> [<span class="underline">Support of
> Protocol</span>](#support-of-protocol)
>
> [<span class="underline">Node technical specifications and
> reliability</span>](#node-technical-specifications-and-reliability)
>
> [<span class="underline">Location</span>](#location)
>
> [<span class="underline">Standing Parties</span>](#_2rf3nam11zr8)
>
> [<span class="underline">Authority set removal</span>](#_f14io3z8jexb)
>
> [<span class="underline">Authority
> Independence</span>](#authority-independence)

[<span class="underline">Protocol Support
Grants</span>](#protocol-support-grants)

> [<span class="underline">Grant Proposals</span>](#grant-proposals)
>
> [<span class="underline">Grant Approval
> Process</span>](#grant-approval)
>
> [<span class="underline">Grant Support</span>](#_uu7tsqi9kyzn)
>
> [<span class="underline">Grant award process</span>](#_6pzh732y1m6)
>
> [<span class="underline">Sunset</span>](#_x8l61sfo94t5)
>
> [<span class="underline">Ongoing Governance
> Grants</span>](#ongoing-governance-grants)
>
> [<span class="underline">Anchor master</span>](#anchor-master)
>
> [<span class="underline">Oracle Master</span>](#oracle-master)
>
> [<span class="underline">Guide Remuneration
> Grant</span>](#guide-remuneration-grant)

[<span class="underline">Token Supply</span>](#token-supply)

> [<span class="underline">Token Rewards</span>](#token-rewards)
>
> [<span class="underline">Grant Pool
> Allocation</span>](#grant-pool-allocation)
>
> [<span class="underline">Grant Rewards</span>](#_1clgkc2k7f57)
>
> [<span class="underline">Authority Set
> Veto</span>](#authority-set-veto)

[<span class="underline">Standing Parties</span>](#standing-parties)

> [<span class="underline">Requirements for a Standing
> Party</span>](#requirements-for-a-standing-party)
>
> [<span class="underline">Support
> Categories</span>](#support-categories)
>
> [<span class="underline">Support category: Proof of
> stake</span>](#support-category-proof-of-stake)
>
> [<span class="underline">Retrospective
> staking</span>](#retrospective-staking)
>
> [<span class="underline">Prospective
> Staking</span>](#prospective-staking)
>
> [<span class="underline">Support category: Proof of
> use</span>](#support-category-proof-of-use)
>
> [<span class="underline">Support category:
> Guide</span>](#support-category-guide)
>
> [<span class="underline">Support category: Authority
> set</span>](#support-category-authority-set)
>
> [<span class="underline">Support category:
> Efficiency</span>](#support-category-efficiency)
>
> [<span class="underline">Support category:
> Contribution</span>](#support-category-contribution)
>
> [<span class="underline">Delegation</span>](#delegation)
>
> [<span class="underline">Delegation
> Process</span>](#delegation-process)
>
> [<span class="underline">Delegation
> Penalty</span>](#delegation-penalty)

[<span class="underline">Amendments and additional community
documents</span>](#amendments-and-additional-community-documents)

Definitions
===========

**Protocol**

Unless explicitly modified to refer to other protocols, the term
protocol in this document refers to the Factom protocol, which is
implemented in software, and run upon servers run by many independent
users and parties. The protocol’s definition is substantially defined
by the software run by the [<span class="underline">authority
set</span>](#kix.lres0524adra). The protocol creates an immutable
record of data, and distributes it over the participating nodes on the
network.

**Governance**

Governance is the process by which a distributed group of entities
design, implement, deploy, execute and promote the protocol, and the
ecosystem around the protocol. Much of governance centers on the
protocol code that in turn generates and provides incentives in the
form of tokens, and distributes those tokens by the rules embodied in
the code. The Guides aid in managing this process.

**Community**

Community in this document refers to the community of users,
developers, investors, traders, and organizations that have an
interest in building, running, promoting, and using the Factom
protocol, and other protocols building upon or dependent upon the
Factom protocol. Community is central to Factom as everyone with an
interest in Factom has an opportunity to play a role in maintaining,
developing, and promoting the Factom protocol.

**Factom Community Testnet Network**

The entirety of the Testnet Network including all operating nodes and
the community of users who support the Testnet Network.

**Testnet Authority Pool**

The group of Qualified Authority Nodes, including nodes currently
operating as part of the Authority Set of the Community Testnet.

**Federated Server**

A node that is authorized to create directory blocks and write to the
blockchain. The Federated servers use a consensus algorithm to agree
on what to include in the blocks.

**Audit Server**

The Audit Servers operate in the same manner as the Federated Servers;
in practice, they do the same work, but are not authorized to write to
the blockchain. If a federated server is removed from the federated
server Set, an Audit server is promoted to take its place, and the
Federated Server becomes an audit server.

**Authority Set**

The complete set of Federated Servers and Audit Servers. These are the
servers that run and serve as the backbone of the protocol.

The Factom Mainnet will include 65 servers in the Authority Set after
Milestone 3 (33 Federated servers and 32 Audit servers).

All Audit and Federated Servers share equally in the tokens issued by
the protocol.

**Authority Node Operator (ANO)**

An entity or an individual selected via governance processes to
operate and maintain Federated Server(s) and/or Audit Server(s).

**Digital identity**

Digital identity and digital identities in this document refer to a
set of chains in the protocol used to define a digital identity. In
some places, we simply refer to an identity, or a protocol identity.
In this document, all of these terms refer to Digital Identity.
Digital identities are central to governance, roles, voting, standing,
and auditing in the protocol.

**Grant Pool**

The protocol will allow the authority set to signal a higher
efficiency, by specifying a distribution less than the maximum
distribution. Tokens left over due to the efficiency of the servers
are placed into the grant pool within the protocol. The grant pool
will be used to promote the protocol, subsidize infrastructure, and
fund development of the protocol.

**Efficiency**

Efficiency in this document refers to how much we can reduce the cost
of running the protocol. To the degree we can increase efficiency
(reduce costs of running the protocol), we can increase the support of
the grant pool. As such, the higher an Authority Node’s deferment to
the protocol, the higher its efficiency.

**Standing Party**

A party that has standing in the protocol to support a given outcome
in any process. These processes include but are not limited to
selection of guides, authority set members, and/or grant proposals.

**Guides**

Guides are a group of entities charged with facilitating orderly
operation of the protocol. Guides are selected by the Standing
Parties, and work with the community to promote and maintain the
protocol. A guide can be an individual, or an organization that is
represented by an individual. Guides have very limited
responsibilities in the protocol.

**Protocol Support Budget**

The protocol support budget is a set of tokens generated at 72933.12
tokens per month. A month is defined as 4383 blocks, and a year is
defined as 52596 blocks.

**Proof of Stake (PoS)**

Proof of Stake refers to using opportunity costs to secure a
blockchain. Parties with tokens locked up are thought to be committed
to the blockchain due to their exposure to the value of the
blockchain, and thus can be trusted to make decisions within the
blockchain. How stake is defined varies over blockchains.

**Proof of Work (PoW)**

The grandfather of blockchains, proof of work is usually done by
hashing, where a nonce allows the miner to change the value of the
hash by changing the nonce. Work is measured by non-random leading
digits, usually zeros. More zeros, more work was done to find an
appropriate hash.

**Delegated Proof of Stake (DPoS)**

Pretty much the same as PoS, but those with stake can delegate their
voting power to other entities. This allows something of a more
representative form of governance.

## 1. Introduction

- **1.1.**  The following documents the governance model for the Authority
        Set and the protocol.

- **1.2.**  The network will be initially governed by a set of Guides
        entrusted with promoting the best interests of the protocol
        and the community depending on the continued orderly operation
        of the protocol.

- **1.3.**  The long term plan is to automate many of the objective
        components, the weighting driving decision making, and other
        aspects of protocol governance. As an interim step, the Guides
        will provide governance, allowing a period of experimentation
        where policies can be swiftly adjusted to meet the needs
        presented by running the protocol in a real world setting. As
        governance is fundamentally a human process, it is likely that
        not all aspects can be fully automated.

- **1.4.**  The Authority Set, Guides, Developers, and Community will work
        to develop and refine workable processes. Once agreed upon,
        these processes will be implemented into the protocol.

## 2. Guides

Guides are a group of entities selected by the other Standing Parties
who are charged with maintaining orderly operation of the protocol.
Guides have very limited responsibilities in the protocol. No group or
entity is to be allowed to provide a majority of the guides.

The responsibilities of the Guides will be phased out over time as the
functions they provide are automated into the protocol.

### 2.1.  Guide eligibility standards

- **2.1.1.**  Guides should demonstrate independence in thought, leadership,
        and business. Two guides should not have entangled business,
        political, or social connections that might call into question
        decisions and actions that might best serve the interest of
        groups of people over the interests of the protocol.

- **2.1.2.**  A Guide can be an individual, or group represented by an
        individual. The individual (or if a group, the group and
        representing individual) must be of good moral character with
        a demonstrated interest in the long term best interests of the
        protocol, willingness to serve the community of users, and
        history as a leader in the community.

### 2.2.  Guide responsibilities

- **2.2.1.**  Guides will make themselves available to the community.

- **2.2.2.**  Guides are charged with maintaining the orderly operation of the
        protocol network and facilitating the relationships between
        Standing Parties and the community.

- **2.2.3.**  Guides will be responsible for overseeing the application of the
        protocol governance to the operation of the protocol. To be
        fair, everyone involved are responsible for adhering to
        governance, but in practice, the Guides will be in the best
        position to provide guidance.

- **2.2.4.**  Maintaining the orderly operation of the network includes
        ensuring an adequate number of applicants to run a large
        enough pool of servers to ensure 65 servers are always
        available for the Authority Set. The guides will be in close
        communication with the Testnet, and monitor the performance of
        members of the Testnet Authority Pool.

- **2.2.5.**  Guides will meet at least once a week. Guide meetings do not
        have to be in person. A valid meeting has at least three of
        the five Guides, and will be public.

- **2.2.6.**  Minutes of the weekly Guide meeting will be published on the
        protocol, including attendance.

- **2.2.7.**  Guides will provide oversight and coordination of the grant
        process, execution, and evaluation.

- **2.2.8.**  Guides will document conflicts of interest in the minutes of
        guide meetings, and recuse themselves from decisions where
        they have a conflict of interest.

## 2.3.  Guide Election and Removal

- **2.3.1.**  The processes to elect and remove a Guide and other relevant
        terms are supplemented by [<span class="underline">Doc 100:
        Guide Election and Removal
        Processes</span>](https://factomize.com/forums/documents/doc-100-guide-election-and-removal-process.57/).
        Upon completion of the necessary infrastructure, relevant
        governance and community documents shall be amended to
        incorporate the on-chain election process.

## 2.4.  Guide remuneration

- **2.4.1.**  Guides will be compensated for their time by the award of tokens
        from the Grant Pool. Each Guide position is allocated tokens
        from the grant pool by the protocol itself.

- **2.4.2.**  Guides will be awarded via the grant process for their service.
        The details of grants should adjust for workload, FCT price,
        and other factors.

### 3. Authority Set

The Authority Set is comprised of entities (and hardware + software
they control) to build blocks on the Factom blockchain. These entities
are Authority Node Operators (“ANOs”) and are elected to the Authority
Set in accordance with [<span class="underline">Doc 005: ANO Election
and Demotion
System</span>](https://factomize.com/forums/documents/doc-005-ano-election-and-demotion-system.107/)
and the principles set out in this chapter. Addresses specified by the
individual ANOs are able to receive newly created FCT as reward for
maintaining the hardware + software which advances progress of the
blockchain.

Standing Parties will evaluate candidates based-on both technical and
non-technical potential contributions to the Factom Protocol.
Membership will be granted and revoked as a result of campaigns, and
performance running the protocol with support of the Standing Parties.

### 3.1. Applications
    ------------

- **3.1.1.**  Applicants wishing to be authorized to run an Authority Set node
        publish their desire to participate and document their
        qualifications by submitting an application via the Factom
        Protocol forum.

### 3.2.  Campaign factors
    ----------------

- **3.2.1.**  The following are some factors that will be considered as
        indicators to begin with when deciding which entities running
        servers on the protocol to promote into the Authority Set.

### 3.2.2. Testnet participation

- **3.2.2.1.**  The applicant will demonstrate the ability to reliably run a
            node by having run an authority server as a member of the
            Testnet Authority Set.

### 3.2.3. Support of Protocol

- **3.2.3.1.**  Applicants commitment to the support of the Factom protocol
            will be a factor considered.

- **3.2.3.2.**  An application can pledge a level of [<span
            class="underline">efficiency</span>](#kix.43gwl7p2gek8).

### 3.2.4. Node technical specifications and reliability

- **3.2.4.1.**  Authority Node Operators are expected to maintain their
            nodes at a level that is consistent with a healthy
            network. These include but are not limited to:

- **3.2.4.2.**  Plans for hot backup/brainswap servers.

- **3.2.4.3.**  Plans for the technical capabilities and capacity of
            proposed nodes.

- **3.2.4.4.**  Planned availability of the maintenance team.

### 3.2.5. Location

        1.  Having Authority nodes spread out over different
            geographies, jurisdictions, Autonomous System Numbers, and
            service providers will help keep the network running
            through localized failures.

    6.  ### Authority Server Specifications

        1.  The minimum server specifications are detailed in [<span
            class="underline">Doc 202 - Authority Server Minimum
            Specifications</span>](https://docs.google.com/document/d/1MF2E9G_hZ3bD0EwKlbsTNvaHMcHqJkLAIfYJb-AGJfg/edit?usp=sharing),
            and applicants should ensure to meet these when submitting
            their application.

3.  Authority Set Removal
    ---------------------

    1.  ### Removal for cause:

        1.  ANOs not meeting the expectations set forth in [<span
            class="underline">Doc 003: Authority Node Operator
            Expectations</span>](https://drive.google.com/open?id=1IylZOUbY5D3_qbRDDOHSFPIKoVav15h8ojTESpQP3Y0)
            may be removed from the Authority Set by the ANO Removal
            process defined in [<span class="underline">Doc 101:
            Removal of ANO from the Authority Set for
            Cause</span>](https://drive.google.com/open?id=1JhdOhz7e93_oSpQ3JzE9YwbH5Y05rnULsOI_hf2UGr4).

        2.  Removed ANOs can campaign to re-enter the Authority Set once
            the issues are resolved. They will do this through means
            of ordinary ANO election campaigns.

    2.  ### Removal for loss of Standing:

        1.  ANOs must maintain a level of Standing as described in
            [<span class="underline">Doc 005: ANO Election and
            Demotion
            System</span>](https://factomize.com/forums/documents/doc-005-ano-election-and-demotion-system.107/)
            to remain in the Authority Set. Should an ANO’s Standing
            fall below the required threshold, the ANO will be removed
            from the Authority Set for loss of Standing in accordance
            with the procedures set forth in Doc 005.

4.  Authority Independence
    ----------------------

Authorities are considered independent if they have no organizational
or contractual ties to other individuals or organizations running
authority nodes. Independence is also measured by sector. For example,
the more nodes that are run by organizations in the financial sector,
the less independent those nodes are, even if the organizations seem
to qualify as being independent.

The factom protocol will strive to maintain a high degree of
independence between authorities. Independence must be enforced
socially through campaigns as it can’t be measured on the blockchain.

Protocol Support Grants
=======================

A Grant Pool of tokens is maintained by the protocol to support
upkeep, enhancement, and promotion of the protocol.

The pool is created from efficiency commitments made by Authority Node
Operators. The details of the token rewards and the grant pool are
discussed in the section on [<span class="underline">Token
Supply</span>](#token-supply).

1.  Grant Proposals
    ---------------

    1.  Proposals for grants may be made by anyone.

    2.  Grants are required to advance the protocol, through building
        infrastructure, promotion, development, or education. Grants
        may pay for completed work or support future work on the
        protocol.

    3.  Grants cannot be issued as part of a lottery, or any other game
        or chance, pyramid type reward structure, etc.

    4.  A grant proposal will specify what is to be accomplished with
        the tokens awarded, a time frame for accomplishing the aims of
        the grant, a general description of how the aims will be
        achieved, and a measurement by which success of the grant can
        be measured.

For complex efforts, grant awards will be issued on completion of
milestones specified in the grant proposal. A sponsor or sponsors
selected from the guides, or willing Standing Parties may be appointed
to validate milestones. This administration should be part of the
proposal itself, with the support of the parties that would have to
oversee the grant.

Grant Approval
--------------

Grants will be awarded based on proposals that receive a score of 60
or more out of 100. The score comes from using the following weighted
set of [<span class="underline">support
categories</span>](#kix.brhaw07m3ptq). To influence the rewarding of a
grant, one must be a [<span class="underline">standing
party</span>](#kix.veu646u0nkzf).

Support is divided into a number of categories, and weighted
independently to limit opportunities for gaming.

1.  ### Grant Award Process

    1.  Grants will be awarded on a regular cadence. The Standing
        Parties will define the cadence of the Grant process.

    2.  Grants are awarded and distributed in accordance with [<span
        class="underline">Doc 107 - Factom Grant
        Process</span>](https://factomize.com/forums/documents/doc-107-factom-grant-process.76/).

2.  Ongoing Governance Grants 
    -------------------------

The protocol needs to support a number of activities to maintain the
protocol in an ongoing fashion. These grants to maintain ongoing
operations of the protocol take precedence over other grants which
improve the protocol.

### Anchor master

The anchor master project would fund the development, maintenance, and
execution of the code to build and write anchors into Bitcoin,
Ethereum, and other chains. At the same time, an independent anchor
monitor should be funded to inspect and report on the performance of
the anchor master.

Details of how to define and manage these roles can be refined over
time. Issues to consider in more detail:

-   Varied cost of anchoring

-   Pricing of the roles

-   Number of supported chains, and those costs

-   Redundancy in the event of failures

-   Number and responsibilities of anchor monitors

    1.  ### Oracle Master

Exchange rates for FCT to Entry Credits are important in order to
maintain a target price for entry credits of 1/10 of a cent. As
determined by the Standing Parties and the Authority Set, the Oracle
Master will record into Factom relevant market information to
establish the trading price of Factoids.

Guide Remuneration Grant
------------------------

Guides are compensated via the grant pool.

Token Supply
============

The Token supply will grow through a fixed set of awards that amounts
to a 10% inflation of the Factoid supply in the first year, without
considering usage of the protocol (which burns Factoids).

The protocol support budget is fixed at about 72933.12 tokens per
month, where a month is defined as 4383 blocks. (365.25\*24\*60 / 10 /
12)

In many blockchains, Proof of Work accounts for much of the rewards
issued for the security of the blockchain. In other words, most of the
resources are expended on energy costs rather than development,
maintenance, and infrastructure. As the protocol uses anchoring,
resources can be expended on a sort of “Proof of Development,”
extending and developing the protocol and the ecosystem around the
protocol. This is the motivation around the Grant Pool design.

1.  Token Rewards
    -------------

    1.  The Protocol issues tokens for each server in the Authority Set.
        The issuance would be fixed at .256 Factoids per Authority
        Server per block. If one assumes a year to be 365.25 days, 10
        minute blocks, and 65 servers in the authority set, then
        72933.12 tokens will be created per month, and 874,598.4
        tokens per year. This is roughly a 10 percent inflation rate
        for the first year of token distribution.

2.  Grant Pool Allocation
    ---------------------

    1.  While Authority Servers can specify all 0.256 Factoids be issued
        by the protocol, these servers compete to provide lower cost
        service to the protocol. As such, a server can specify a lower
        share, say 0.2 Factoids, or 0.13 Factoids per block.

    2.  Tokens not distributed to an authority server are allocated
        instead to the grant pool.

3.  Authority Set Veto
    ------------------

    1.  The Coinbase transactions, and thus all issuance of new Factoids
        can be vetoed by a majority of the Authority Set. Due to
        protocol bugs or issuance of Factoids that would be
        detrimental to the protocol, the Authority Set can prevent a
        particular pending Factoid issuance.

    2.  Coinbase issuances are proposed 1000 blocks (normally \~7 days)
        before they become active in the Factoid block. The majority
        of the Authority Set can cancel any output in any coinbase
        between when it is proposed and when it is issued.

    3.  The majority of the Authority Set would create digital
        signatures to specify a coinbase output to cancel. If a
        majority of the Authorities at the time publish their
        signatures on the blockchain, the specified output will not
        appear in the Coinbase.

    4.  The balance of the canceled Coinbase is returned to the Grant
        Pool to allow an orderly rectification of the error at a
        future time.

    5.  Information about how to execute coinbase cancellations can be
        found in [<span class="underline">Doc 203 - Cancellation of
        coinbase
        outputs</span>](https://docs.google.com/document/d/1P7w_M8QSU3Z3GUftx4AMWR_jHXkcPgenFgM0wdOFMHc/edit?usp=sharing).

Standing Parties
================

A Standing Party (one that has standing in the protocol to vote in a
protocol process) must qualify in some way. The protocol has a number
of mechanisms to define Standing Parties.

Factom uses [<span class="underline">DPoS</span>](#kix.5okwvpiloppf)
to define the Standing Parties and how support is collected and
measured. This is done by defining how the [<span
class="underline">PoS</span>](#kix.chafrfq6l9io) is defined, then how
 it is distributed.

PoS is not as simple as it might first seem. When people can use
tokens to stake to make decisions, the game theory is complex, with
many unintended outcomes and incentives.

Factom intends to use a number of distinct categories that combine to
define a voting weight for various issues within the protocol. The
idea is to introduce tradeoffs that can be adjusted to ensure
behaviors like bribery and influence pooling does not yield the
optimal outcome for individuals.

Some categories like Efficiency and Entry Credit purchases seek to
provide influence to parties actively engaged in using and running the
protocol. The value of these activities is ranked high at the time of
execution, and reduces over time. Other categories like staking tokens
provide influence to those willing to commit resources to the
protocol. As time goes on, staking gains influence as long as the
tokens are not touched.

The interesting observation is that each of the categories that tend
to either burn tokens (EC buys) or relinquish tokens (Efficiency) get
their influence up front because once committed, the tokens are not
available to the Standing Party. On the other hand, Staking provides
the tokens to the Standing Party, so they are not lost. The value to
the protocol is in keeping them staked, so their influence grows over
time.

Tokens can not be used for multiple categories, by their nature. You
can’t leave tokens in the grant pool, and stake them. Or buy Entry
Credits with them. And a bribe removes the tokens from your control,
and can only gain influence if other parties are not engaged in such
behavior.

1.  Requirements for a Standing Party
    ---------------------------------

    1.  A standing party has a digital identity.

    2.  The digital identity must have an entry that defines a voting
        signature. This voting signature can be changed by a properly
        signed entry with one of the digital Identity’s signing keys.

    3.  The digital identity must be registered in the Standing Party
        Registration chain.

    4.  A Standing Party must have one or more categories of support.

2.  Support Categories
    ------------------

Each Standing Party has a number of categories of support. For voting
for different processes, these categories can be weighted differently.
This is a matter to be determined.

The following sections detail each of the possible support categories.

1.  ### Support category: Proof of stake

    1.  To collect support from proof of stake, tokens are assigned to
        the standing party chain via a properly formed entry that
        details the address holding the tokens, and is signed by that
        address.

    2.  #### Retrospective staking

        1.  Any change to the tokens at that address invalidates the
            proof of stake vote. An address can only be staked once.
            To be staked again, the tokens must be moved to a new
            address, which has not been staked to any standing party.

        2.  Tokens allocated to a proof of stake address assigned to a
            standing party will accrue additional voting weight equal
            to 5% of the original token count each month they are left
            in the proof of stake address until 24 months. After 24
            months, no further weighting will accrue. (Note:
            Additional tokens will not accrue, just additional voting
            power.)

    3.  #### Prospective Staking

        1.  Tokens can be sent to an address which doesn’t allow tokens
            to move from it for a predefined period of time.

        2.  Token locking functionality is not yet implemented in the
            protocol. The need and implementation schedule for token
            locking will be developed in Q2 of 2018.

2.  ### Support category: Proof of use

    1.  To collect support from proof of use, entry credit purchases are
        assigned to the standing party chain via a properly formed
        entry that details the entry credit address, and properly
        signed with the entry credit address.

    2.  At the point of purchase, entry credits bought are weighted at
        100%. With each month, the weight of an entry credit purchase
        is reduced by 20%, such that entry credits purchased more than
        six months back provides no support.

3.  ### Support category: Guide

    1.  A Guide is a protocol identity, and a properly formed Guide
        identity has a voting signature. Being a Guide is a category
        of support.

4.  ### Support category: Authority set

    1.  An authority server is defined by a digital identity, and a
        properly formed authority identity has a voting signature.
        Being an authority server is a category of support.

5.  ### Support category: Efficiency 

    1.  Additionally, an authority server can specify an award of less
        than the maximum tokens issued to authority servers. Doing so
        is an indication of efficiency, and the unclaimed tokens are
        diverted to the [<span class="underline">Grant
        Pool</span>](#kix.qj0sc7dzt717).

    2.  Calculating the value of support for efficiency uses a sliding
        scale with those levels of efficiency (the difference of the
        draw and the maximum token issue) in the last 30 days weighted
        at 100%. With each month, the weight of efficiency is reduced
        by 20%, such that efficiency greater than six months back
        provides no support.

    3.  Efficiency support is calculated on the number of tokens left to
        the grant pool. An authority server’s ability to earn
        efficiency support is capped at 50%. An authority server can
        earn efficiency up to a maximum of 50% of the maximum tokens
        budgeted for an authority server.

### 6.2.6 Support category: Contribution

- **6.2.6.1**  This is a theoretical idea, but for which we have no solution as
             of yet.

- **6.2.6.1**  We may consider mechanisms for contributing to the grant pool
             without being an authority server. This is more complex from
             an accounting/legal perspective.

- **6.2.6.1**  We may consider mechanisms for creating grant weight for direct
             support of protocol advancements, infrastructure development,
             conference sponsorship, protocol promotion, business
             development, security improvements, etc. This is hard because
             these activities are in the real world, not within the
             protocol.

## 6.3. Delegation

Delegation allows parties that don’t have too much influence to lend
their influence to parties that can spend more time thinking and
researching issues regarding the protocol.

The disadvantage is the possibility of forming cartels and political
parties. Bribery, regional conflicts, and other disruptions are
encouraged when people can form stronger political movements in an
organization than they can as individuals. We see this in governments
today with entrenched political parties. Voting outside the parties is
considered by most as a waste of time.

### 6.3.1 Delegation Process

An individual’s standing is defined by their digital identity and
entries on that digital identity that provide cryptographic proof of
stake, Entry Credit purchases, Efficiency, etc.

Delegation is done by a Digital Identity signing and adding a
delegation record entry in the receiving Digital Identity. This entry
includes a numbered weight of each category. The support is withdrawn
by adding a withdrawal entry added to the receiving Digital Identity.

### 6.3.2 Delegation Penalty

When standing is delegated, it loses some of its voting power as
follows:

- 10% from an original Standing party to another.

- 20% from a second party to a third.

- 30% from a third to a fourth.

- 30% on any additional delegation.

The purpose is to make individual support more powerful than the same
Standing Parties would be if they delegated their support.

# 7. Amendments and additional community documents

**7.1** This Factom Governance Doc 001 is a living document that will
        need to be amended on a regular basis. Amending it shall only
        be executed in accordance with the process described in [<span
        class="underline">Doc 002 - Administration of Governance- and
        community documents</span>](https://factomize.com/forums/documents/doc-002-administration-of-governance-and-community-documents.47/).

**7.2** Additional Factom governance and community documents shall be
        created and administered in accordance with the procedures set
        forth in Doc 002.
