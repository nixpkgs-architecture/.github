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

### Preparing Jitsi for live streaming

- Go to the [Jitsi meeting](https://meet.jit.si/nixpkgs-architecture)
- Enter your nick or name
- Click "Join meeting", you can mute and turn off the camera
- Click on the "..." button, this opens up a submenu
- Click on the "Start live stream" entry, this opens up a panel
- Click on the "Sign in with Google" button, this opens a pop-up
- Select your Google account from the previous section
- Click on "Allow"
- Ensure that the "Live stream key" field has been automatically filled out. Note that the title of the stream indicated might be wrong, this is not a problem
- Click on Cancel and leave the meeting, this will work automatically for future meetings

## Hosting the meeting

These steps are necessary every time a meeting is hosted, preparation takes about 15 minutes.

### Preparing the live stream

- Go to [YouTube Studio](https://studio.youtube.com/)
- Click on the Go Live button, it looks like this:

  ![The Go Live button](./go-live-button.png)

- Edit the live-stream by click on the "Edit" button, a panel should open
  - Set the "Title" field to "Nixpkgs Architecture Team Meeting #NUMBER on YYYY-MM-DD", filling in the correct meeting number and date
  - Set the "Description" field to the following, filling in the correct meeting number and date

    > This is the NUMBERth meeting of the Nixpkgs Architecture Team, held on YYYY-MM-DD in https://meet.jit.si/nixpkgs-architecture. For more info on the team, see https://github.com/nixpkgs-architecture. Meeting notes are taken live in https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ and later uploaded to https://github.com/nixpkgs-architecture/meetings
  - Set the "Visibility" to "Public", note that you need to click on "Done" to apply the setting. This allows sharing a link to the live-stream before it is started
  - Under the "Playlists" section, select the "Nixpkgs Architecture Team Meetings" playlist
  - Click "Save", the panel should close. Briefly check the "Title" and "Privacy" fields to make sure the changes were applied

### Coping the URL to the stream before it started
- Go to the [Nixpkgs Architecture Team Meetings playlist](https://www.youtube.com/playlist?list=PLHG2N-mfvWT7XA0Sn4RLGSVSpUYPlTXHI)
- Click on the bottom-most entry of that list, it should be the just-created live-stream. This takes you to the stream viewing page
- Click on the "Share" button, a panel should open, displaying the URL to the stream
- Click on "Copy" to quickly copy the URL into the clipboard

### Announcing the meeting on Matrix

- Write a message on the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with the following content, filling in the URL to the stream from the previous section:

  > @room: The next meeting will take place soon in https://meet.jit.si/nixpkgs-architecture or live streamed at STREAM-URL, meeting notes are taken https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ

- If possible with your Matrix client, create and copy a shareable URL to the written message

### Preparing the meeting notes

- Go to the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Ensure that the meeting number is correct
- Fill out the "Matrix announcement" field with the URL to the Matrix message from the previous section
- Fill out the "Recording link" field with the URL to the live-stream
- Fill out the "Who records" and "Who leads the meeting" fields with your nick or name
- Fill out the "Who takes meeting notes" field with the person taking the meeting notes
- Add entries to the "Administrative" section if there are any administrative things to discuss
- Add all agenda entries to the "Agenda" section

### The meeting

- Join the [Jitsi meeting](https://meet.jit.si/nixpkgs-architecture)
- Wait a couple minutes
- Start the live-stream
  - Click on the "..." button
  - Click on the "Start live stream" entry
  - Click the "Start live stream" button
  - Wait until you get confirmation that the stream was started, this takes about 10 seconds
- Welcome everybody
- Mention who records, who takes meeting notes and who leads the meeting
- Have the meeting
  - Go through all Administrative points
  - Go through all Agenda points
  - Keep the time in mind
  - Keep the discussion on-topic
- When the meeting time is up or if all agenda items have been discussed:
- Thank everybody for participation, say goodbye, but mention that people are free to continue the discussion here
- Stop the live-stream
  - Click on the "..." button
  - Click on the "Stop live stream" entry

### Afterwards

- If necessary, clean up the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Upload the meeting notes to the [meetings repository](https://github.com/nixpkgs-architecture/meetings) in any way you like
  - Either copy the meeting notes into the clipboard directly or download them as a Markdown file
  - Commit the meeting notes to the repository, either via a local checkout or the GitHub UI for creating a new file
  - Make sure that the file name is of the form YYYY-MM-DD.md
  - The commit subject should be "Meeting #NUMBER"
