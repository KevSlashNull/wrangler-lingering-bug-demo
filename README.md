# wrangler-lingering-bug-demo

## Steps to reproduce

1. Run `pgrep workerd | wc -l` and note the number of `workerd` processes
2. Run `git clone https://github.com/KevSlashNull/wrangler-lingering-bug-demo`
3. Run `cd wrangler-lingering-bug-demo`
4. Run `npm install`
5. Run `npx wrangler dev`
6. See an error like `MiniflareCoreError [ERR_RUNTIME_FAILURE]: The Workers runtime failed to start. There is likely additional logging output above.`
7. Run `pgrep workerd | wc -l` again and see that the number of processes increased by one!

## Error message

```
/private/tmp/wrangler-lingering-bug-demo/node_modules/wrangler/wrangler-dist/cli.js:29768
            throw a;
            ^

MiniflareCoreError [ERR_RUNTIME_FAILURE]: The Workers runtime failed to start. There is likely additional logging output above.
    at #assembleAndUpdateConfig (/private/tmp/wrangler-lingering-bug-demo/node_modules/miniflare/dist/src/index.js:9281:13)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async Mutex.runWith (/private/tmp/wrangler-lingering-bug-demo/node_modules/miniflare/dist/src/index.js:3522:16) {
  code: 'ERR_RUNTIME_FAILURE',
  cause: undefined
}

Node.js v20.15.1
```
