# rollup-plugin-merge

Rollup plugin to merge JSON files

## Install

```sh
npm i -D rollup-plugin-merge
```

## Usage

```js
import merge from 'rollup-plugin-merge';

export default {
  input: 'src/index.js',
  output: {
    file: 'dist/bundle.js',
    format: 'iife',
    name: 'app'
  },
  plugins: [
    merge({
      input: ['src/1.json', 'src/2.json'],
      output: 'dist/config.json',
      verbose: true,
      watch: true
    })
  ]
};
```

### Options
  - verbose (default is `false`). Enable/disable logging
  - watch (default is `false`). Enable/disable watching. If disabled then copy only on start
