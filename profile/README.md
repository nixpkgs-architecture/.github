# Nixpkgs Team

TODO: Two objectives:
- Decide on things that no single person can decide themselves
- Develop things that no single person can develop themselves

TODO: Don't just focus on technical issues

## Motivation

Nixpkgs is arguably the most valuable resource for Nix users. Its collection of thousands of packages is used by virtually every Nix user, private or commercially.

However, the current state of nixpkgs leaves a lot to be desired:
- Inconsistent and confusing overriding story: There's overlays, `.override`, `.overrideAttrs`, `overrideScope'`, `.extend` and others, each of which has a related use case. Knowing when to use what is unreasonably difficult. And sometimes there's no way to do the desired override at all
- Inconsistent package versioning: If multiple versions of a package are required, the convention is to introduce additional top-level attributes reflecting the alternation in their name, such as `python2`, `ffmpeg-full`, `firefox-esr`, `haskellPackages.aeson_1_5_6_0`. This is problematic because the attributes are not discoverable, follow no shared convention and they make overrides more problematic. Additionally there is [a desire](https://github.com/NixOS/nixpkgs/issues/93327) to be able to refer to specific versions of packages
- Problematic `stdenv.mkDerivation` base builder concepts: Focused on C and Makefiles, attributes are stringified and turned to environment variables, build phases are finnicky to override, package sources and patches are tied to the builder, different build inputs are hard to distinguish.
- Package meta information is too vague: What does `broken` mean, unfree licenses, supported platforms, maybe a category/tagging system would be nice
- File structure of the `pkgs` directory and the `pkgs/top-level/all-packages.nix` file is arbitrary and inconsistent
- No well-specified process for backwards compatibility and deprecation of packages, other attributes, function arguments, etc.
- Authority over nixpkgs is hard to delegate, commit bits give too much power, maybe it could use some splitting up into different repositories
- The documentation of Nix code is bad, hard to find or non-existent

## Goals

The goal of this team is to improve the large-scale design of nixpkgs, focusing on issues that are too large for any single individual to undertake, or that require consistency among all of nixpkgs.

Such improvements have to be backwards-compatible regarding the conventionally agreed-upon API surface of nixpkgs. Backwards incompatible changes are only allowed after a deprecation window with an appropriate duration and an accompanying warning.

### Non-goals

- Making design improvements to NixOS
- Review and merge the huge number of nixpkgs PRs

## Process

This section describes the process of going from an issue to a solution. While described here as one, this shouldn't be a linear process. Instead this should be done in a feedback-oriented way.

To track progress for an issue, [GitHub projects](https://github.com/orgs/nixpkgs-team/projects?type=beta) are used.

### Problem statement

Before working towards a solution the team needs to figure out whether there even is a problem and to clearly describe it.

### Solution exploration

The team should explore various potential solutions and figure out trade-offs with methods like:
- Prototyping
- Surveying
- A/B testing
- Measuring performance

Specifically for nixpkgs, this includes all the past history, with all its approaches, refactorings, complaints and testimonies.

### Reaching consensus

To decide on a solution, consensus has to be reached among _all_ team members. If consensus cannot be reached yet it means that there is some fundamental misundestanding or difference in values between team members. This needs to be reconciled by:
- Going back to solution exploration to find new alternatives or gather more information or support for arguments
- Trying to better understand each other by talking and listening
- Being willing to compromise

### Official RFC

In order to comply with the [Nix RFC process](https://github.com/NixOS/rfcs), after the team has reached consensus among themselves, an RFC should be created so the decision can be approved officially. Members of the nixpkgs team are encouraged to nominate themselves as [RFC shepherds](https://github.com/NixOS/rfcs#shepherd-team).

## Administration

### Team

The nixpkgs team is there to develop and discuss the large-scale design of nixpkgs. As a team member you are expected to partake in the teams discussions by bringing in your expertise and opinions in order to steer the final decisions into the best direction.

While anybody is welcome to join the public nixpkgs design discussions, both to listen in or to bring their opinion, only the team members need to reach consensus to make decisions.

#### Current Team

- Silvan Mosberger ([@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org), [Tweag](https://www.tweag.io/))

#### Joining the team

The requirements for being part of the team:
- Having an interest in the large-scale design of nixpkgs
- Being able to discuss with reason, because only with reason it is possible to find consensus for decisions among a large team
- Being reachable through [Matrix](https://matrix.org/), so that at least asynchronous communication is possible

Additional recommendations:
- Be willing and available to have occasional synchronous audio/video meetings
- Have a GitHub account, allowing you to become part of the [nixpkgs-team](https://github.com/nixpkgs-team) organization for working on code together

To join the team, reach out to the [#nixpkgs-team:nixos.org](https://matrix.to/#/#nixpkgs-team:nixos.org) Matrix channel.

#### Leaving the team

If the requirements for being part of the team are not met anymore, the member should leave the team.

### Code

Code developed for the nixpkgs team is generally committed under the [nixpkgs-team GitHub organization](https://github.com/nixpkgs-team).

### Communication

Team communication happens in mainly two forms:
- Continuously over text in the [#nixpkgs-team:nixos.org](https://matrix.to/#/#nixpkgs-team:nixos.org) Matrix channel
- Weekly from 15:00 to 16:00 UTC over audio/video in a meeting on https://meet.jit.si/nixpkgs-team

Other forms can be used as needed.

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

Meeting notes in https://pad.lassul.us/, later committed to https://github.com/nixpkgs-team/meetings

