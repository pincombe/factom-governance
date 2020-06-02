**FACTOM**

**PROTOCOL**

**M3 Rollout Plan & Procedure**

**DOC 005**

<table>
<thead>
<tr class="header">
<th>VERSION</th>
<th>DATE</th>
<th>CHANGED BY</th>
<th>CHANGES</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0.1</td>
<td>2018-04-28</td>
<td>Brian Deery</td>
<td>First draft</td>
</tr>
<tr class="even">
<td>0.2</td>
<td>2018-04-28</td>
<td>Tor Hogne Paulsen</td>
<td>Applied standard formatting and drafted introduction. Proposed timeline and Authority Set population scheme.</td>
</tr>
<tr class="odd">
<td>0.3</td>
<td>2018-04-29</td>
<td><p>David Chapman, Brian Deery &amp;</p>
<p>Niels Klomp</p></td>
<td>Add references, uniform names for operators and authority sets. Extra install instructions. Added fallback procedure if a leader isn’t ready. Added reward start height.</td>
</tr>
<tr class="even">
<td>0.4</td>
<td>2018-05-21</td>
<td>Tor Hogne Paulsen</td>
<td>Changed table in chapter 5.</td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

1.  # Introduction and Scope
    
    1.  > This document describes the envisioned and planned process of
        > distributing control of the Factom Network to the broader
        > Factom community represented by a planned set of 65 Authority
        > Nodes.
    
    2.  > The status as of the writing of this document (2018-04-29) is
        > that Factom Incorporated hosts and controls all 18 of the
        > current Factom Network Authority Nodes. They are running on
        > v0.4.2.22. M3 factomd is v 5.0.0.
    
    3.  > The intended end-state for the Factom Network is to include 65
        > Authority Nodes, and upon reaching that goal this document
        > will be retired.

2.  # Proposed Timeline

| **Phase** | **Task**                                                  | **Description**                                                                                                          | **Planned date** | **Executed** | **Reference** |
| --------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------- | ------------ | ------------- |
| 1         | New code deployment                                       | Factom Inc. deploys M3 code on mainnet                                                                                   | 2018-04-30       | No           | 3.3.          |
| 2A        | Follower nodes deployed by operators                      | Operators: deploy follower nodes on mainnet                                                                              | Continuous       | Ongoing      | 3.4.2.1.      |
| 2B        | Test Portainer network                                    | Connect some follower nodes to portainer network                                                                         | 2018-04-30       | No           | 3.4.2.2.1.    |
| 2B        | Test Portainer network                                    | Convert the Testnet Leaders over to Portainer based docker images.                                                       | 2018-05-01       | No           | 3.4.2.2.2.    |
| 2B        | Test Portainer network                                    | Test Portainer System (start/stop/control) on testnet                                                                    | 2018-05-01       | No           | 3.4.2.2.3.    |
| 2B        | Test Portainer network                                    | The first 10 Operators outside Factom Inc. install docker-based M3-code for Mainnet and connect to the portainer system. | 2018-05-02       | No           | 3.4.2.2.5.    |
| 2B        | Test Portainer network                                    | Test Portainer System (start/stop/control) on mainnet, as well as brain swap if available.                               | 2018-05-02       | No           | 3.4.2.2.6.    |
| 2C        | New Factoids are created                                  | Promotion of the first operator outside factom inc. to the Authority Set.                                                | 2018-05-03       | No           | 3.4.2.3.1.    |
| 2C        | Start adding more entities                                | Start populating the Authority set with the remaining selected Authority Set Operators                                   | 2018-05-04       | No           | 3.4.2.3.4.    |
| 3A        | Server rewards begin                                      | Authorities contributing on this date are rewarded with new Factoids                                                     | 2018-05-10       | No           | 3.5.1.        |
| 3B        | Create software for adding FCT-address and set efficiency | Allow identities to be created which support receiving coinbase FCT                                                      | TBD              | No           | 3.5.2.        |
| 3C        | Operators creating and populating identities              | Identities and secret keys (lvl 1-4) needs to be created in a safe manner by all Authorities                             | TBD              | No           | 3.5.3         |

3.  # Rollout phases
    
    1.  > Factom Milestone 3 (M3) has 3 distinct objectives that will
        > happen in 3 different overlapping phases:

> **Phase 1** - <span class="underline">Objective</span>: New code
> deployment
> 
> **Phase 2** - <span class="underline">Objective</span>: Distribution
> of control
> 
> **Phase 3** - <span class="underline">Objective</span>: New Factoids
> are created

2.  > The phases have different requirements and timelines

