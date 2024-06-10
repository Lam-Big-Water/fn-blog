---
author: Sam Lam
categories: ["studio tips"]
date: 10/6/2024
featured: false
image: ./images/coffee.jpg
title: React Query
---

# Point

- `staleTime`: Query instances via useQuery or useInfiniteQuery by default consider cached data as stale.
```tsx
staleTime: 10000,
```

- `gcTime`: Query results that have no more active instances of useQuery, useInfiniteQuery or query observers are labeled as "inactive" and remain in the cache in case they are used again at a later time.
```tsx
gcTime: 5000,
```

- `retry & retryDelay`: Queries that fail are silently retried 3 times, with exponential backoff delay before capturing and displaying an error to the UI.
```tsx
retry: 5,
```