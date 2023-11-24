# YouTube streaming setup

The Nixpkgs Architecture Team has a [YouTube](https://www.youtube.com/@nixpkgs-architecture) channel that can be used to stream presentations, and has been used for past meetings.

This document describes how to set it up.

## One-time

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
  - Make sure you're on the Nixpkgs Architecture Team account
  - Click on "Settings" on the bottom left, a panel should open
  - Click on the "Permissions" tab
  - Click on "Invite"
  - Enter the E-Mail address of your Google account
  - Select "Editor" in the "Access" field

## Before every stream

### Preparing the live stream

- Go to [YouTube Studio > Go Live > Manage](https://studio.youtube.com/)
- Click on "SCHEDULE STREAM"
- Click on "REUSE SETTINGS"
- Update the meeting number and the date in the title
- Click "NEXT" to get to the Customization tab
- Click "NEXT" to get to the Visibility tab
- YouTube always uses your local timezone, so if the meeting happens in a different one you need to convert the timezone.
  To do so you can run the following command, replacing `<date>`, `<time>` and `<timezone>` with the details of the stream time:

  ```
  date --date='<date> <time> <timezone>' +'%Y-%m-%d %r'
  ```

- Under "Schedule", enter the date and time returned from the above command
- Click "DONE"

### Starting the stream
- Click on the "..." button
- Click on the "Start live stream" entry
- Copy the "Stream key" from the live-stream tab and paste it into the Jitsi tab
- Click the "Start live stream" button
- Wait until you get confirmation that the stream was started, this takes about 10 seconds

### Stopping the stream
- Click on the "..." button
- Click on the "Stop live stream" entry
