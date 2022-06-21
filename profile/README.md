# Nixpkgs Design Team

## Motivation

Nixpkgs is arguably the most valuable resource for Nix users. Its collection of thousands of packages is used by virtually every Nix user, private or commercially.

However, the current state of nixpkgs leaves a lot to be desired:
- Inconsistent and confusing overriding story: There's overlays, `.override`, `.overrideAttrs`, `overrideScope'`, `.extend` and others, each of which has a related use case. Knowing when to use what is unreasonably difficult. And sometimes there's no way to do the desired override at all
- Inconsistent package versioning: If multiple versions of a package are required, the convention is to introduce additional top-level attributes reflecting the alternation in their name, such as `python2`, `ffmpeg-full`, `firefox-esr`, `haskellPackages.aeson_1_5_6_0`. This is problematic because the attributes are not discoverable, follow no shared convention and they make overrides more problematic. Additionally there is [a desire](https://github.com/NixOS/nixpkgs/issues/93327) to be able to refer to specific versions of packages
- Problematic `stdenv.mkDerivation` concepts: Focused on C and Makefiles -focused, attributes are stringified and turned to environment variables, build phases are finnicky to override, package sources and patches are tied to the builder, different build inputs are hard to distinguish.
- Poor documentation
- Meta: broken, licenses, platforms, tags
- Deprecation and backwards compatibility
- File structure
- Splitting nixpkgs into multiple repositories

## Goals

The goal of this team is to improve the large-scale design of nixpkgs, focusing on issues that are too large for any single individual to undertake, or that require consistency among all of nixpkgs.

Such improvements have to be backwards-compatible regarding the conventionally agreed-upon API surface of nixpkgs. Backwards incompatible changes are only allowed after a deprecation window with an appropriate duration and an accompanying warning.

### Non-goals


## Process

Based on [Nix RFCs](https://github.com/NixOS/rfcs)

## Team

The team consists of:
- Silvan Mosberger (@infinisil, contact@infinisil.com, Tweag)

### Joining the team

Anybody with an interest in discussing or working on nixpkgs design is welcome

To join the team, open a PR to change the above team list to include your entry

## Communication

Team page: https://github.com/nixpkgs-design
Chat: Matrix channel #nixpkgs-design:nixos.org
Weekly meetings: https://meet.jit.si/


