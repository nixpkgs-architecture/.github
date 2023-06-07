# How to host a Nixpkgs Architecture Team Meeting

This is a detailed guide for how to prepare and host Nixpkgs Architecture Team meetings.

## One-time setup

These steps are only necessary once.

### Getting a Google account

In order to have access to the YouTube channel, you need a Google account.
If you have one already you can use that one, but you're free to create a new one as well.

#### Creating a new Google account

- Go to [YouTube](https://www.youtube.com/)
- Click on the "Sign In" button at the very top right
- Click on "Create account"
- Follow the steps to your liking

#### Copying the E-Mail address of your Google account

- Go to the [Google Account page](https://myaccount.google.com/)
- Click on the round icon at the top right of the page
- Copy the E-Mail it displays to the clipboard

### Get access to the YouTube channel

- Send the E-Mail address of your Google account to [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org)
- [@infinisil:matrix.org](https://matrix.to/#/@infinisil:matrix.org) will do the following steps for you:
  - Go to [YouTube Studio](https://studio.youtube.com/)
  - Click on "Settings" on the bottom left, a panel should open
  - Click on the "Permissions" tab
  - Click on "Invite"
  - Enter the E-Mail address of your Google account
  - Select "Editor" in the "Access" field

## Before every the meeting

### Preparing the live stream

- Go to [YouTube Studio > Go Live > Manage](https://studio.youtube.com/)
- Click on "SCHEDULE STREAM"
- Click on "REUSE SETTINGS"
- Update the meeting number and the date in the title
- Click "NEXT" to get to the Customization tab
- Click "NEXT" to get to the Visibility tab
- If the meeting doesn't happen in your timezone (see the [NixOS Calendar](https://calendar.google.com/calendar/u/0/embed?src=b9o52fobqjak8oq8lfkhg3t0qg@group.calendar.google.com&ctz=Europe/Zurich)), run the following command, replacing `<date>`, `<time>` and `<timezone>` with the details from the meeting, to figure out the time in your local timezone

  ```
  date --date='<date> <time> <timezone>' +'%Y-%m-%d %r'
  ```

- Under "Schedule", enter the date and time returned from the above command
- Click "DONE"

### Announcing the meeting

- Write a message on the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with the following content:

  ```
  @room: The next meeting will take place soon - [meeting link](https://meet.jit.si/nixpkgs-architecture) - [live stream](https://www.youtube.com/@nixpkgs-architecture) - [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ)
  ```

### Preparing the meeting notes

- Go to the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Fill out the "Recording" field with the URL to the live-stream. To get the URL, click on the Arrow button on the top right in the live-stream tab
- Fill out the "Matrix announcement" field with the URL to the Matrix message
- Fill out the "Who records" and "Who leads the meeting" fields with your nickname
- Fill out the "Who takes meeting notes" field with the person appointed with taking meeting notes

## The meeting

- Join the [Jitsi meeting](https://meet.jit.si/nixpkgs-architecture)
- Wait a couple minutes
  - Make sure the person taking meeting notes is present
  - Make sure the "Attending" field of the meeting notes includes at least all the present NAT members
- Start the live-stream
  - Click on the "..." button
  - Click on the "Start live stream" entry
  - Copy the "Stream key" from the live-stream tab and paste it into the Jitsi tab
  - Click the "Start live stream" button
  - Wait until you get confirmation that the stream was started, this takes about 10 seconds
- Have the meeting
  - Keep the time in mind
  - Keep the discussion on-topic
- When the meeting time is up or there's nothing else to discuss, end the meeting and mention that people are free to continue the discussion here
- Stop the live-stream
  - Click on the "..." button
  - Click on the "Stop live stream" entry

## Afterwards

- If necessary, clean up the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Upload the meeting notes to the [meetings repository](https://github.com/nixpkgs-architecture/meetings) in any way you like
  - Either copy the meeting notes into the clipboard directly or download them as a Markdown file
  - Commit the meeting notes to the repository, either via a local checkout or the GitHub UI for creating a new file
  - File name should be "YYYY-MM-DD.md", commit subject should be "Meeting #NUMBER on YYYY-MM-DD"
- Create a Discourse post with the meeting notes, see [previous posts](https://discourse.nixos.org/search?q=meeting%20%23dev%3Anixpkgs%20order%3Alatest) for the pattern
