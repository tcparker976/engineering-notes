# [Clipboard Health] — [Software Engineer]

**Date:** 2026-03  
**Round:** Technical 1

## What they asked

- Explain pagination bug in technical assessment
- Explain a filter on shifts in the worplaces script
- Write a retry method for API calls
- Wrtie a batch processing method that solves the problem of holding all shifts and workplaces in memory

## What I did well

- ??

## What I'd do differently

- Clearer communication of pagination bug. I was asked how I found it.
- Filter explanation - I said I didn't need one of the filters, he said I did. Not clear
- Fetch retry method. I didn't implement exponential backoff right away
- Batch processing - first he asked me if there was anything I would improve which was vague. Then he dropped a hint about batch processing to avoid keeping all the workplaces/shifts in memory.


## Follow-up / prep for next time

- How to write a simple retry method with typescript - memorize.
### Simple retry in TypeScript

```ts
type AsyncFn<T> = () => Promise<T>;

export async function retry<T>(
  fn: AsyncFn<T>,
  retries = 3,
  delayMs = 500
): Promise<T> {
  let lastError: unknown;

  for (let attempt = 0; attempt <= retries; attempt++) {
    try {
      return await fn();
    } catch (err) {
      lastError = err;

      if (attempt === retries) {
        throw lastError;
      }

      await new Promise((resolve) => setTimeout(resolve, delayMs));
    }
  }

  throw lastError;
}
```

- How to write a simple batch processing method for a paginated api with typescript - memorize.
### Simple batch processing in Typescript

```ts
async function processPaginatedInBatches<T, R>(
  fetchPage: (page: number) => Promise<{ items: T[]; hasNext: boolean }>,
  batchSize: number,
  worker: (item: T) => Promise<R>
): Promise<R[]> {
  const results: R[] = [];
  let page = 1;
  let hasNext = true;
  while (hasMore) {
    const { items, hasNext: more } = await fetchPage(page);
    hasNext = next;
    page++;
    // process this page's items in batches
    const pageResults = await Promise.all(items.map(worker));
    results.push(...pageResults);
  }
  return results;
}
```