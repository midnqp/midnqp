# API Design
![](https://static.apiary.io/assets/3PBYeVhR.png)

Table of contents:
- Prelude
- Errors
- Client libraries

## Prelude

Google Cloud API [design guide](https://cloud.google.com/apis/design)
has been used inside Google since 2014. This guide is made public for
outside devleopers.

### Resource-oriented design
Most of Google's APIs are resource-oriented. Goal of the guide is to
help develops design networked APIs that are: 
- simple
- consistent
- easy-to-use

The core principle of REST is to define names resources that can be
manipulated using a smaller number of methods. the resource and
methods are "noums" and "verbs" of the APIs. This resourlts in fewer
things to learn.

Design flow steps:
1. What type of resources an API provides? _(??)_
2. Relationship between resources _(??)_
3. Resource schema based on types & relationships.
4. Decide resource schema. _(ok)_
5. Attach minimum set of methods to resources. _(ok)_

### REST API
See the article on [REST API]().
