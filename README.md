# WaniKani to Anki Exporter

#### Get your WaniKani decks in Anki!

WaniKani to Anki Exporter is a small website that allows you to easily fetch data from your
[WaniKani](https://www.wanikani.com/) account and generate a file that can be imported
into an [Anki](http://ankisrs.net/) deck.

If you have a WaniKani account, you can see the site up and running at http://wanikanitoanki.com.
You will need a WaniKani API key to see all the functionality built in.

## Prerequisites

1. Ruby 2.2.0 https://www.ruby-lang.org/en/

Install as per your operating system instructions.

2. Bundler http://bundler.io/

```
gem install bundler
```

## How to run the website

The WaniKani to Anki Exporter site is a [Padrino](http://www.padrinorb.com/) app.

Getting the site up and running is very simple.
In the project's directory, run the following:

```
$ bundle install
$ rackup
```

That should be all! If you go to http://localhost:9292 after that, the site should be working.
Currently there's no database required, but that might change in the future as I expand the
site's functionality.

## Docker

If you have [Docker](https://www.docker.com/) installed in your local environment, use the
included Dockerfile to build a Docker image that will run the WaniKani to Anki Exporter site
on your system for development purposes.

After building the image (assuming the naming convention `<image_name>:<image_tag>`), you can
run the WaniKani to Anki Exporter site:

```
docker run \
  -p 9292:9292 \
  -v $PWD:/app \
  <image_name>:<image_tag>
```

Alternatively, if you have [Docker Compose](https://docs.docker.com/compose/) installed, you
can simply run `docker-compose up` to build and run

## Why did I build this?

I'm both an avid WaniKani user as a Japanese student, as well as an avid Anki user. I wanted to
be able to have a little bit more control about what things from WaniKani I wanted to study, as
well as control other variables like the time intervals, etc. I noticed that other WaniKani users
were looking for something similar, so I decided to share it as a website.

## Submit a pull request!

1. Fork the repo into your own Github account (https://github.com/dennmart/wanikani-to-anki/fork)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`) and make sure your write tests for your new feature!
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
6. That's it! High fives given upon request :smile_cat:

## To run a single test

Use rspec <path/to/spec.rbb>
