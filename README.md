# shame-eraser

A small Ruby script for erasing your shame on Twitter (i.e. your oldest tweets).

## Author

[Benjamin Jackson](http://twitter.com/benjaminjackson)

## Instructions

### Set up a Twitter app

First, you'll have to set up a Twitter app on the developer portal and generate an OAuth key.

1. Visit the [Twitter Developer Apps](https://dev.twitter.com/apps) page and [create a new app](https://dev.twitter.com/apps/new), filling out only the required fields.
2. Select the **Settings** tab for your app, scroll down, and change **Application Type** to `Read and Write`. Click **Update this Twitter application's settings**.
3. Select the **Details** tab. Scroll down and click **Create my access token** (or **Recreate my access token** if you already created one). When you refresh, you should see "Access Level: Read and Write" after your access token and secret.

Make sure to note down your **Consumer key**, **Consumer secret**, **Access token**, and **Access token secret**. You'll need them to run the script.

### Install git

Install Git using [these instructions on GitHub](https://help.github.com/articles/set-up-git).

### Download your tweets

Download your tweet archive from your Twitter settings page. Unzip the downloaded archive.

### Install ruby bundler

This will require running some things on the command line. Open the Terminal (just type `Terminal` into Spotlight). Copy and paste this line into the window that opens and press `Enter`:

    sudo gem install bundler

Enter your password if and when it asks for it and press `Enter`.

### Install shame-eraser

Copy and paste the following line into the Terminal window and press `Enter`:

    git clone https://github.com/benjaminjackson/shame-eraser.git && cd shame-eraser && bundle install && open lib

### Run shame-eraser

Still in the Terminal, copy and paste the following line into the window:

    bundle exec ruby bin/eraser.rb

Drag your tweets folder onto the Terminal window. It should auto-complete the path to the folder. *Now* press `Enter`.

When the script runs it will ask for your consumer key, consumer secret, access token, and access token secret which you noted down earlier.

The script will prompt you for a start and end date, and confirm that you **really** want to do this.
