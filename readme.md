# Requirements

You must have Node.js installed. If you don't have it installed yet, don't worry, it's easy. Go to http://nodejs.org/ and click Install!

Currently we only support local development for Mac OS X. If you need to develop in windows, contact your support representative and we'll work with you to get setup.


# Getting Started

This repository is bootstrapped with a bunch of useful functions for managing your website. First you'll need to make sure your system is up and running.

* Open `config.js` and setup the configuration settings. These are available in your Momentum HQ under **Theming > Setup**.
* Open your terminal and `cd` to your repository directory.
* Run `make install`
* Run `./rain reset` (this loads any deployed theme content into your repository, local changes will be overwritten)
* After installation is completed, and anytime you want to work on your theme in the future, run `make run` and your changes will automatically deploy live as you work.

# Updating

1. Accept any pull requests from Momentum's GIT repository and merge them into your repo.
2. Run `make install && make update` to install any new modules and update old ones.

# The Playground

> (coming soon)

Packaged in this repo in the `./themes/playground` directory are dozens of useful coding examples that you can edit and view live. Once you're done playing
with a specific example you can always copy it to an appropriate file.

* Reset all playground examples. `make playground`

# Testing Live
Every time you make a change to a file, it synchronizes live to a testing queue on your Momentum server. In order to view your changes without publishing, you have to connect your session to the API key you're using.

Just run `./rain preview` and your default browser will automatically open a page that configures your session for preview. If it doesn't just copy the URL generated into your browser. You should see a message in your browser indicating that your session is currently associated with the API key you've configured in `config.js` file.

> Make sure that every developer working on the website is using their own API credentials or you may see changes from another developer.

# Publishing
Once you're satisfied that a page is ready for the public, you just have to run `./rain deploy FILENAME`. e.g. `./rain deploy pages/index.lhtml`

If you've created or modified any modules, make sure you also deploy those.

If you want to deploy all the pending changes you've made live just type `./rain deploy` and all the queued changes will be deployed.

# Managing Revisions / Conflicts
We recommend setting up a GIT repository if you have multiple developers working on the same website, or if you just want to be able to easily rollback to previous versions of the website.

Momentum does not merge files if there are code conflicts, nor do we track file history. Make sure to properly commit your changes and merge in other developer's work before deploying live.

