---
title: "About the GraphQLResolveInfo Object"
date: 2022-03-28T16:47:36+01:00
draft: false
---
The `GraphQLResolveInfo` object contains data specific to the current operation and resolver, as well as global data that applies to the entire GraphQL schema:

* *fieldName* — the name of the field being resolved for the current resolver
* *fieldNodes* — a representation of the selection set of the GraphQL operation
* *returnType* — what is the type of the field currently being resolved?
* *parentType* — what is the type of the parent object?
* *path* — what fields were traversed to reach the current field being resolved
* *schema* — the executable GraphQLSchema object, for the entire GraphQL schema, not just the type being resolved
* *fragments* — any fragments used in the query
* *rootValue* — the rootValue argument passed to the GraphQL execution function
* *operation* — the Abstract Syntax Tree (AST) of the GraphQL operation
* *variableValues* —*the values of any GraphQL variables used in the operation
(Field list taken from: [GraphQL ResolveInfo Deep Dive. Building Efficient GraphQL Resolvers By… | by William Lyon | GRANDstack - GraphQL, React, Apollo, Neo4j Database](https://blog.grandstack.io/graphql-resolveinfo-deep-dive-1b3144075866))

Can use this data to add logging to middleware to inspect resolvers.
