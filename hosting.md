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

## One day before the meeting

These steps should be taken a day ahead of every meeting.

### Preparing the agenda

- Go on [Discourse](https://discourse.nixos.org/) and create a new topic
  - Title should be (fill in the variables)

    > YYYY-MM-DD Nixpkgs Architecture Team Meeting #NUMBER

  - Category should be [Development > Nixpkgs Architecture](https://discourse.nixos.org/c/dev/nixpkgs/44)
  - The start of the text should be something like this (fill in MEETING DAY AND TIME):

    ```
    The [Nixpkgs Architecture Team](https://nixos.org/community/teams/nixpkgs-architecture.html) will have the next meeting tomorrow at MEETING DAY AND TIME. The meeting is open for anybody to join.
    
    - [Meeting link](https://meet.jit.si/nixpkgs-architecture)
    - [Livestream](https://www.youtube.com/channel/UC_BFweJOiukTHdKCr1P0kRQ)
    - [Live meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ)
    
    ## Tentative Agenda
    ```

- Go to the [Matrix room](https://matrix.to/#/#nixpkgs-architecture:nixos.org) and find the message announcing the previous meeting
  - One way to do this is by searching for `@room`
  - Another way is to go to the [meeting notes](https://github.com/nixpkgs-architecture/meetings) and clicking the "Matrix announcement" link on the latest meeting
- Go through the Matrix channel logs to collect discussed topics. For each topic:
  - If it's off-topic or otherwise doesn't seem worth further discussing, skip it. If you're unsure, it's fine to include it.
  - Add an entry with a `###` header to the Discourse draft containing the briefly summarized discussion
    - Include a link to the Matrix message that initiated the discussion
    - Include the usernames of all people that participated.
- Publish the Discourse post

### Preparing the live stream

- Go to [YouTube Studio > Go Live > Manage](https://studio.youtube.com/channel/UC_BFweJOiukTHdKCr1P0kRQ/livestreaming/manage)
- Click on "SCHEDULE STREAM"
- Click on "REUSE DETAILS"
- Update the meeting number and the date in the title
- Select the "Nixpkgs Architecture Team Meetings" playlist
- Click "NEXT" to get to the Customization tab
- Click "NEXT" to get to the Visibility tab
- If the meeting doesn't happen in your timezone, run the following command, replacing `<date>`, `<time>` and `<timezone>` with the details from the meeting, to figure out the time in your local timezone

  ```
  date --date='<date> <time> <timezone>' +'%Y-%m-%d %r'
  ```

- Under "Schedule", enter the date and time returned from the above command
- Click "DONE"

### Preparing the meeting notes

- Go to the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Fill out the "Agenda" entry with the link to the Discourse agenda
- Fill out the "Recording" field with the URL to the live-stream. To copy the URL:
  - Go to the [Nixpkgs Architecture Team YouTube channel](https://www.youtube.com/channel/UC_BFweJOiukTHdKCr1P0kRQ)
  - Click on the upcoming livestream
  - Click on the "Share" button, a panel should open, displaying the URL to the stream
  - Click on "Copy" to quickly copy the URL into the clipboard
- Fill out the "Who records" field with your nickname
- Copy the headers of the Discourse agenda entries into the meeting notes

## Shortly before the meeting

- Write a message on the [#nixpkgs-architecture:nixos.org](https://matrix.to/#/#nixpkgs-architecture:nixos.org) Matrix channel with the following content:

  ```
  @room: The next meeting will take place soon - [Meeting link](https://meet.jit.si/nixpkgs-architecture) - [live stream](https://www.youtube.com/channel/UC_BFweJOiukTHdKCr1P0kRQ) - [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ) - [agenda](https://discourse.nixos.org/c/dev/nixpkgs/44)
  ```

- If possible with your Matrix client, create and copy a shareable URL to the message
- Go to the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
  - Fill out the "Matrix announcement" field with the URL to the message
  - Fill out the "Who leads the meeting" field
  - Fill out the "Who takes meeting notes" field

## The meeting

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
  - Go through all Agenda entries
  - Keep the time in mind
  - Keep the discussion on-topic
- When the meeting time is up or if all agenda items have been discussed:
- Thank everybody for participation, say goodbye, but mention that people are free to continue the discussion here
- Stop the live-stream
  - Click on the "..." button
  - Click on the "Stop live stream" entry

## Afterwards

- If necessary, clean up the [meeting notes](https://pad.lassul.us/uIi7xeSJTW6LJUEHulZgVQ?edit)
- Upload the meeting notes to the [meetings repository](https://github.com/nixpkgs-architecture/meetings) in any way you like
  - Either copy the meeting notes into the clipboard directly or download them as a Markdown file
  - Commit the meeting notes to the repository, either via a local checkout or the GitHub UI for creating a new file
  - File name should be "YYYY-MM-DD.md", commit subject should be "Meeting #NUMBER"
- In the Discourse agenda, create a reply containing the meeting notes
