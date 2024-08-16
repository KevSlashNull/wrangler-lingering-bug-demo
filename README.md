# wrangler-lingering-bug-demo

## Steps to reproduce

1. Run `git clone https://github.com/KevSlashNull/wrangler-lingering-bug-demo`
2. Run `cd wrangler-lingering-bug-demo`
3. Run `npm install`
4. Run `npx wrangler dev`

See an error like:

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
