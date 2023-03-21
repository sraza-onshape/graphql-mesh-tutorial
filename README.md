# GraphQL Mesh Services examples

*Originally found [here](https://the-guild.dev/graphql/mesh/docs/getting-started/installation) - thanks to the team behind GraphQL Tools!*

## Setup


### Build all APIs

First, if you are new to using `yarn`, then you'll need to install its `workspace-tools` plugin - this is a one-time action:

```bash
$ yarn plugin import workspace-tools
```

Then, `cd` into each package and run the following:
```bash
$ mkdir dist
$ npm run build
$ yarn install
```

Then, `cd` back to this root directory and run:

```bash
$ yarn workspaces foreach run build
```
For more info on this command, see the `yarn` docs [here](https://yarnpkg.com/cli/workspaces/foreach#options-A%2C-all).

<p>&nbsp;</p>

## Examples

### Start the single source (Books Gateway) Mesh Gateway

```
yarn run start-single-source
```

More information on https://graphql-mesh.com/docs/getting-started/your-first-mesh-gateway.


<p>&nbsp;</p>


### Start the single source (Books API without definition) Mesh Gateway

```
yarn run single-source-no-source-definition
```

More information on https://graphql-mesh.com/docs/getting-started/sources-with-no-definition


<p>&nbsp;</p>

### Start the multiple sources Mesh Gateway

```
yarn run start-multiple-sources
```

More information on https://graphql-mesh.com/docs/getting-started/combine-many-sources.

<p>&nbsp;</p>

### Start the multiple sources Mesh Gateway (with programmatic resolvers)

```
yarn run start-multiple-sources-prog-resolvers
```

More information on https://graphql-mesh.com/docs/guides/extending-unified-schema#extending-the-unified-schema.


<p>&nbsp;</p>

----

<p>&nbsp;</p>

## Services

### Books API (OpenAPI)
- `GET /books`
- `GET /books/:id`
- `GET /books/categories`


### Authors API (gRPC)
- `GetAuthor`
- `ListAuthors`

### Stores (GraphQL)
- `stores` Query
- `bookSells(storeId: ID!)` Query
