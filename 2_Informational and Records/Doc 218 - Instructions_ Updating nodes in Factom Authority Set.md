**FACTOM**

**COMMUNITY**

**Instructions:**

**Updating nodes in**

**Factom Authority Set**

**DOC 218**

| VERSION | DATE       | CHANGED BY                       | CHANGES          |
|---------|------------|----------------------------------|------------------|
| 1.0     | 2019-10-15 | The 42nd Factoid AS, Factom, Inc | Initial document |
|         |            |                                  |                  |
|         |            |                                  |                  |
|         |            |                                  |                  |
|         |            |                                  |                  |
|         |            |                                  |                  |
|         |            |                                  |                  |

1.  Introduction

    1.  This document’s purpose is to describe for ANOs how to
        > appropriately update factomd for nodes in the Factom Mainnet
        > Authority Set.

    2.  A general call for update will be announced by the Factom Core
        > Committee via appropriate channels, and will include as a
        > minimum the following relevant information:

        1.  New version designator (example: v6.4.3-alpine).

        2.  Date by which all ANOs are expected to have executed update.

> Note: Normally 7 days.

1.  A link to Doc [<span
    > class="underline">208</span>](https://docs.google.com/spreadsheets/d/1fopTNg7ZnokwybEwC6H7W3vEAmNMkyFd_3xumDj5q0Q/edit?usp=sharing)
    > (update tracking spreadsheet).

2.  **If applicable**: Information that the savestate file will be
    > rebuilt.

3.  **If applicable**: Information about activation height.

4.  **If applicable**: Requirement that Audit servers are updated prior
    > to federated servers.

5.  **If applicable**: Required update method (<span
    > class="underline">Alpha</span> or <span
    > class="underline">Bravo</span>).

6.  **If applicable**: Any other relevant information.

<!-- -->

1.  There are two ways of proceeding to update a factomd node in the
    > authority set, <span class="underline">and both may be used at
    > will if nothing else is specified</span> in the announcement:

    1.  **Method Alpha** *- “Brainswap”*

        1.  This method involves updating factomd via first moving the
            > associated Authority identity away to another factomd
            > node, and only then shutting down factomd to update it.

        2.  If the factomd node being updated is acting as a Federated
            > Server the Federated Server is preserved with the ANO when
            > proceeding via this method.

    2.  **Method Bravo** *- “Shutting down”*

        1.  Updating via Method Bravo involves shutting down the factomd
            > Authority node without first brainswapping away the
            > authority identity.

        2.  If the factom node being updated is acting as a Federated
            > Server, shutting it down will trigger an election within
            > the authority set, and the node will be downgraded to an
            > Audit Server.

<!-- -->

1.  Updating nodes (factomd)

    1.  **Method <span class="underline">Alpha</span>** - Updating via
        > Brainswap

        1.  The process of performing an upgrade manually via Method
            > Alpha is detailed [<span
            > class="underline">here</span>](https://docs.factomprotocol.org/authority-node-operators/ano-guides-and-tutorials/updating-and-brainswapping-your-node).

        2.  It is however recommended to use this automatic [<span
            > class="underline">Brainswap
            > Script</span>](https://github.com/Stamp-IT-io/brainswap)
            > to execute the update via this method, as it will perform
            > a host of automatic checks and verification to ensure the
            > brainswap is executed normally. After the swap is executed
            > then shut down and upgrade factomd, and then swap the
            > identity back again to the original server.

        3.  Confirm that you have updated the servers by proceeding to
            > tick the right boxes in [<span class="underline">Doc
            > 208</span>](https://docs.google.com/spreadsheets/d/1fopTNg7ZnokwybEwC6H7W3vEAmNMkyFd_3xumDj5q0Q/edit?usp=sharing)
            > (update tracking spreadsheet).

    2.  **Method <span class="underline">Bravo</span>** - Updating via
        > shutting down

        1.  Identify the correct time to shut down the Authority Node by
            > opening up the associated factomd control panel and locate
            > the following area on the “more detailed information”
            > page.

<img src=".//media/image1.png" style="width:5.07813in;height:0.49609in" />

1.  The red circle identifies which *minute* the node is on, and it
    > **<span class="underline">must be showing a minute between 3 and 7
    > (inclusive) when shutting down.</span>**

> Note: A network pause at the boundary between minute zero and one runs
> the risk of leaving the network in a non-restartable state. The blocks
> are saved to the database at the switch to minute 1 and if only some
> Federated servers save the block, restarting will require
> community-wide intervention.

1.  When the number shows a minute between 3 and 7, shut down the node
    > by stopping the docker container. Next upgrade the docker image
    > and restart.

> Note: Only shut down one Federated node per block to reduce risks of
> unintended consequences.

1.  Confirm that you have updated the servers by proceeding to tick the
    > right boxes in [<span class="underline">Doc
    > 208</span>](https://docs.google.com/spreadsheets/d/1fopTNg7ZnokwybEwC6H7W3vEAmNMkyFd_3xumDj5q0Q/edit?usp=sharing)
    > (update tracking spreadsheet).

Appendix A

Core Committee call for update template

Authority Node Operators,

Please update your factomd nodes to version: v10.0.0-alpine.

Updates should be completed by YYYY-MM-DD at XX:YY UTC.

After updating the nodes confirm that it has been successfully completed
in Doc 208 (link below). Please also specify what kind of nodes
(federated/audit) are associated with your identity/identities.

The factomd savestate file will/will not be rebuilt during this upgrade.

Please see Doc 218 below for instructions about how to update.

Doc 218 (Instructions for updating Factom Authority nodes):

\<[<span
class="underline">https://docs.google.com/document/d/1ak\_0i899Ix--ofKEfT32GmY5R7y2bWBSd3\_cFMSkd2Q/edit?usp=sharing</span>](https://docs.google.com/document/d/1ak_0i899Ix--ofKEfT32GmY5R7y2bWBSd3_cFMSkd2Q/edit?usp=sharing)\>

Doc 208 (Update tracking spreadsheet): \<[<span
class="underline">https://docs.google.com/spreadsheets/d/1fopTNg7ZnokwybEwC6H7W3vEAmNMkyFd\_3xumDj5q0Q/edit?usp=sharing</span>](https://docs.google.com/spreadsheets/d/1fopTNg7ZnokwybEwC6H7W3vEAmNMkyFd_3xumDj5q0Q/edit?usp=sharing)\>.

---------------------------------------------------------------------------------------------------------------

The following information should be included in the announcement as
applicable:

**If applicable**: During this update Audit servers should be updated
prior to federated servers, as we would prefer that
brainswapped/promoted (via faulting) servers becoming federated servers
are already updated.

Please only update audit servers for now. A new announcement will be
made when updates of federated servers are commencing.

**If applicable**: This release has an activation height of 123456789.
You must update prior to this height or risk being faulted out of the
authority set.

**If applicable**: There are two possible update methods described, and
during this update ONLY Method ALPHA/BRAVO shall be used. The reason for
this is XYZ.

**If applicable**: Any other relevant information.
