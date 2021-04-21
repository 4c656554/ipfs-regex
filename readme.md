# ipfs-regex 

> Regular expression for matching ipfs [content identifiers](https://docs.ipfs.io/concepts/content-addressing/).


## Install

```
$ npm install --save ipfs-regex
```


## Usage

```js
const base64Regex = require('ipfs-regex');

ipfsRegex().test('dW5pY29ybg== foo bar');
//=> true

ipfsRegex({exact: true}).test('dW5pY29ybg== foo bar');
//=> false

ipfsRegex({exact: true}).test('dW5pY29ybg==');
//=> true

'foo dW5pY29ybg== bar Ym9hdA=='.match(base64Regex());
//=> ['dW5pY29ybg==', 'Ym9hdA==']
```


## API

### ipfsRegex([options])

Returns a regex for matching base64 encoded strings.


## License

MIT © [Kevin Mårtensson](http://kevinmartensson.com)
