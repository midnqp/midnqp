# REST

![](https://static.apiary.io/assets/22L9GTDX.png)

REST stands for 'Representational State Transfer'. This is an
architectural style for hypermedia state transfer. A web API conforming to REST architectural style is a REST API.

## Guiding Principles

- Uniform interface
- Client-server: separate backend and frontend.
- Stateless: each HTTP request contains all info e.g. session, auth
    to, to understand the individual request.
- Cacheable
  - GET: always
  - POST: `expire`, `cache-control`, `etag`, `last-modified`
  - PUT, DELETE: never
- Layered system: each layer cannot see beyond their layer
- Code-on-demand: downloadable scripts to be executed by client

A collection of individually-addressable resources. These resources are
referred by resource names and manipulated via small set of method. 

## Resource

APIs are modeled as a resource hierarchy - where each node is either a
collection, or a single resource. A single resource has some state, or
sub-resources. As example, Gmail API has a collection of user. Each
user has the following:
- a collection of messages
- a collection of labels
- a profile resource
- several simple setting resources

#### Consistency

Some constraints in REST API naming ensures a design of scalable API endpoints:

Use plural nouns to name, and represent resources. Example: users, orders, categories.
Use hypen, not underscores. Use lowercase letters in URI, never camel-case. GET /food-categories, not GET /foodCategories.
No trailing forward slash. Example: GET /users/ is wrong, and GET /users is correct.
Never use CRUD function names in URIs, like /users/list or /users/create. Rather use:
GET /users - get all users.
GET /users/:id - get a single user.
POST /users/:id - create a single user.
PUT /users/:id - update a single user.
DELETE /users/:id - delete a single user.
Use query components to filter collection, never use for anything else. Example: /users?region=Malaysia&sort=createdAt.
