# Hanami

A Clojure utility library for [Heroku][] web applications.

[heroku]: https://heroku.com

## Installation

Add the following dependency to your `project.clj`:

    [hanami "0.1.0-SNAPSHOT"]

## Usage

Hanami currently just has one multimethod, `jdbc-uri`, that can be used to
change a Heroku `DATABASE_URL` value into a JDBC connection string.

```clojure
(require '[hanami.core :as hanami])

(hanami/jdbc-uri "postgres://foo:foo@heroku.com:5432/hellodb")
=> "jdbc:postgresql://heroku.com:5432/hellodb?user=foo&password=foo"
```

## License

Copyright © 2014 James Reeves

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
