## edge-ps-core

# This package is now deprecated in favor of `edge-ps`
## NPM: https://www.npmjs.com/package/edge-ps
## GitHub: https://github.com/agracio/edge-ps 

### This is a PowerShell compiler for Edge.Js using dotnet 8.0.

Forked from https://github.com/dfinke/edge-ps to support dotnet core projects.  
For full overview, examples and documentation visit https://github.com/dfinke/edge-ps 

### Differences from `edge-ps`
* `edge-ps` only supports .NET Framework 4.x, `edge-ps-core` supports dotnet 8

### Requirements
* dotnet version 8 or higher
* `edge-js` version 21.7.4 or higher
* cannot be scripted directly from .js, requires a dotnet project with reference to `Microsoft.PowerShell.SDK`.  
Sample code is provided at https://github.com/agracio/edge-js-quick-start.

### Usage

```
npm install edge-js
npm install edge-ps-core
```

```js
    var edge = require('edge-js');

    var hello = edge.func('ps-core', function () {/*
        "PowerShell welcomes $inputFromJS on $(Get-Date)"
    */});

    hello('Node.js', function (error, result) {
        if (error) throw error;
        console.log(result[0]);
    });
```  
  
Visit https://github.com/dfinke/edge-ps for more examples

