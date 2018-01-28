# lerna-rollup-watch

Simplified example of problem with lerna + rollup -w

1. Clone the repo: `git clone https://github.com/schneidmaster/lerna-rollup-watch.git`

2. Install dependencies: `yarn install`

3. Run `yarn watch`

* Expected: lerna runs the `watch` command in each package, and the commands stay alive indefinitely waiting for changes

* Actual: lerna runs the `watch` command in each package, and each command exits as soon as the first build is complete
