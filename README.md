png2psd
=======

convert PNG file to PSD file.

[![Build Status](https://secure.travis-ci.org/ynakajima/png2psd.png?branch=master)](http://travis-ci.org/ynakajima/png2psd) [![npm version](https://badge.fury.io/js/png2psd.svg)](http://badge.fury.io/js/png2psd) ![node dependencies](https://david-dm.org/ynakajima/png2psd.png)

## cli

### install
```sh
npm install -g png2psd
```

### usage
```sh
png2psd source.png export.psd
```

## node module

### install
```sh
npm install png2psd
```

### usage
```node
var png2psd = require('png2psd'),
    fs = require('fs');

// file path
var pngFilePath = 'source.png';
var psdFilePath = 'export.psd';

// convert
png2psd(pngFilePath, function(psdFileBuffer) {
  // save psd file
  fs.writeFile(psdFilePath, psdFileBuffer, function(err) {
    if (err) throw err;
    console.log('save psd file.');
  });
});
```