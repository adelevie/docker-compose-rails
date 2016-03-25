# docker-compose-rails

A starter app for using [Rails](http://rubyonrails.org/) with [docker-compose](https://docs.docker.com/compose/). The app is not very opinionated. It's shipped to use Postgres, but this can be easily changed.

## Installation

The only dependency is docker-compose.

Clone this repo, and `cd` into it.

Build the images:

```
$ docker-compose build
```

Rename the app:

```
$ docker-compose run web bundle exec rails g rename:app_to your_new_app_name
```

To run the local server (should be at localhost:3000):

```
$ docker-compose up
```

To run any Rails or Ruby command, prepend it with `docker-compose run web`. For example, to create a migration:

```
$ docker-compose run web bundle exec rails g migration CreatePosts title:string body:text
```

And to run the migrations:

```
$ docker-compose run web bundle exec rake db:migrate
```

To run the Rails console:

```
$ docker-compose run web bundle exec rails c
```

## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
