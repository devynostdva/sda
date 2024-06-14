# sda
sda
Install the exact v8 canary version
jobs:
  build:
    runs-on: ubuntu-latest
    name: Node sample
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 'v20.1.1-v8-canary20221103f7e2421e91'
      - run: npm ci
      - run: npm test
Nightly versions
You can specify a nightly version to download it from https://nodejs.org/download/nightly.

Install the nightly build for a major version
jobs:
  build:
    runs-on: ubuntu-latest
    name: Node sample
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '16-nightly' # it will install the latest nightly release for node 16
      - run: npm ci
      - run: npm test
Install the nightly build for a specific version
jobs:
  build:
    runs-on: ubuntu-latest
    name: Node sample
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '16.0.0-nightly' # it will install the latest nightly release for node 16.0.0
      - run: npm ci
      - run: npm test
Install an exact nightly version
jobs:
  build:
    runs-on: ubuntu-latest
    name: Node sample
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '16.0.0-nightly20210420a0261d231c'
      - run: npm ci
      - run: npm test)
