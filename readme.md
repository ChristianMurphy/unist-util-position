# unist-util-position

[![Build][build-badge]][build]
[![Coverage][coverage-badge]][coverage]
[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]
[![Sponsors][sponsors-badge]][collective]
[![Backers][backers-badge]][collective]
[![Chat][chat-badge]][chat]

[**unist**][unist] utility to get the positional info of nodes.

## Install

[npm][]:

```sh
npm install unist-util-position
```

## Use

```js
var remark = require('remark')
var position = require('unist-util-position')

var tree = remark().parse('# foo\n\n* bar\n')

console.log(position(tree))
console.log(position.start(tree))
console.log(position.end(tree))

console.log(position())
console.log(position.start())
console.log(position.end())
```

Yields:

```js
{start: {line: 1, column: 1, offset: 0}, end: {line: 4, column: 1, offset: 13}}
{line: 1, column: 1, offset: 0}
{line: 4, column: 1, offset: 13}
{start: {line: null, column: null, offset: null}, end: {line: null, column: null, offset: null}}
{line: null, column: null, offset: null}
{line: null, column: null, offset: null}
```

## API

### `position(node?)`

Get the positional info of `node` ([`Node?`][node]).
Returns [`Position`][position].

### `position.start(node?)`

### `position.end(node?)`

Get the start or end points in the positional info of `node` ([`Node?`][node]).
Returns [`Point`][point].

## Contribute

See [`contributing.md` in `syntax-tree/.github`][contributing] for ways to get
started.
See [`support.md`][support] for ways to get help.

This project has a [code of conduct][coc].
By interacting with this repository, organization, or community you agree to
abide by its terms.

## License

[MIT][license] © [Titus Wormer][author]

<!-- Definitions -->

[build-badge]: https://github.com/syntax-tree/unist-util-position/workflows/main/badge.svg

[build]: https://github.com/syntax-tree/unist-util-position/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/syntax-tree/unist-util-position.svg

[coverage]: https://codecov.io/github/syntax-tree/unist-util-position

[downloads-badge]: https://img.shields.io/npm/dm/unist-util-position.svg

[downloads]: https://www.npmjs.com/package/unist-util-position

[size-badge]: https://img.shields.io/bundlephobia/minzip/unist-util-position.svg

[size]: https://bundlephobia.com/result?p=unist-util-position

[sponsors-badge]: https://opencollective.com/unified/sponsors/badge.svg

[backers-badge]: https://opencollective.com/unified/backers/badge.svg

[collective]: https://opencollective.com/unified

[chat-badge]: https://img.shields.io/badge/chat-discussions-success.svg

[chat]: https://github.com/syntax-tree/unist/discussions

[license]: license

[author]: https://wooorm.com

[npm]: https://docs.npmjs.com/cli/install

[contributing]: https://github.com/syntax-tree/.github/blob/HEAD/contributing.md

[support]: https://github.com/syntax-tree/.github/blob/HEAD/support.md

[coc]: https://github.com/syntax-tree/.github/blob/HEAD/code-of-conduct.md

[unist]: https://github.com/syntax-tree/unist

[node]: https://github.com/syntax-tree/unist#node

[position]: https://github.com/syntax-tree/unist#position

[point]: https://github.com/syntax-tree/unist#point
