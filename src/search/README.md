# AOSearch
Work in Progress Array and Object Searching System for AzurAPI

## Files
```
search
   |- bentch.ts (Benchmarks for algorithms)
   |- compare.ts (Comparison algorithms)
   |- search_typings.ts (Type definitions for the AOSearch class)
   ╵- search.ts (Contains the AOSearch class)
```

## Documentation
Create a new AOSearch Instance
```ts
import { AOSearch } from './search';

const search = new AOSearch(<Dataset>, <SearchOptions>);
```

## Types

### `Dataset`:
```ts
interface Dataset = any[] | Record<string, unknown>;
```

### `SearchOptions`:
```ts
interface SearchOptions {
    keys: string[] | null,
    limit?: number,
    accuracy?: number,
    noMatch?: 'all' | 'none',
    algorithm?: 'distance2' | ((a: string, b: string) => number),
    initialize?: boolean,
    light?: boolean
}
```
