Title: Using Qbot with the-asf Slack channels

The Infrastructure team's **Qbot** is a Slack assistant that can simplify both important and frivolous tasks on Slack channels in the `the-asf` workspace. It can support requests in channels for PMCs, ASF committees, the ASF Board and `asfmembers`.

The name references the tool-maker who provides weapons and gadgets for Agent 007 in the James Bond movies.

## What Qbot can do
Qbot has an evolving set of functions:
  - Providing to the channel notifications related to your project's Jira tickets - new ticket, new comment, ticket resolved.
  - Starting a huddle in a channel workspace
  - Adding people to private channels

It also has a set of 'fun' features, such as rolling dice or flipping a coin.

## Setting up Qbot in your PMC's channels
If you want to have Qbot available in your PMC's channel, create a Jira ticket for Infra with the request. Include this information:
  - The name of the channel or channels where notifications about Jira tickets related to your projects should appear
  - How you want notifications to appear. There are five options:
      - No notifications
      - All notifications
      - `nodescription`: All notifications without the title of the ticket, but not its description
      - `nocomments`: No notifications of comments on tickets
      - `createclose`: Just notifications of ticket creation and resolution

  - Specify who can use the `addme` command -- committers, members of your PMC only, ASF Members only...

To have Qbot active in a project's private channel, once it is available in your public channels, someone already in the channel has to invite it with the Slack command `/invite @QBot`.
  

## Talking to Qbot
In Slack, there are three ways to talk to Qbot:

  -  Anywhere in the ASF workspace, type `/qbot` and the command you want to give it. If it is a command which you do not have permission to use where you currently are in Slack, the command will fail.
  -  In a channel where Qbot is present, type `qbot` without the slash, and the command.
  -  In the Slack interface, there is a general menu bar at the far left. The next column is the menu bar for the ASF workspace. At the bottom of the list of your contacts and channels, there is a section for `Apps`. Qbot appears there as.
        -  Click that entry to see a display with three tabs.
        -  Select the `Messages` tab.
        -  Write your command to Qbot without `/` or 'qbot` at the start.
        

## Qbot commands
**Note** we are expanding Qbot's reach, and this list will expand to match its capabilities.

  - `addme`- Add yourself to a private channel. (Without Qbot, you have to request in a Jira ticket that Infra do this.) The syntax is `/qbot addme <NAME OF CHANNEL>`.
  - `flip` - Qbot will flip a coin and tell you whether it came up heads or tails.
  - `help` - You will see a list of the available commands.
  - `q` - This command starts a huddle in your current channel, and makes you the administrator. The syntax is `/qbot q start`.
  - `queue` - Performs the same function as `q`. The syntax is `/qbot queue start`.
  - `roll` - Qbot rolls one six-sided die and reports the result.
      - You can roll up to ten dice at a time, and each die can have up to 100 sides or 'pips'.The syntax for a basic dice roll is `/q roll NdP`, where `N` is the number of dice (up to 10) and `P` is the number of surfaces each die has (up to 100): `/roll 8d12`.
      - In a role-playing game such as Dungeons and Dragons, when your character gets in trouble you may be able to try a **saving roll** to, well, save them from disaster. The syntax to see if Qbot can help in your current crisis is `roll saving`.
  - `shanty` - Qbot sings you a verse of a sea shanty.

## Requesting features
If you have an idea for a Qbot service that could help your PMC on Slack (or you just want to add a verse from another sea shanty), please suggest it in the <a href="https://github.com/apache/infrastructure-ideas/discussions/categories/qbot" target="_blank">Infrastructure-ideas repository</a>.
