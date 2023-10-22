# DEPRECATED

Use analog implementation in [more-proms](https://npmjs.com/package/more-proms) instead.


# Resable promise

Simple promise subclass, allowing for resolvement outside of callback (as property).

## Installation

```shell
 $ npm i resable-promise
```

## Usage

Do this:

```ts
import ResablePromise from "resable-promise"

const prom = new ResablePromise()
// later...
prom.res()
```

So you dont have to do this:

```ts
let promRes
const prom = new Promise(res => promRes = res)
// later ...
promRes()
```

Only convinience, as I see myself doing this a lot. And this provides type safety without effort.

### On Settled

Is a promise that resolves when the base promise is ether resolved or rejected.

```ts
const prom = new ResablePromise()

prom.settled.then(() => console.log("settled"))
```


## Contribute

All feedback is appreciated. Create a pull request or write an issue.
