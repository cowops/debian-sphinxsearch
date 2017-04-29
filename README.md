Debian-Sphinx
=============

Sphinx is an open source full text search server, designed from the ground up with performance, relevance (aka search quality), and integration simplicity in mind.

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

sphinxsearch:
    start: "yes"
    sql:
        host: "localhost"
        user: "test"
        pass: ""
        db: "test"
        port: "3306"

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cowops.debian-sphinxsearch, sphinxsearch.start: "yes", sphinxsearch.sql.host: "localhost", sphinxsearch.sql.user: "test", sphinxsearch.sql.pass: "", sphinxsearch.sql.db: "test", sphinxsearch.sql.port: "3306" }

Tasks
-----

  - Install [Sphinx](http://sphinxsearch.com/)
  - Enable auto-start

License
-------

BSD
