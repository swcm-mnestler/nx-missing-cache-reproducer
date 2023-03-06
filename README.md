# NxMissingCacheReproducer

Generated with `npx create-nx-workspace@latest nx-missing-cache-reproducer --preset=ts` + `npx nx generate @nrwl/js:library sample`.
Setting `NX_CACHE_DIRECTORY=.nx` with an empty `.nx` directory causes an error when running a task - can be fixed by running `nx reset`.

Steps to reproduce:
* Clone repository
* `npm ci`
* `npm run reproduce` -> Error
* `npx nx reset`
* `npm run reproduce` -> Success
