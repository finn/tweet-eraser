# shame-eraser

A small Ruby script for erasing your shame on Twitter (i.e. your oldest tweets).

## Author

[Benjamin Jackson](http://twitter.com/benjaminjackson)

## Instructions:

### Set Up A Twitter App

First, you'll have to set up a Twitter app on the developer portal and generate an OAuth key.

1. Visit the [Twitter Developer Apps](https://dev.twitter.com/apps) page and [create a new app](https://dev.twitter.com/apps/new), filling out only the required fields.
2. Go to the "Settings" tab for your app, scroll down, and change "Application Type" to "Read and Write", then click "Update this Twitter application's settings".
3. Go to the "Details" tab, scroll down, and click "Create my access token" (or "Recreate my access token" if you already created one). When you refresh, you should see "Access Level: Read and Write" after your access token and secret.

Make sure to note down your **consumer key**, **consumer secret**, **access token**, and **access token secret**. You'll need them to run the script.

### Install Ruby Bundler

Thsi will require running some things on the command line. Open the Terminal (just type `Terminal` into Spotlight), copy and paste this into the tab that opens up, and hit `Enter`:

    sudo gem install bundler

Enter your password if and when it asks for it and press `Enter`.

### Install Git

Install Git using [these instructions on GitHub](https://help.github.com/articles/set-up-git).

### Download your tweets

Download your tweet archive from your Twitter settings page. Unzip the downloaded archive.

### Install shame-eraser

Open the Terminal again, copy and paste the following line into it, and hit Enter:

    git clone https://github.com/benjaminjackson/shame-eraser.git && cd shame-eraser && bundle install && open lib


### Run shame-eraser

    bundle exec ruby bin/eraser.rb

Drag your tweets folder onto the Terminal and it should auto-complete the path to the folder. *Now* hit Enter.

When the script runs it will ask for your consumer key, consumer secret, access token, and access token secret which you noted down earlier.

The script will prompt you for a start and end date, and confirm that you **really** want to do this.
