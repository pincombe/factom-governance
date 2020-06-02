**FACTOM**

**COMMUNITY**

**DRAFT**

**Authority Node update process**

**DOC 105**

| VERSION | DATE       | CHANGED BY        | CHANGES                       |
| ------- | ---------- | ----------------- | ----------------------------- |
| 0.1     | 2018-04-29 | Brian Deery       | Initial draft                 |
| 0.2     | 2018-05-23 | Tor Hogne Paulsen | Changed document name.        |
| 0.3     | 2018-05-23 | Steven Masley     | Added node update information |
|         |            |                   |                               |
|         |            |                   |                               |
|         |            |                   |                               |
|         |            |                   |                               |

1.  # Introduction
    
    1.  > This document describes the process for updating an Authority
        > Node to a new version. This document will refer to various
        > processes at a high level such as brain swapping, checking
        > node’s health, etc. These processes are described in
        > [<span class="underline">this
        > document</span>](https://github.com/FactomProject/factomd-authority-toolkit/blob/master/README.update.md)
        > at GitHub.
        
        1.  > The document linked should be read before continuing. If a
            > node operator is unfamiliar with any process in this
            > document
    
    2.  > There are three distinct update types (1-3, depending on
        > backwards- and future compatibility….)

2.  # Backwards Compatible Updates
    
    1.  > Backwards compatible updates do not have to be coordinated
        > synchronously. This means node operators can update at their
        > leisure. Most updates will also have a timeframe the update is
        > expected to be completed by depending on it’s severity.
    
    2.  > How to update:
        
        1.  > Before updating a node, the node should have no authority
            > identity attached to it. If the node has an identity,
            > perform a [<span class="underline">brain
            > transfer</span>](https://github.com/FactomProject/factomd-authority-toolkit/blob/master/README.update.md#1-brain-swapping--brain-transferring)
            > such that the node is without an identity
            
            1.  > The brain transfer should be to a node that has been
                > updated unless otherwise specified
        
        2.  > Factomd is run within a docker container. The update will
            > specify a version number, and a
            > [<span class="underline">docker
            > update</span>](https://github.com/FactomProject/factomd-authority-toolkit/blob/master/README.update.md#2-updating-factomd-docker-container)
            > with the new version

3.  # Height Activated Updates
    
    1.  > Follow the same instructions as a backwards compatible update,
        > making sure to update before the specified activation height

4.  # Non-Backwards Compatible Updates
    
    1.  > ???
