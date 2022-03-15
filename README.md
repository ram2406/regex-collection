# regex-collection
The regular expression book for me

## import (\{.*?\}|\w+|\{(\w|\n|,|\s)*?\}) from (.*);
### replace
const $1 = require($3);
#### example data
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