3.  > Phase 1 - New Code Deployment
    
    1.  > The Factom network is going through a non-reverse compatible
        > software change after a year of maintaining backwards
        > compatibility. This is similar to a hard fork. Phase 1 is
        > scheduled for Monday April 30, 2018.
    
    2.  > Follow progress at
        > [<span class="underline">https://status.factom.com/</span>](https://status.factom.com/)
    
    3.  > Non-upgraded nodes will not see new blocks. There are no
        > groups that will maintain the older software. This is not an
        > airdrop, spinoff, coin swap, or contentious fork. It uses the
        > same genesis block and chain history as before.
    
    4.  > <span class="underline">Wallets will continue to operate
        > without upgrading.</span>
        
        1.  > After the upgrade, both *Enterprise Wallet* and the API
            > wallet *<span class="underline">factom-walletd</span>*
            > will continue to operate normally against updated factomd
            > nodes.
        
        2.  > There will be an upgrade window for the courtesy node
            > provided by Factom Incorporated, which powers the
            > *Enterprise Wallet* by default. After the upgrade window
            > Monday, Enterprise Wallet will resume normal operation.
        
        3.  > No existing FCT balances will change by this upgrade. Only
            > wallet users who run a full node will have to take action.
            > Note the Upgrade Procedure below.

4.  > **Phase 2** - **Distribution of control**
    
    1.  > This phase is about replacing the control of the network with
        > disparate parties.
    
    2.  > The goals for Phase 2 are:
        
        1.  > <span class="underline">**2A**) Prepare Selected Operators
            > as M2 follower nodes</span>
            
            1.  > Selected Operators can begin downloading the M2
                > blockchain to prepare for installing M3 docker code on
                > their mainnet servers. This would mean installing the
                > latest M2 release from
                > [<span class="underline">https://github.com/FactomProject/distribution</span>](https://github.com/FactomProject/distribution)
                > or from source
                > https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md.
            
            2.  > Besides running the M2 factomd, no additional
                > configuration is needed. The M2 database can be
                > installed in a M3 docker volume to speed up the
                > bringup process. Never use the M3 Testnet database as
                > a starting point\!
        
        2.  > <span class="underline">**2B**) Test Portainer network
            > reset</span>
            
            1.  > Convert some of the Testnet followers to connect into
                > the Portainer system and test bringing the followers
                > up and down.
            
            2.  > Convert the Testnet Leaders over to Portainer based
                > docker images.
            
            3.  > Test the start/stop/remote control abilities of the
                > Portainer system on Testnet.
            
            4.  > Relevant links:
                
                1.  > [<span class="underline">https://github.com/portainer/portainer</span>](https://github.com/portainer/portainer)
                
                2.  > [<span class="underline">http://demo.portainer.io/</span>](http://demo.portainer.io/)
            
            5.  > The 10 (or however many are ready) non-FactomInc
                > Operators will install the docker based M3 code for
                > Mainnet and connect into the Portainer system as
                > followers.
            
            6.  > The ability to reboot the nodes (while acting as
                > followers) will be tested on Mainnet.
            
            7.  > Alternate node types (i.e. for brain swap) should be
                > tested if available.
        
        3.  > <span class="underline">2C) New M3 Leaders are
            > created</span>
            
            1.  > Thursday May 3 - The first of the Selected Operators
                > will be promoted to a Federated server ( total number
                > for promotion TBD).
            
            2.  > This will give some time to ensure that a poor
                > connection will result in the leader being faulted out
                > if it goes poorly.
            
            3.  > This step will be informed by the progress of phase 3
                > for the various Operators. They should have an
                > identity with a factoid address and efficiency before
                > promotion.
            
            4.  > More entities are brought into Authority set.

5.  > Phase 3 - New Factoids are created

> Coinbase transactions will be non-zero.

1.  > <span class="underline">3A - Authority Node rewards will not begin
    > until until block \#140200, which is expected around May 10, 2018.
    > This date is when it is planned for Guide nodes make up a minority
    > of the Authority set. New Factoids will be created in the coinbase
    > 1000 blocks later at \#141200.</span>

2.  > <span class="underline">3B - Create software for adding FCT
    > address and efficiency</span>
    
    1.  > There exists software for the testnet to add efficiency and a
        > FCT address, but it was quickly spun up as a server side
        > crypto library.
    
    2.  > It should not be trusted for determining production payouts.
    
    3.  > Only offline or locally run software should deal with identity
        > key operations.
    
    4.  
3.  > <span class="underline">3C) Operators should make identities and
    > populate to the blockchain</span>
    
    1.  > This is tested on the testnet. Operators should make secure
        > paper copies of their identity keys, ideally using offline
        > computers with ephemeral CD bootable linux machines.
    
    2.  > This may not be possible for many operators, so avoiding
        > saving the key to the HDD might be the best that they can do.
    
    3.  > Note, if enough of the operators identity keys get
        > compromised, it can result in a systemic risk for the Factom
        > network.
    
    4.  > It is not merely their own factoids that these leaders are
        > protecting. Please be careful with identity keys. They are
        > arranged in a hierarchy, so higher numbered keys can replace
        > lower level keys (note, this key replacement is not
        > implemented in factom yet, so only key 1 is viable at this
        > point).
    
    5.  > The existing factom inc identities do not have items in their
        > identity which specify efficiency or a factoid address. This
        > means that they are considered 100% efficient, and no coinbase
        > payouts will happen for them. Factom Inc will not drop below
        > 100% efficiency for it’s two nodes until after other parties
        > control a majority of the Authority set. Factom Inc will not
        > get a disproportionate number of new Factoids.

