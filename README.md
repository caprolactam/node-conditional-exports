This repository test which key takes precedence within `exports` objects, when using [Conditional Exports](https://nodejs.org/api/packages.html#conditional-exports) in Node.js.

## Run the test

```bash
npm install
npm run dev
// try npm run dev:wokerd or something.
```

## The expected

The expected behavior is as follows:

When run `npm run dev:workerd`, it outputs:
**"This is worked environment!"**

When run `npm run dev:node`, it outputs:
**"This is node environment!"**

When run `npm run dev:browser`, it outputs:
**"This is node environment!"**

It do not outputs: **"This is browser environment!"**. This is because, in the library's export object, the "node" key has a higher precedence than the "browser" key.
