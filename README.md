# DBML - Database Markup Language [![Build Status](https://travis-ci.org/khoahuynhf/dbml.svg?branch=master)](https://travis-ci.org/khoahuynhf/dbml) [![Coverage Status](https://coveralls.io/repos/github/khoahuynhf/dbml/badge.svg?branch=master)](https://coveralls.io/github/khoahuynhf/dbml?branch=master)

[![Build Status](https://travis-ci.org/holistics/dbml.svg?branch=master)](https://travis-ci.org/holistics/dbml)


DBML (database markup language) is a simple, readable DSL language designed to define database structures.

For more information, please check out [DBML homepage](https://dbml.org)

## Benefits

- It is simple, flexible and highly human-readable
- It is database agnostic, focusing on the essential database structure definition without worrying about the detailed syntaxes of each database
- Comes with a free, simple database visualiser at [dbdiagram.io](http://dbdiagram.io)

## Example

Example of a database definition of a simple blogging site:

    Table users {
        id integer
        username varchar
        role varchar
        created_at timestamp
    }

    Table posts {
        id integer [primary key]
        title varchar
        body text [note: 'Content of the post']
        user_id integer
        created_at timestamp
    }

    Ref: posts.user_id > users.id // many-to-one

## Community Contributions

* Emacs Mode for DBML (Contributed by ccod): https://github.com/ccod/dbd-mode
* Vim Plugin for DBML (Contributed by jidn): https://github.com/jidn/vim-dbml
