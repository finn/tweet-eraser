# shame-eraser

Now that Twitter has made it easy to download our entire tweet archives, the
Internet is faced with the scary reality that the dumbest things we've ever
said are only a few clicks away. Our early tweets were sent from a time of
innocence, joy, and freedom from the realization that one day other people (and
we ourselves) might pass judgement on them.

But the time of reckoning has come. And if you're unable to bear the weight of
your shame, this is your way out. Perhaps you had a particularly dark period
after a break-up. Maybe your first six months on Twitter were just bad haikus.
If you're the type of person who rips up your old shitty poems, this script is
for you.

**Important:** this should be obvious, but to be sure **there is no undo** for
this script. If you haven't seen *Eternal Sunshine of the Spotless Mind*, you
might want to watch it first. Weigh your options carefully before erasing your
past. (You will, of course, still have your local archive after deleting the
public tweets.)

## Author

* [Benjamin Jackson](http://twitter.com/benjaminjackson)
* [Finn Smith](http://twitter.com/finn)

## Instructions:

### Set Up A Twitter App

First, you'll have to set up a Twitter app on the developer portal and generate
an OAuth key.

* Visit the [Twitter Developer Apps](https://dev.twitter.com/apps) page and
  [create a new app](https://dev.twitter.com/apps/new). Fill out only the
  required fields.

* Go to the "Settings" tab for your app, scroll down, and change "Application
  Type" to "Read and Write", then click "Update this Twitter application's
  settings".

* Go to the "Details" tab, scroll down, and click "Create my access token" (or
  "Recreate my access token" if you already created one). When you refresh,
  you should see "Access Level: Read and Write" after your access token and
  secret.

### Set up the script

* Clone this repo.

* cd into the repo dir.

* Install the bundled gems locally:

    bundle install --path vendor

* Configure the script with your Twitter app authentication information. Edit
  `lib/config.rb` and add your consumer key, consumer secret, access token, and
  access token secret from dev.twitter.com

### Delete Your Old Tweets

* Download your tweet archive from Twitter and unzip it. Note the patht the the
  newly unzipped directory.

* Using bundler, run the `erase_tweets` script from this repo, pointing it to
  the path of your unzipped tweet archive directory:

    bundle exec bin/erase_tweets /path/to/tweet/archive/dir
