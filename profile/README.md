> [!note]
> The team is now disbanded, see https://discourse.nixos.org/t/nixpkgs-architecture-team-conclusion-and-prospective/41020 for more info.

# Nixpkgs Architecture Team

The Nixpkgs Architecture Team is there to solve architectural nixpkgs issues that are too big in scope for any single person to undertake.

## Motivation

Nixpkgs is arguably the most valuable resource for Nix users. Its collection of packages is used by virtually every Nix user, private or commercially. However, there's continuous complaints by virtually every user of nixpkgs about various aspects, like missing documentation, difficulty of contributing, inconsistent interfaces and missing features. These problems need to be fixed eventually, doing nothing is not an option if Nix should be taken seriously as a universal solution for packaging.

The scale of nixpkgs has grown so considerably in recent years that it's not possible anymore for any single person to fix larger problems. And even if someone does manage to find a solution to a problem, there's nobody who can officially accept that solution and actually merge it. Over the years a number of improvements have been suggested and implemented, but most of them never made it to the finish line.

By creating a team tasked with the job of finding solutions to these issues it becomes much more feasible to actually do it.

## Goals

The primary goal of this team is to make interactions with nixpkgs a joy, so that it's easy and intuitive to use, learn and contribute to. The way in which this should be achieved is to fix problems in a clean, consistent and future-proof way. It should be ensured that nixpkgs is a solid and trustworthy foundation for the Nix community that can be relied upon.

The process in which this should be achieved is to gather and analyze critical feedback from users to find the root causes of problems. We will come up with solutions to these problems and evaluate them. Eventually we'll reach consensus and decide on a solution and turn it into reality. This is explained in more detail in the process section over on GitHub.

Since nixpkgs is widely used by third-party code, this team needs to be very careful to ensure reasonable backwards-compatibility. Backwards incompatible changes are only in scope after a deprecation window of an appropriate duration and accompanying warning.

Check out this GitHub board for an up-to-date list of issues that are being considered. If you have an idea for an issue that should be considered, please open a new issue and it will be automatically added to the board. 

## Process

This section describes the process of going from an issue to a solution. While described here as one, this shouldn't be a linear process. Instead this should be done in a feedback-oriented way.