<!-- end list -->

4.  # M3 related procedures
    
    1.  > Upgrade Procedure for followers
    
    2.  > These instructions are for normal users of factomd, like
        > businesses writing to the blockchain, exchanges, wallet users
        > with a full node. These nodes are also referred to as Follower
        > nodes. Authority Node operators have a different procedure
        > documented elsewhere.
    
    3.  > After v5.0.0 is pushed to the Master branch, upgrades should
        > be made. Watch
        > [<span class="underline">https://status.factom.com/</span>](https://status.factom.com/)
        > for Phase 1 upgrade progress.
    
    4.  > Link to Factomd:
        > [<span class="underline">https://github.com/FactomProject/factomd</span>](https://github.com/FactomProject/factomd)
    
    5.  > Built from source
    
    6.  > Warning: Please do not build Factomd on your production
        > servers\! Use another machine to build Factomd. You don’t want
        > compilers on production servers.
    
    7.  > Golang 1.10 or above is recommended for factomd. To check your
        > golang version, in a terminal run **go version**. Some OS
        > distributions supply out of date golang versions.
    
    8.  > These instructions will guide a user through the compilation
        > steps for factomd
        > [<span class="underline">https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md\#install-factom</span>](https://github.com/FactomProject/FactomDocs/blob/master/installFromSourceDirections.md#install-factom)
    
    9.  > Prebuilt Binary Installers
    
    10. > Installers for Debian/Ubuntu and Windows will be available
        > within a day or two after release.
    
    11. > [<span class="underline">https://github.com/FactomProject/distribution</span>](https://github.com/FactomProject/distribution)

5.  # Authority set population
    
    1.  > Authority Set Node Operators (“Operator”) will be included in
        > the Authority Set by their internal ranking provided by the
        > Authority Set Application Process(es). This process is
        > described as “Promotion”.
    
    2.  > If an Operator is not ready to be promoted when it is their
        > turn, the next Operator in the sequence will be offered to be
        > promoted instead and the team that was not ready will drop to
        > the bottom of their 11 or 21 queue. As such, teams should be
        > ready at least a couple days ahead of their scheduled rollout
        > or they may be dropped to the end of the queue.
    
    3.  > The Operator is required to follow the process described in
        > *Doc 110 - Process for including a new entity in the Authority
        > Set*.
    
    4.  > The table below describes the tentative dates for promotion
        > into the Authority Set. Note that this table will undergo many
        > revisions depending on a large number of fluid factors. Also
        > note that Operators that has been promoted to the Authority
        > Set is designated by green cell color.

| **Operator name**                  | **Onboarding group number** | **Tentative date for promotion** |
| ---------------------------------- | --------------------------- | -------------------------------- |
| Factom Inc.                        | \# 0                        | Promoted                         |
| Blockchain Innovation Foundation   | \# 1                        | Promoted                         |
| Factomize LLC                      | \# 1                        | Promoted                         |
| Go Immutable                       | \# 1                        | Promoted                         |
| The Factoid Authority (TFA)        | \# 1                        | Promoted                         |
| DBGrow Inc                         | \# 1                        | Promoted                         |
| Matter of Fact, LLC                | \# 1                        | Promoted                         |
| LUCIAP                             | \# 1                        | Promoted                         |
| Block Party                        | \# 1                        | Promoted                         |
| Federate This                      | \# 1                        | Promoted                         |
| Factoshi                           | \# 1                        | Promoted                         |
| Building Innovation Management Ltd | \# 2                        | Promoted                         |
| HashnStore                         | \# 2                        | Promoted                         |
| CryptoVikings                      | \# 2                        | Promoted                         |
| LayerTech (prev: NX Capital)       | \# 3                        | Promoted                         |
| Canonical Ledgers                  | \# 3                        | Promoted                         |
| RewardChain                        | \# 3                        | Promoted                         |
| Blockrock Mining AS                | \# 4                        | Promoted                         |
| SyncroBlock                        | \# 4                        | Promoted                         |
| Factomatic LLC                     | \# 4                        | Promoted                         |
| Stamp-IT                           | \# 4                        | Promoted                         |
