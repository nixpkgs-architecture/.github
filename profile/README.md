# Nixpkgs Architecture Team

The Nixpkgs Architecture Team is there to solve architectural nixpkgs issues that are too big in scope for any single person to undertake.

## Motivation

Nixpkgs is arguably the most valuable resource for Nix users. Its collection of packages is used by virtually every Nix user, private or commercially. However, there's continuous complaints by virtually every user of nixpkgs about various aspects, like missing documentation, difficulty of contributing, inconsistent interfaces and missing features. These problems need to be fixed eventually, doing nothing is not an option if Nix should be taken seriously as a universal solution for packaging.

The scale of nixpkgs has grown so considerably in recent years that it's not possible anymore for any single person to fix larger problems. And even if someone does manage to find _a_ solution to a problem, there's nobody who can officially _accept_ that solution and actually merge it. Over the years a number of improvements have been suggested and implemented, but most of them never made it to the finish line.

By creating a team tasked with the job of finding solutions to these issues it becomes much more feasible to actually do it.

## Goals

The primary goal of this team is to make interactions with nixpkgs a joy, so that it's easy and intuitive to use, learn and contribute to. The way in which this should be achieved is to fix problems in a clean, consistent and future-proof way. It should be ensured that nixpkgs is a solid and trustworthy foundation for the Nix community that can be relied upon.

