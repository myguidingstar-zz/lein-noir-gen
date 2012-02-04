# lein-noir-gen
This is a CRUD-actions generator for a Noir-project. It is heavily inspired by the Rails generators.
Noir-gen creates default view and model for the specified entity. It uses the Mongodb to store the models.

The generated pages have some basic layout made with Bootstrap. The examples of generated pages are here:
https://docs.google.com/open?id=0BzmL7xzGeOtOYjFkZjg4ZjQtYjMwNy00N2M4LTg2MzQtOGFhYzFhYmJkMWEy
https://docs.google.com/open?id=0BzmL7xzGeOtOMmY4MDNlMjItODU5ZS00Y2Q1LWEzM2EtZGM1ZDRiNDUxMDk0

While generating, it rewrites the file 'server.clj' -- do not edit it manually. Also you need to add the congo-mongo dependency to your 'project.clj' like this: [congomongo "0.1.7"]. Each time you generate an entity, lein-noir-gen will tell you to add the dependency.

The options which you may set in your 'project.clj':
:noir-gen {:namespace alternate_namespace
           :database alternate_database}

If these options weren't set, lein-noir-gen will use the default namespace; the name of the database is also a default namespace.

## Usage
Install:
lein plugin install lein-noir-gen 0.2.1

Warning: you must have no previous versions of lein-noir-gen installed. You may delete it manually from $HOME/.lein/plugins/

Run it from the root of your web-application.

lein noir-gen <my-entity> <field1> <field2> ... <fieldN>

$ lein noir-gen article title body author date published

## License

Copyright (C) 2012 Dmitry Bushenko

Distributed under the Eclipse Public License, the same as Clojure.