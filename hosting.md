# How to host a Nixpkgs Architecture Team Meeting

This is a detailed guide for how to prepare and host Nixpkgs Architecture Team meetings.

## Before every the meeting

### Announcing the meeting

- Write a message on the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with the following content:

  ```
  @room: The next meeting will take place soon - [meeting link](https://meet.jit.si/nixpkgs-architecture) - [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ)
  ```

### Preparing the meeting notes

- Go to the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Fill out the "Matrix announcement" field with the URL to the Matrix message
- Fill out the "Who leads the meeting" fields with your nickname
- Fill out the "Who takes meeting notes" field with the person appointed with taking meeting notes

## The meeting

- Join the [Jitsi meeting](https://meet.jit.si/nixpkgs-architecture)
- Wait a couple minutes
  - Make sure the person taking meeting notes is present
  - Make sure the "Attending" field of the meeting notes includes at least all the present NAT members
- Have the meeting
  - Keep the time in mind
  - Keep the discussion on-topic
- When the meeting time is up or there's nothing else to discuss, end the meeting and mention that people are free to continue the discussion here

## Afterwards

- If necessary, clean up the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Upload the meeting notes to the [meetings repository](https://github.com/nixpkgs-architecture/meetings) in any way you like
  - Either copy the meeting notes into the clipboard directly or download them as a Markdown file
  - Commit the meeting notes to the repository, either via a local checkout or the GitHub UI for creating a new file
  - File name should be "YYYY-MM-DD.md", commit subject should be "Meeting #NUMBER on YYYY-MM-DD"
- Create a Discourse post with the meeting notes, see [previous posts](https://discourse.nixos.org/search?q=meeting%20%23dev%3Anixpkgs%20order%3Alatest) for the pattern