The process in which this should be achieved is to gather and analyze critical feedback from users to find the root causes of problems, coming up with and evaluating solutions to these problems, reaching consensus and deciding on a solution and then actually turning it into reality. This is explained more detailed in the [process](#process) section.

Since nixpkgs is widely used by third-party code, this team needs to be very careful to ensure reasonabe backwards-compatibility. Backwards incompatible changes are only in scope after a deprecation window of an appropriate duration and accompanying warning.

### Concrete Examples

To give a taste, here are some examples for concrete issues this team might be attempting to solve:

- Inconsistent and confusing overriding story: There's overlays, `.override`, `.overrideAttrs`, `overrideScope'`, `.extend` and others, each of which has a related use case. Knowing when to use what is unreasonably difficult. And sometimes there's no way to do the desired override at all
- Inconsistent package versioning: If multiple versions of a package are required, the convention is to introduce additional top-level attributes reflecting the alternation in their name, such as `python2`, `ffmpeg-full`, `firefox-esr`, `haskellPackages.aeson_1_5_6_0`. This is problematic because the attributes are not discoverable, follow no shared convention and they make overrides more problematic. Additionally there is [a desire](https://github.com/NixOS/nixpkgs/issues/93327) to be able to refer to specific versions of packages
- Problematic `stdenv.mkDerivation` base builder concepts: Focused on C and Makefiles, attributes are stringified and turned to environment variables, build phases are finnicky to override, package sources and patches are tied to the builder, different build inputs are hard to distinguish.
- Package meta information is too vague: What does `broken` mean, unfree licenses, supported platforms, maybe a category/tagging system would be nice
- File structure of the `pkgs` directory and the `pkgs/top-level/all-packages.nix` file is arbitrary and inconsistent
- No well-specified process for backwards compatibility and deprecation of packages, other attributes, function arguments, etc.
- Authority over nixpkgs is hard to delegate, commit bits give too much power, maybe it could use some splitting up into different repositories
- The documentation of Nix code is bad, hard to find or non-existent

### Non-goals

- Reviewing and merging trivial PRs: Instead of trying to bring down the PR queue, this team should try to find the root cause of such issues and work on fixing those. This could mean improving maintainer independence, splitting nixpkgs up or something else

## Process

This section describes the process of going from an issue to a solution. While described here as one, this shouldn't be a linear process. Instead this should be done in a feedback-oriented way.

To track progress for an issue, [GitHub projects](https://github.com/orgs/nixpkgs-architecture/projects?type=beta) are used.

### Problem statement

Before working towards a solution the team needs to figure out whether there even is a problem, what its suspected root cause is, and to clearly describe it.

### Solution exploration

The team should explore various potential solutions and figure out trade-offs with methods like:
- Developing prototypes
- Creating test cases
- Surveying the community
- Measuring performance

Specifically for nixpkgs, this includes all the past history, with all its approaches, refactorings, complaints and testimonies.

### Reaching consensus

To decide on a solution, consensus has to be reached among _all_ team members. If consensus cannot be reached yet it indicates that there is some fundamental misundestanding or difference in values between team members. This needs to be reconciled by:
- Going back to solution exploration to find new alternatives or gather more information or support for arguments
- Trying to better understand each other by talking and listening
- Being willing to compromise

### Official RFC

In order to comply with the [Nix RFC process](https://github.com/NixOS/rfcs), after the team has reached consensus among themselves, an RFC should be created so the decision can be approved officially. Members of the nixpkgs team are encouraged to nominate themselves as [RFC shepherds](https://github.com/NixOS/rfcs#shepherd-team).

## Administration

### Team

As a team member you are expected to partake in the teams discussions by bringing in your expertise and opinions in order to steer the final decisions into the best direction.

While anybody is welcome to join the public nixpkgs architecture discussions, both to listen in or to bring their opinion, only the team members need to reach consensus to make decisions.

#### Current Team

- Silvan Mosberger ([@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org), [Tweag](https://www.tweag.io/))

A log of the team modifications is available [here](https://github.com/nixpkgs-architecture/team-log)

#### Joining the team

The requirements for being part of the team:
- Having an interest in the large-scale architecture of nixpkgs
- Being reachable through [Matrix](https://matrix.org/), so that at least asynchronous communication is possible
- Being able to discuss with [reason](https://en.wikipedia.org/wiki/Reason), because only then it is possible to find consensus for decisions among a larger team

Additional strong recommendations:
- Be willing and available to have occasional synchronous audio/video meetings
- Have a GitHub account, allowing you to become part of the [nixpkgs-architecture](https://github.com/nixpkgs-architecture) organization for working on code together

The process of joining the team is as follows:
- Reach out to the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with your request to join the team. Feel free to tell us a little bit about yourself, such as:
  - Motivation for joining, what you're interested in discussing or working on
  - If you'd like to join the GitHub team, mention your GitHub user
  - If applicable and wanted, the company that sponsors time to work on this
  - Tell us what times you'd be available for audio/video meetings
- A discussion will take place as to whether you're accepted as a new team member
- The current team members will reach consensus on whether to accept the request and record that decision in the public [team log](https://github.com/nixpkgs-architecture/team-log) document, including all relevant arguments
- If accepted, [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org) will take these steps for adding you to the team:
  - Updating the above [team list](#current-team) list with your entry and all relevant details
  - If you want to join the GitHub team, adding your GitHub user to the [nixpkgs architecture](https://github.com/nixpkgs-architecture) organization
  - If you haven't joined the weekly public meetings already, invite you

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
- Remove the respective team member from the above [team list](#current-team)
- If applicable, removing the respective team member from the [nixpkgs architecture](https://github.com/nixpkgs-architecture) organization

### Code

Code developed for the nixpkgs team is generally committed under the [nixpkgs-architecture GitHub organization](https://github.com/nixpkgs-architecture).

### Communication

Team communication happens in mainly two forms:
- Continuously over text in the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel
- Weekly from 15:00 to 16:00 UTC over audio/video in a meeting on https://meet.jit.si/nixpkgs-architecture

Other forms of communication can be used as needed.

### Meetings

The agenda of the weekly meetings is as follows:

- Protocol (5m)
  - Who records and start recording
  - Who takes meeting notes
  - Who leads the meeting
- Introduction and Administration (5m)
  - Optional onboarding of new members
  - Organizational changes
- Discussions (50m)
  - Status updates since last week
  - Next steps


Meetings recorded and uploaded or live-streamed to YouTube

Meeting notes in https://pad.lassul.us/, later committed to https://github.com/nixpkgs-architecture/meetings

