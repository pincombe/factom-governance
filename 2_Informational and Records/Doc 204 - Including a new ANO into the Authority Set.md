**FACTOM**

**COMMUNITY**

**Process for including a new entity in the Authority Set**

**DOC 204**

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
<td>Tor Hogne Paulsen</td>
<td>First draft</td>
</tr>
<tr class="even">
<td>0.2</td>
<td>2018-05-09</td>
<td>Tor Hogne Paulsen / Steven Masley / Brian Deery</td>
<td>Second draft</td>
</tr>
<tr class="odd">
<td>1.0</td>
<td>2018-05-10</td>
<td>Tor Hogne Paulsen / Steven Masley / Brian Deery</td>
<td>Reorg with Github docs</td>
</tr>
<tr class="even">
<td>1.1</td>
<td>2018-05-17</td>
<td>Brian Deery</td>
<td>Added special peers, checklist</td>
</tr>
<tr class="odd">
<td>1.2</td>
<td>2018-06-14</td>
<td>Niels Klomp</td>
<td>Improve setup process, add missing info</td>
</tr>
<tr class="even">
<td>1.3</td>
<td>2018-06-21</td>
<td>Brian Deery</td>
<td>Created section to put identities on server</td>
</tr>
<tr class="odd">
<td>1.4</td>
<td><p>2018-08-27</p>
<p>2018-08-27</p></td>
<td>The 42ND Factoid</td>
<td>Added youtube tutorials courtesy Blockrock mining.</td>
</tr>
<tr class="even">
<td>1.5</td>
<td>2018-09-07</td>
<td>Sam Vanderwaal</td>
<td>Added link to and explanation of new Emergency Contact form in Section 9.</td>
</tr>
<tr class="odd">
<td>1.6</td>
<td>2018-10-19</td>
<td>Brian Deery</td>
<td>Added new IP for firewall.</td>
</tr>
<tr class="even">
<td>1.7</td>
<td>2019-05-27</td>
<td>Brian Deery</td>
<td>Removed IP for old firewall 52.48.130.243.</td>
</tr>
<tr class="odd">
<td>1.8</td>
<td>2020-02-20</td>
<td>The 42nd Factoid</td>
<td>Changed contact email at bottom of document.</td>
</tr>
</tbody>
</table>

1.  Introduction
    ============

    1.  This document describes the process for including a new entity
        > (operator) into the Factom network authority set.

    2.  Note that there are multiple YouTube-videos detailing some of
        > the processes throughout this document.

