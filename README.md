# Indigenous for Desktop

An IndieWeb app with extensions for sharing information to micropub endpoints and reading 
from microsub endpoints. Written in Electron, so available for Windows, MacOS and Linux.

The philosophy at the moment of the app is that it will not be a full blown client like
the Android version. The main focus is on the most common features used on a daily basis.

Android: https://github.com/swentel/indigenous-android  
iOS: https://github.com/swentel/indigenous-ios

## Screenshot

<img src="https://realize.be/sites/default/files/indigenous-desktop-timeline.png" width="800" />

## Functionality

- General
  - Uses the font of your system
  - Account: configure endpoints and token
  - Screen state: remember position, fullscreen etc
  - Developer: view response of microsub requests in console
- Microsub
  - You can use https://indigenous.realize.be to test the reader
  - Allow for global unread start screen if the server supports it
  - Different displays: Cards, titles and feed with overlay view
  - Autoload more posts
  - Read channels and posts per timeline
  - Inline responses with or without confirmation
  - Listen to audio or watch video
  - Mark all read button, per item and optionally when viewing detail
  - View individual feed via author name
  - Search in all channels and feeds
  - Delete or move posts, with default channel for moving
  - Navigate posts with keyboard shortcuts:
    - p: previous post in feed or overlay
    - n: next post in feed or overlay, trigger 'More posts' at end
    - r or z: read the post in the overlay
    - c or esc: close overlay when opened
  - Context menu: right click when selecting text to search DuckDuckGo, or save
    an image, or copy the link and so on.
  - External links in posts open in your system browser
- Micropub
  - Post types: note/article
  - Single photo upload
  - Syndication targets
  - Publish date and status
  - Tags, with autocomplete
  - Upload a file to media endpoint (soon in posts)

Video of first release: https://www.youtube.com/watch?v=7egdRBg70XA

## Roadmap

There are a few outstanding feaures coming somewhere in the near future:

- Use media endpoint to upload image, and allow multiple
- Show all sources (if the microsub supports method=tree)
- Figure out automatic builds and updates

Note that currently multiple accounts or using the IndieAuth flow is
not on the roadmap. Pull requests welcome of course :)

## Installation

See the releases page: https://github.com/swentel/indigenous-desktop/releases

## Token generation in Wordpress

When you generate a token on Wordpress and using Aperture as your Microsub
server, make sure the 'me' value of the token is set to the same as used
in Aperture. Usually, this is just the URL of your website. To make sure
that the 'me' value is set to that, fill in the Website on your profile
and set the 'Set User to Represent Site URL' value to your user on the
IndieAuth settings page.

## Launcher on Linux

You create a launcher by creating a file called 'Indigenous.desktop and place
it in /usr/share/applications or ~/.local/share/applications

```
[Desktop Entry]
Name=Indigenous
Comment=IndieWeb for desktop
Exec=/home/other/indigenous-desktop-packages/Indigenous-linux-x64/Indigenous
Terminal=false
Type=Application
Icon=/home/other/indigenous-desktop-packages/Indigenous-linux-x64/resources/app/images/icon.png
```

This should at least work for Fedora and Ubuntu, it might be different on other
linux distributions.

## Development or installation from source

You can also run this application if you are familiar with development tools. Make sure
to have the most stable version running of npm.

To clone and run this repository you'll need [Git](https://git-scm.com) and 
[Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) 
installed on your computer. From your command line:

```bash
# Clone this repository
git clone https://github.com/swentel/indigenous-desktop
# Go into the repository
cd indigenous-desktop
# Install dependencies
npm install
# Run the app
npm start
```

## Credits

This app uses following libraries:

- https://github.com/electron/electron
- https://github.com/sindresorhus/electron-store
- https://jquery.com
- https://iamceege.github.io/tooltipster
- https://github.com/iamkun/dayjs
- https://craig.is/killing/mice
- https://github.com/zeusdeux/isInViewport
- https://github.com/sindresorhus/electron-context-menu
- https://github.com/mawie81/electron-window-state
- https://github.com/dimsemenov/Magnific-Popup
- https://github.com/HubSpot/pace

## Other Micropub and Microsub clients

There are ton of other (mobile) clients, see https://indieweb.org/Micropub/Clients and
https://indieweb.org/Microsub
