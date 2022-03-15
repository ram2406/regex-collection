# regex-collection
The regular expression book for me

## regex for find import to replace require
```regex
import (\{.*?\}|\w+|\{(\w|\n|,|\s)*?\}) from (.*);
```
### replace
```regex
const $1 = require($3);
```
### example data
```js
import http from "http";
import {
  addGatewayDataSourceToSubscriptionContext,
  getGatewayApolloConfig,
  makeSubscriptionSchema
} from "federation-subscription-tools";
import { ApolloGateway } from "@apollo/gateway";
import {
  execute,
  getOperationAST,
  GraphQLError,
  parse,
  subscribe,
  validate
} from "graphql";
import { useServer } from "graphql-ws/lib/use/ws";
import ws from "ws";

import { LiveBlogDataSource } from "./datasources/LIveBlogDataSource/index";
import { resolvers } from "./resolvers";
import { typeDefs } from "./typeDefs";
```
### expected result
```js
const http = require("http");

const {
  addGatewayDataSourceToSubscriptionContext,
  getGatewayApolloConfig,
  makeSubscriptionSchema
} = require("federation-subscription-tools");
const { ApolloGateway } = require("@apollo/gateway");
const {
  execute,
  getOperationAST,
  GraphQLError,
  parse,
  subscribe,
  validate
} = require("graphql");
const { useServer } = require("graphql-ws/lib/use/ws");
const ws = require("ws");

const { LiveBlogDataSource } = require("./datasources/LIveBlogDataSource/index");
const { resolvers } = require("./resolvers");
const { typeDefs } = require("./typeDefs");

```