2.  Node setup Part 1

    1.  Install Docker

        1.  Make sure docker software is installed on your machine
            > following the info [<span
            > class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#install-docker).

> Note: There is a video detailing the steps
> [here](https://www.youtube.com/watch?v=Qghv05RCMcE).

1.  Configuring Ports

> The ports below need to be opened. The machine with IP-address
> 18.203.51.247 is the Docker Swarm Master machine currently used for
> the Authority nodes. See [<span
> class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#configure-docker)
> for more info.
>
> Note: There is a YouTube video detailing steps [<span
> class="underline">here</span>](https://www.youtube.com/watch?v=VIr9OT7ZRp0).

1.  **Incoming ports** (allow all from unprivileged ports, so higher
    > than port 1024 from the incoming connection)

    1.  <span class="underline">TCP/UDP port 2376</span> from <span
        > class="underline">18.203.51.247</span>. Secure Docker engine
        > communication (TLS) to the Docker Swarm Master communication
        > (TLS) to the Docker Swarm Master

    2.  <span class="underline">TCP/UDP port 2222</span> from <span
        > class="underline">18.203.51.247</span>. Database access (not
        > keys)

    3.  <span class="underline">TCP port 8088</span> from <span
        > class="underline">18.203.51.247</span>. API Access

    4.  <span class="underline">TCP port 8090</span> from <span
        > class="underline">18.203.51.247</span>. Control panel access

    5.  <span class="underline">TCP/UDP port 8108</span> from <span
        > class="underline">everywhere</span> (<span
        > class="underline">0.0.0.0/0</span>). Peer to peer
        > communication

2.  **Outgoing ports**. This is an advanced use case and optional, that
    > would protect your nodes better, **but means you really need to
    > know what you are doing**. Besides the ports mentioned below, you
    > would also need to open up ports for DNS, HTTP(s) and DHCP
    > probably. We advise you to enable all return traffic for existing
    > incoming connections (see above) and explicitly enable the ports
    > below.

    1.  <span class="underline">TCP port 2376</span> to <span
        > class="underline">18.203.51.247</span>. Secure Docker engine
        > communication (TLS) to the Docker Swarm Master

    2.  <span class="underline">TCP port 2377</span> to <span
        > class="underline">18.203.51.247</span>. Docker Swarm Master
        > remote management

<!-- -->

1.  Exposing the Docker Engine

    1.  Visit the github documentation to expose the docker engine
        > [<span
        > class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#exposing-the-docker-engine).

        1.  The documentation details a few ways to accomplish it.

2.  Setup docker volumes

    1.  Setup docker volumes for factomd database and factom.conf. The
        > instructions to setup the volumes are detailed [<span
        > class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#create-the-factomd-volumes).

3.  Create factomd config file

    1.  Make sure to download the factomd.conf file from [<span
        > class="underline">here</span>](https://github.com/FactomProject/factomd/raw/master/factomd.conf)
        > and store it in directory:
        > /var/lib/docker/volumes/factom\_keys/\_data/factomd.conf

4.  Add Special Peers to configuration

    1.  Add some special peers to your factomd config file by placing
        > the following line somewhere under the \[app\] line in your
        > config file.

    2.  MainSpecialPeers = "52.17.183.121:8108 52.17.153.126:8108
        > 52.19.117.149:8108 52.18.72.212:8108"

    3.  After completing step 2.8 and it works, on your control panel
        > you will see a little chain symbol next to the IPs, showing
        > them as special, meaning they will get election messages you
        > create.

5.  Get connected to the Swarm  
    > The swarm follows a synchronized reboot of the Factom network when
    > it stalls

    1.  Instructions to join the swarm can be found [<span
        > class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#join-the-docker-swarm).

6.  Lastly, Run factomd

    1.  Instructions to run factomd from the command line or GUI can be
        > found [<span
        > class="underline">here</span>](https://github.com/FactomProject/factomd-authority-toolkit#starting-factomd-container).

    2.  Please make sure to revisit point 2.6.3 and double check it.

<!-- -->

1.  Node setup Part 2

2.  Create and set up server identities

> Note: YouTube Tutorial for the steps below available [<span
> class="underline">here</span>](https://www.youtube.com/watch?v=g9FzNtSB7I4).

1.  **Requirements**:

    1.  <span class="underline">Entry Credits</span>

        1.  You can use these courtesy ECs to get bootstrapped:

> EC3VZedSyxGqch522oL9pVYBNjWwepuz61Vwm4Vupxcgh8Bfttpm

Es2bTzUy71xg24XVQNV7xcsJwDxRofeV84NEiRJ49RV7HmcaUEUV

1.  <span class="underline">Access to a full Factomd node,
    > factom-walletd, and factom-cli</span>

2.  <span class="underline">GoLang</span>

<!-- -->

1.  **Process**

    1.  Create and setup a server identity for each server you are
        > running. This will be two identities for the two servers that
        > the first Authorities will be running.

        1.  If you use the courtesy EC’s above, first check the balance
            > [<span
            > class="underline">here</span>](https://explorer.factom.com/addresses/EC3VZedSyxGqch522oL9pVYBNjWwepuz61Vwm4Vupxcgh8Bfttpm).

        2.  Run a copy of factomd locally synced to the blockchain.

> Note: You can edit some commands later if you want to use a different
> node, like the courtesy node, but that is less reliable.

1.  Download and build server identity program. The following are
    > directions for linux.

    1.  Install git, golang 1.10, and glide. Set the proper $GOPATH
        > environment variable.

    2.  <span class="underline">Clone the serveridentity program</span>:

    <!-- -->

    1.  \`mkdir -p $GOPATH/src/github.com/FactomProject/\`

    2.  \`cd $GOPATH/src/github.com/FactomProject/\`

    3.  \`git clone [<span
        > class="underline">https://github.com/FactomProject/serveridentity.git</span>](https://github.com/FactomProject/serveridentity.git)\`

    4.  \`cd serveridentity\`

    5.  \`glide install\`

    6.  \`go install\`

    7.  \`cd signwithed25519\`

    8.  \`go install\`

    9.  Copy $GOPATH/bin/serveridentity to an offline computer with a
        > thumbdrive

    10. On the offline computer run \`./serveridentity full elements
        > Es2bTzUy71xg24XVQNV7xcsJwDxRofeV84NEiRJ49RV7HmcaUEUV
        > -n=important -f\`

    11. It will create the files important.conf and important.sh

    12. Record the private keys printed out to the screen on paper or
        > long term storage. These are used to control your identity in
        > the future. Level 4 is the highest security and level 1 will
        > be used to do more operations.

    13. Copy the file important.sh, important.conf back to a thumbdrive
        > to run on an online computer. This will be added to your
        > \`factomd.conf\` file on the server.

    14. Make sure factomd is running

    15. Run factom-walletd in a terminal window (use
        > -s=courtesy-node.factom.com:80 if you don’t have a full node)

    16. The factom-cli commands in important.sh need to be directed to
        > the courtesy-node. Change all lines with \`factom-cli …\` now
        > read, \`factom-cli -s=courtesy-node.factom.com:80 ...\` (or
        > whatever factomd you are using)

    17. Import the EC address to your wallet: \`factom-cli importaddress
        > Es2bTzUy71xg24XVQNV7xcsJwDxRofeV84NEiRJ49RV7HmcaUEUV\`

    18. Check the balance \`factom-cli listaddresses\`

    19. Run the important.sh script.

    20. Check the explorer that the new identity chains were created 10
        > minutes later.

2.  Copy the identity to the Server

    1.  important.conf generated above will contain the lines like this:

<table>
<tbody>
<tr class="odd">
<td><p>IdentityChainID = 8888884c26a0a07780b0eb2adc77c3be534e5c1186ab058e278ee0b195ff56ce</p>
<p>LocalServerPrivKey = 57a0531c15ecf435b2e3d0a3402f1e7c8ac16e7f3672c108efbd50c9f9d64ee6</p>
<p>LocalServerPublicKey = 414686d2e1514db10d0ddbb77ac10f3cac27b9f2f53156542c1f644e10e0fb00</p></td>
</tr>
</tbody>
</table>

> Copy these lines your factomd.conf file on your server. It goes in the
> \[app\] section of the file. The file was put there in an early step
> at /var/lib/docker/volumes/factom\_keys/\_data/factomd.conf

1.  Make sure to keep a backup of these lines (as well as the level 1-4
    > keys from above) as those constitute your factom server digital
    > identity.

2.  Restart your factomd node to load the identities.

    1.  To check to see if it worked, open the control panel on port
        > 8090 of your server. Navigate to “more detailed node
        > information” \> “servers” \> “My Node”. It should show the
        > Identity ChainID and Signing Key that were specified in the
        > IdentityChainID and LocalServerPublicKey above.

<!-- -->

1.  Add factoid address and efficiency

> YouTube Tutorial for the steps below available [<span
> class="underline">here</span>](https://www.youtube.com/watch?v=Q9AXt0UHoHM).

1.  **Please wait until all 11 of the first Authorities are promoted.
    > Setting up the earlier identity is sufficient to be promoted to a
    > leader. Your identity will run at 100% efficiency until these
    > steps are run. Keep an eye on discord for an** **(automated)
    > announcement from the Standing Parties** **when to finish this
    > step.**

    1.  Download [<span class="underline">this
        > software</span>](https://github.com/PaulBernier/factom-identity-cli)

    2.  Boot into an operating system that can be started with an
        > internet connection but has the ability to be removed. A good
        > suggestion would be from a CD/USB or a ephemeral OS without a
        > hdd for best security.

    3.  [<span
        > class="underline">https://github.com/PaulBernier/factom-identity-cli/blob/master/offline-process-proposal.md</span>](https://github.com/PaulBernier/factom-identity-cli/blob/master/offline-process-proposal.md)

        1.  A fork is available under the carryforward GH user

    4.  \`cd factom-identity-cli/\`

    5.  ...

2.  Fill out form

Before being promoted into the Authority Set the operator has to supply
the necessary contact- and node-information via [**<span
class="underline">THIS
FORM</span>**](https://goo.gl/forms/prXcy2ZCL9mgSU043).

In addition, please us [**<span class="underline">this
form</span>**](https://goo.gl/forms/3c5CLp3GtEZ06kfz2) for filling out
your ANO’s emergency contact information. This second form can be
updated via the same link if your info changes in the future. It links
directly to the Emergency Alert bot configuration sheet, maintained the
Standing Parties or eligible (core) committees, so please keep the
information current.

1.  Checklist

    1.  During onboarding, these things will be checked by others. Some
        > of them cannot be checked by the operators themselves, but
        > some can be. Operators aren’t expected to use this checklist
        > themselves. This is not the master list, just a snapshot of
        > the one at time of authorship.

<table>
<tbody>
<tr class="odd">
<td><p>### Check ports</p>
<p>### Check individual ports</p>
<p>### Check Control Panel access</p>
<p>### Check that they are following minutes</p>
<p>### Check that they have the Special Peers</p>
<p>The control panel should show these IPs with a lock icon: 52.17.183.121 52.18.72.212 52.19.117.149 52.17.153.126</p>
<p>### Check that the IDs on the control panels match the submitted IDs</p>
<p>### Check logs</p>
<p>In portainer, make sure the docker logs don't show the server attempting to fault other servers</p>
<p>### Check startup flags</p>
<p>expecting `-startdelay=600 -faulttimeout=120 -config=/root/.factom/private/factomd.conf`</p>
<p>### Check reboot</p>
<p>in portainer, reboot the containers that are associated with the identity. Make sure they come up fine while watching the control panel.</p>
<p>### Check efficiency</p>
<p>https://github.com/Emyrk/factom-identity/tree/master/factom-identity-cli</p>
<p>factom-identity-cli -id=88888abcdef... -p</p>
<p>### Demote a factom inc server identity</p>
<p>If there are any left to demote</p>
<p>### Promote the server identity</p></td>
</tr>
</tbody>
</table>

### **NOTE: The Swarm cluster is still experimental, so please pardon our dust! If you have an issues, please contact steven at factom dot com.**