Every issue considered by this team is tracked by [this project board](https://github.com/orgs/nixpkgs-architecture/projects/2).

The recommended way to track progress for a specific issue is to create a separate project board and fill it with nixpkgs issues.

### Problem statement

Before working towards a solution the team needs to figure out whether there even is a problem, what its suspected root cause is, and to clearly describe it. This is done with an issue in the main [project board](https://github.com/orgs/nixpkgs-architecture/projects/2)

### Solution exploration

The team should explore various potential solutions and figure out trade-offs with methods like:
- Developing prototypes
- Creating test cases
- Surveying the community
- Measuring performance

Specifically for nixpkgs, this includes all the past history, with all its approaches, refactorings, complaints and testimonies.

### Attempt at consensus

To decide on a solution, ideally consensus should to be reached among the team members. If consensus cannot be reached yet it can mean that there is a fundamental misundestanding or difference in values between team members. This should be reconciled by:
- Going back to solution exploration to find new alternatives or gather more information or support for arguments
- Trying to better understand each other by talking and listening
- Being willing to compromise

### Last resort: Voting

As a last resort, if still no consensus can be reached after everything has been tried, [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org) can decide to hold a vote to decide on the issue. The members that don't win in the vote should be accomodated to the best extent possible.

### Official RFC

In order to comply with the [Nix RFC process](https://github.com/NixOS/rfcs), after the team has reached consensus among themselves, an RFC should be created so the decision can be approved officially. Members of the nixpkgs team are encouraged to nominate themselves as [RFC shepherds](https://github.com/NixOS/rfcs#shepherd-team).

## Administration

### Team

As a team member you are expected to partake in the teams discussions by bringing in your expertise and opinions in order to steer the final decisions into the best direction.

While anybody is welcome to join the public nixpkgs architecture discussions, both to listen in or to bring their opinion, only the team members need to make decisions.

### Team Lead

The current team lead can be found [here](https://nixos.org/community/teams/nixpkgs-architecture.html).

The responsibilities of the team lead are:
- Making judgement calls when consensus cannot be reached among team members.
- Handle team administration such as:
  - Ensuring the meeting gets recorded, meeting notes get written and published
  - Implement the addition/removal of team members in the GitHub organization, private Matrix channel, the team log, and the NixOS homepage
- Staying informed on other team members current work
- Publicly representing the team in the Nix community and owning up to the teams mistakes

The team lead has the highest level of access to the teams infrastructure:
- Owner of the [GitHub organization](https://github.com/nixpkgs-architecture)
- Admin of the [public](https://matrix.to/#/#nixpkgs-architecture:nixos.org) and private Matrix rooms
- Owner of the [YouTube channel](https://www.youtube.com/@nixpkgs-architecture)

#### Current Team

See [here](https://nixos.org/community/teams/nixpkgs-architecture.html).

A log of the team modifications is available [here](https://github.com/nixpkgs-architecture/team-log)

#### Joining the team

The requirements for being part of the team:
- Having an interest in the large-scale architecture of nixpkgs
- Being reachable through [Matrix](https://matrix.org/), so that at least asynchronous communication is possible
- Being able to discuss with [reason](https://en.wikipedia.org/wiki/Reason), because only then it is viable to find consensus for decisions among a larger team

Additional strong recommendations:
- Be willing and available to have occasional synchronous audio/video meetings
- Have a GitHub account, allowing you to become part of the [nixpkgs-architecture](https://github.com/nixpkgs-architecture) organization for working on code together

The process of joining the team is as follows:
- Reach out to the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with your request to join the team. Feel free to tell us a little bit about yourself, such as:
  - Motivation for joining, what you're interested in discussing or working on
  - If you'd like to join the GitHub team, mention your GitHub user
  - If applicable and wanted, the company that sponsors time to work on this
  - Tell us what times you'd be available for audio/video meetings
  - If you want an automatically updating invite to the meetings, mention your email address
- A private discussion among the current team will take place as to whether you're accepted as a new team member
- The current team members will reach consensus on whether to accept the request and record that decision in the public [team log](https://github.com/nixpkgs-architecture/team-log) document, including all relevant arguments
- If accepted, [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org) will take these steps for adding you to the team:
  - Updating the team list [here](https://github.com/NixOS/nixos-homepage/blob/master/community/teams/nixpkgs-architecture.tt) with your entry and all relevant details
  - Adding you to the private Matrix channel for team members
  - If you want to join the GitHub team, adding your GitHub user to the [nixpkgs architecture](https://github.com/nixpkgs-architecture) organization
  - If you haven't joined the public meetings already, invite you

#### Leaving the team

All three requirements for joining the team are essential to the functioning of the team, therefore it is important to also make members not fulfilling them leave the team:
- Having an interest in nixpkgs architecture is important to be able to contribute to the team, otherwise there's no reason for somebody to be part of the team
- Being reachable through Matrix is needed because Matrix is the main communication channel for the team. You can't discuss without communication
- Being able to discuss with reason is essential for the team's ability to reach consensus on issues, otherwise no decisions can be made

If any requirement for being part of the team is not met anymore, the respective member should leave the team, ideally voluntarily.

If there is a hint that a team member doesn't fulfil the requirements anymore but doesn't leave voluntarily, here is how to proceed:
- Talk with other team members about it
  - This ideally also includes the respective team member themselves
- Try to reach consensus on whether any requirement is not being met anymore
- If consensus cannot be reached, reach out to [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org), who will make the final decision
- If the respective team member should be removed from the team, see below

The process for voluntarily or involuntarily removing a team member is done by [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org) and goes as follows:
- An removal entry is added to the public [team log](https://github.com/nixpkgs-architecture/team-log) including all relevant arguments for removal
- Removing the respective team member from the private Matrix channel for team members
- Remove the respective team member from the team list [here](https://github.com/NixOS/nixos-homepage/blob/master/community/teams/nixpkgs-architecture.tt)
- If applicable, removing the respective team member from the [nixpkgs architecture](https://github.com/nixpkgs-architecture) organization

### Code

Code developed for the nixpkgs team is generally committed under the [nixpkgs-architecture GitHub organization](https://github.com/nixpkgs-architecture).

### Communication

Team communication happens in mainly these forms:
- Continuously over text in the public [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel
  - There is also a private Matrix channel exclusively for team members for discussions that can't be shared publicly, like reviewing team member applications
- Regularly over audio/video in a meeting on Jitsi
- On Discourse for persistent discussions among the wider community, more end-user focused
- In GitHub comments for persistent discussions in the team and with nixpkgs developers
- Gathering design knowledge on [the wiki](https://github.com/nixpkgs-architecture/issues/wiki)

### Meetings

Meetings are held on [Jitsi](https://meet.jit.si/nixpkgs-architecture) and are fully public. Meetings are tracked as a calendar event in the public [NixOS Google Calendar](https://calendar.google.com/calendar/embed?src=b9o52fobqjak8oq8lfkhg3t0qg%40group.calendar.google.com&ctz=Europe%2FZurich). If you're interested in participating (whether you're a member of the team or not), ask for an invite with your Email in [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org), so you get automatic updates when something changes about the event. Anybody that's already invited to the meeting is free and encouraged to invite anybody else.

Meeting notes are taken on https://pad.lassul.us/ and later committed to https://github.com/nixpkgs-architecture/meetings.

A guide for how to host these meetings can be found [here](./hosting.md)
