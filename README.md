## Project status : in progress


### Introduction

The simple library for event streams. OOP programming consider a stream as an object. On the other hand, in functional programming a stream is high order function.

#### OOP (zen-observable)

```javascript
const unsubscribe = Observable.of(1, 2, 3)
  .map(x => x + 1)
  .filter(x => x % 2 !== 0)
  .subscribe({
    next: value => console.log(value),
    error: err => console.error(err),
    done: () => console.log('done')
  });
```

#### FP

```ocaml
let unsubscribe = [1; 2; 3]
  |> Stream.Async.of_list ~delay:1000
  |> Stream.map (fun x -> x + 1)
  |> Stream.filter (fun x -> x mod 2 <> 0)
  |> Stream.subscribe (fun x -> x |> string_of_int |> print_endline)
```


-----------------------
### API

#### `module Stream`

* [x] [empty](./docs/empty.md)
* [x] [of_item](./docs/of_item.md)
* [x] [later](./docs/later.md)
* [x] [prepend](./docs/prepend.md)
* [x] [scan](./docs/scan.md)
* [x] [skip](./docs/skip.md)
* [x] [skip_while](./docs/skip_while.md)
* [x] [take](./docs/take.md)
* [x] [take_while](./docs/take_while.md)
* [x] [chain](./docs/chain.md)
* [x] [chain_latest](./docs/chain_latest.md)
* [x] [subcribe](./docs/subscribe.md)
* [x] [of_list](./docs/of_list.md)
* [x] [of_list_reverse](./docs/of_list_reverse.md)
* [x] [of_array](./docs/of_array.md)
* [x] [of_array_reverse](./docs/of_array_reverse.md)
* [x] [map](./docs/map.md)
* [x] [map2](./docs/map2.md)
* [x] [map3](./docs/map3.md)
* [x] [filter](./docs/filter.md)
* [x] [ap](./docs/ap.md)
* [x] [Async.of_list](./docs/of_list.md)
* [x] [Async.of_array](./docs/of_array.md)

------------------------
### Setup

#### Build
```
npm run build
```

#### Watch

```
npm run watch
```

#### Editor
If you use `vscode`, Press `Windows + Shift + B` it will build automatically