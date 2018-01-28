# lerna-rollup-watch

Simplified example of problem with lerna + rollup -w

1. Clone the repo: `git clone https://github.com/schneidmaster/lerna-rollup-watch.git`

2. Install dependencies: `yarn install`

3. Run `yarn watch`

* Expected: lerna runs the `watch` command in each package, and the commands stay alive indefinitely waiting for changes

* Actual: lerna runs the `watch` command in each package, and each command exits as soon as the first build is complete

I think this is a problem specifically with rollup, because babel's watch mode works fine (as can be seen in this repo with `yarn watch:babel`) -- so it's not that lerna is killing the processes or something.
