**FACTOM**

**COMMUNITY**

**Authority Server**

**Minimum Specifications**

**DOC 202**

| VERSION | DATE       | CHANGED BY          | CHANGES        |
|---------|------------|---------------------|----------------|
| 0.1     | 2018-04-17 | Niels Klomp         | First draft    |
| 1.0     | 2018-04-17 | Tor Hogne Paulsen   | First version  |
| 2.0     | 2019-09-30 | The 42nd Factoid AS | Second version |
|         |            |                     |                |
|         |            |                     |                |
|         |            |                     |                |
|         |            |                     |                |

1.  Introduction

Pursuant to section 3 of the Factom Protocol [<span
class="underline">Governance
Document</span>](https://factomize.com/forums/documents/doc-001-factom-governance.9/),

“Node technical specification” is a weighted variable in the Authority
Node

> election process. It is expected that Authority Node applicants meet
> at least Tier 1 technical specifications described below. An applicant
> that gets elected to the Authority set is expected to operate servers
> with technical specifications as described in the application.

1.  Technical specifications

> Technical specifications are described as three *tiers* where 1 is the
> minimum requirement and 3 is the best. The tiers are written in red
> text throughout this document.

### CPU

> We expect at least a Intel Xeon or equivalent CPU that is no older
> than 3 years. We choose not to opt for specific CPU names or versions,
> since Factom needs a performant CPU, but it is not the most important
> part of a good performing Auth node. Instead we focus on the amount of
> cores dedicated to the Auth Node. Please note, that we are not talking
> about hyperthreading here. It means actual cores (dedicated or virtual
> backed by real cores).
>
> For cloud based providers, some plans throttle the amount of CPU
> capacity available to a running instance. This allows for efficient
> bursting capability, but for steady state operations will cause
> cascading problems if CPU usage is high. A cloud platform shouldn’t
> use an instance with CPU credits that diminish with use.

<table>
<thead>
<tr class="header">
<th><blockquote>
<p>CPU - Intel Xeon or equivalent</p>
</blockquote></th>
<th><strong>2 core</strong></th>
<th><strong>4 core</strong></th>
<th><strong>&gt;= 4 cores</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>1</td>
<td>2</td>
<td>3</td>
</tr>
</tbody>
</table>

### Memory

> The minimum required amount of memory for Factom is 8GB. This amount
> allows you to run Factom without problems, but it is strongly
> recommended to ensure more memory is available for Factom. We do not
> give a maximum amount, so if your machine has more memory than in the
> top column you will not score any extra points. Please note that
> Factom in itself will do with 8 GB of memory, but extra memory for
> caching is always beneficial for speedy operation of Factom and your
> node. Modern operating systems always benefit from more memory! Please
> note that extra points can be awarded when a machine can scale memory,
> but only when it is not in the top column already. The latter does not
> score you the full amount, since dedicated spare memory is always
> available, whilst scaling almost always requires a reboot.

<table>
<thead>
<tr class="header">
<th></th>
<th><strong>8-15 GB</strong></th>
<th><strong>16-23 GB</strong></th>
<th><strong>&gt;= 24 GB</strong></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Memory</p>
</blockquote></td>
<td>1</td>
<td>2</td>
<td>3</td>
<td></td>
</tr>
</tbody>
</table>

### Disk type

> Since Factom does a lot of reads and writes it benefits from disks
> with low latency and high throughput. We are not scoring based on raw
> numbers in this round of applications, but based on type of disks,
> since that roughly translates into speed categories.
>
> For cloud based deployments, when selecting a drive type, most of the
> time there are bursting types and the type which fully provisions
> access. In AWS parlance gp2 vs io1, with gp2 getting throttled with
> heavy usage. Using the bursting type of storage causes slowdowns when
> booting if for example the network needed to be started multiple times
> in a short period of time.
>
> Note: Factom Federated servers currently provision 600 IOPS

<table>
<thead>
<tr class="header">
<th></th>
<th></th>
<th>SAS</th>
<th>SSD</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Disk Type</p>
</blockquote></td>
<td></td>
<td>1</td>
<td>2</td>
</tr>
</tbody>
</table>

### Free disk size

> Although not directly a technical specification it is important to
> account for the (future) growth of the Factom database. We will take
> into account the amount of free space for the database to grow.
> Providing separate partitions or volumes for the Factom database adds
> bonus points, since other files like log-files or operating system
> files cannot get in the way of the Factom database.

<table>
<thead>
<tr class="header">
<th></th>
<th>50-99GB</th>
<th>100-199B</th>
<th>&gt;= 200 GB</th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Disk Size free for DB</p>
</blockquote></td>
<td>1</td>
<td>2</td>
<td>3</td>
<td></td>
</tr>
</tbody>
</table>

### Network uplink/interconnectivity

> On the Testnet Factom sometimes exceeds 10 Mbps and on average
> utilizes 1 to 2 Mbps. This means a 100Mbit connection will do for now.
> It is however the minimum uplink requirement for now. Please note that
> we are not only talking about the speed of the network interface card
> here. This has to be the minimum uplink speed to the internet! Since
> Gbit lines typically have lower latency and are better equipped to
> handle peak and future loads they score a little better.
>
> **<span class="underline">Static IPs is required</span>**, so reboots
> don’t throw off seeding, routing, and administration.

<table>
<thead>
<tr class="header">
<th></th>
<th>100 Mbit</th>
<th>&gt;= 1 Gbit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>Network speed (uplink not NIC only)</p>
</blockquote></td>
<td>1</td>
<td>2</td>
</tr>
</tbody>
</table>
