# NoSQL

All praises are for Allah. I started working on this piece on 30 June 2022 from
questioning whether MongoDB is an ORM. MongoDB is rather an ODM, and
REST has more similarity to ODM.


Table of contents:
- [NoSQL: A prelude](#nosql-a-prelude)
- [NoSQL: Types](#nosql-types)
- [JSON vs BSON](#json-vs-bson)
- [ORM vs ODM](#orm-vs-odm)
- [Horizontal vs vertical scaling](#horizontal-vs-vertical-scaling)

## NoSQL: A prelude

NoSQL databases are non-tabular database, whch mostly store
unstructured JSON-like data.

4 major NoSQL database types:
- Document: similar to JSON, contains pairs of key-value.
- Key-value: each item contains keys and values.
- Wide-column: store data in tables, rows, and dynamic columns.
- Graph: 
  - Stores data in nodes and edges. Nodes store info about peoples,
    places - and edges store info about relationship between the
    nodes.
  - Usually runs alongside traditional databases, because these
    databases are optimized for relations - to avoid JOIN among
    tables.

## NoSQL: Types
