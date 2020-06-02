**FACTOM**

**COMMUNITY**

**Emergency Alert System**

**DOC 142**

| VERSION | DATE       | CHANGED BY        | CHANGES       |
| ------- | ---------- | ----------------- | ------------- |
| 0.1     | 2018-07-16 | Samuel Vanderwaal | First version |
|         |            |                   |               |
|         |            |                   |               |
|         |            |                   |               |
|         |            |                   |               |
|         |            |                   |               |
|         |            |                   |               |

# Introduction

The Factom community has a Discord bot running as an Emergency Alert
System that is capable of contacting all ANOs via their preferred
emergency communication medium to alert them of network issues that
require immediate attention and intervention. This document describes
the system and the process for using it.

# System

The Emergency Alert System is a Discord bot created by Stuart Johnson of
The Factoid Authority used for monitoring ANO nodes and performing
operations alerting and scheduling. It has emergency alerting features
built-in that make it suitable for the general alert system required by
the Factom Guides and technical committee.

The bot runs on a server and requires integration into a Discord server
and/or specific channel. It uses a Google Document for configuration
purposes. Instructions for setting up and installing the bot can be
found
[<span class="underline">here</span>](https://docs.google.com/document/d/1asksY8HIHxrJkylmi7xXT6TW0QT72gzOp0jzFgIjbQA/edit).

# Procedure

## General Procedure

The Core, Tech and Code Committee is responsible for investigating
network issues and determining their status and severity levels and what
action is required to be taken to resolve them. If the committee, after
being informed about an issue, has investigated it and determined that
it requires immediate response from all ANOs, they shall issue an
Emergency Alert via the system. Factom Guides are the other entity
responsible for issuing alerts.  
  
Pragmatically, anyone with access to the Discord \#operators-alert
channel can trigger the Emergency Alert by posting the word “EMERGENCY”
to the channel. The bot picks up this keyword and dials all phone
numbers in its user configuration sheet. In addition, any other bots
monitoring that channel for the alert keyword will be triggered to
respond in ways they were programmed internally by their specific ANOs.
In practice and socially, only the Core, Tech and Code Committee and
Factom Guides should initiate emergency alerts.  
  
The system configuration sheet has the chosen preferred ANO contact
options. Messages will be disseminated in the following manner:

\- To ANOs that prefer being alerted via a telephone message: A call is
automatically initiated to their one (1) listed telephone number.

\- To ANOs that prefer being alerted via their own Discord BOT: An
alert-message that triggers the individual ANOs own discord bot is typed
in \#operators-alerts.

ANOs who receive the Alert message will know a priori to respond by
checking the Discord \#operators-technical channel and begin
coordinating the appropriate response actions.

Individual ANOs can be alerted by using the keyword associated with them
in the “KeywordAlert” column of the ANO-Bot Config Google Sheet
available in a restricted Google Drive folder. E.g. posting
“CANONICALLEDGERS” in the \#operators-alerts channel on Discord will
trigger an alert only to Canonical Ledgers by calling their number
listed in the configuration Google Sheet.

## ANO Expectations

ANOs should maintain updated contact info available to the Guides and
the Core, Tech and Code Committee by filling out and keeping updated
[<span class="underline">this
form</span>](https://drive.google.com/open?id=1Jwvks9H-zuf-JNSyHi-bXZlzdlKPn6hlqkdq9k6IPC0).
The form requires a Google account to access and allows for information
to be updated via the same Google account. To update the form, click on
the “Edit your response” link when presented with this window:

![](.//media/image1.png)

You will then be presented with your filled-out form and be able to edit
the fields to update your information.

![](.//media/image2.png)

Click the “Submit” form once you are finished updating the information.

ANOs who use a bot for their alert method should keep it running with
high uptime and ensure that its trigger contacts ANO members reliably.
ANOs who use a phone number for their alert method should ensure that
they can reliably receive calls from the Factom Alert system. If useful,
ANOs can whitelist the number the Factom Alert system uses to ensure it
gets through. Contact the Guides if you need the number for
whitelisting.

Upon receiving an Emergency Alert System in any form, the ANOs should
endeavour to respond to it within two hours by checking in on the Factom
Community Discord \#operators-technical and \#operators-chat channels to
find out further details of the emergency and what required action they
are to take.
