# FediFollow-Chrome
A Chrome extension that simplifies following Fediverse/Mastodon users on other instances than your own by automatically redirecting you to your instance when pressing a follow button. Should work for other Chromium browsers too, as well as Kiwi browser on Android. It was tested with about 20 instances and supports different instance layouts/flavours.

I made this since I could only find a working extension for Firefox, that does the same (Simplified Federation).

> **Note**
> This worked with all instances tested, but I know there are some instances that use custom layouts/flavours or chose to hide the follow button when not logged in. So please be aware, that this extension can fail in some cases.

## Installation
Right now, you need to install it using developer mode. The extension is already submitted for review by Google, so it shouldn't be long until you can install it from the Chrome Webstore.
1. Download this repository as ZIP or the current release ZIP file and extract it somewhere.
2. Go to your Chrome extension page and enable developer mode.
3. Click the "Load unpacked" button and then select the folder of the unpacked extension (should be "FediFollow-Chrome-main").
    + If you have a "Load ZIP" option you can also directly load the downloaded zip file

## Setup
- Required: Click the extension icon to set your Mastodon instance
  - Only set the domain name (like "infosec.exchange") without http/https or URL)
- Optional: Set the mode (all sites except those on blacklist (default) / no sites but those on whitelist)
- Optional: Add domain names to the blacklist/whitelist textarea, one per line, for ex.
  ```
  mastodon.social
  bbq.snoot.com
  ```
- Required: Hit "Submit" to update your settings

When visiting a user profile on other Mastodon instances, the follow button will now redirect you to your home instance. The redirection is shortly indicated in the follow button itself. Info modals are blocked because they are not needed due to redirection.

The whitelist mode is especially useful if you do not want the extension to run on every site (since it needs to determine if it is a Mastodon site). Not sure the blacklist feature is good for anything but I still included it.

## Screenshots
![Extension Popup](https://github.com/lartsch/FediFollow-Chrome/blob/main/img/screenshot1.PNG?raw=true)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Redirect Indication](https://github.com/lartsch/FediFollow-Chrome/blob/main/img/screenshot2.PNG?raw=true)

## Todos
- Publish to Chrome Webstore (in progress, currently in review by Google)
- Add feature to indicate if you are already following a user when browsing his profile on another instance (this requires calls to the home instance, will look into it soon)
- Review if permissions in current manifest are actually needed like that
- If I find myself to be bored, probably more
