---
id: useIsFetching
title: useIsFetching
---

`useIsFetching` is an optional hook that returns the `number` of the queries that your application is loading or fetching in the background (useful for app-wide loading indicators).

```js
import { useIsFetching } from '@tanstack/react-query'
// How many queries are fetching?
const isFetching = useIsFetching()
// How many queries matching the posts prefix are fetching?
const isFetchingPosts = useIsFetching(['posts'])
```

**Options**

- `queryKey?: QueryKey`: [Query Keys](../guides/query-keys)
- `filters?: QueryFilters`: [Query Filters](../guides/filters#query-filters)
- `context?: React.Context<QueryClient | undefined>`
  - Use this to use a custom React Query context. Otherwise, `defaultContext` will be used.

**Returns**

- `isFetching: number`
  - Will be the `number` of the queries that your application is currently loading or fetching in the background.
