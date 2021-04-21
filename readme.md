# ipfs-regex 

> Regular expression for matching ipfs [content identifiers](https://docs.ipfs.io/concepts/content-addressing/).


## Install

```
$ npm install --save ipfs-regex


```
## Supported CIDv1 default multibase prefixes:

    > *encoding*             *code*                               
    > base16upper            F
    > hexadecimal base32     b
    > base32upper            B
    > base58btc              z
   

## Default CIDv1  multibase prefixes not yet supported:
    > identity               0x00
    > base16                 f
    > base64                 m   
    > base64url              u
    > base64urlpad           U
    > 

see https://github.com/multiformats/multibase#multibase-table

## Usage

```js
const ipfsRegex = require('ipfs-regex');

ipfsRegex().test('QmcRD4wkPPi6dig81r5sLj9Zm1gDCL4zgpEj9CfuRrGbzFr');
//=> true

ipfsRegex().test('bafybeigrf2dwtpjkiovnigysyto3d55opf6qkdikx6d65onrqnfzwgdkfa');
//=> true

## API

### ipfsRegex()

Returns a regex for matching IPFS CIDs.


## License

MIT © [Kevin Mårtensson](http://kevinmartensson.com)
