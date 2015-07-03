# Sublime Settings
Copy the snippets, keybindings and preferences json to sublime.

%APPDATA%/Sublime Text 3/Packages

Install Plugins
 - Emmet
 - Package Control
 - JSHint Gutter
 - HTML-CSS-JS Prettify
 - AdvanceNewFile

Copy .jshintrc to JSHint Gutter options

Copy .jsbeautify to HTML-CSS-JS Prettify options

Set both format on save option to true

## Console

### [cd] console.dir

```javascript
console.dir("$1", $1);
```

### [ce] console.error

```javascript
console.error("$1", $1);
```

### [cl] console.log

```javascript
console.log("$1", $1);
```

### [cw] console.warn

```javascript
console.warn("$1", $1);
```

### [de] debugger

```javascript
debugger;
```

## DOM

### [ae] addEventListener

```javascript
${1:document}.addEventListener('${2:event}', function(e) {
	${3}
});
```

### [ac] appendChild

```javascript
${1:document}.appendChild(${2:elem});
```

### [rc] removeChild

```javascript
${1:document}.removeChild(${2:elem});
```

### [cel] createElement

```javascript
${1:document}.createElement(${2:elem});
```

### [cdf] createDocumentFragment

```javascript
${1:document}.createDocumentFragment(${2:elem});
```

### [ca] classList.add

```javascript
${1:document}.classList.add('${2:class}');
```

### [ct] classList.toggle

```javascript
${1:document}.classList.toggle('${2:class}');
```

### [cr] classList.remove

```javascript
${1:document}.classList.remove('${2:class}');
```

### [gi] getElementById

```javascript
${1:document}.getElementById('${2:id}');
```

### [gc] getElementsByClassName

```javascript
${1:document}.getElementsByClassName('${2:class}');
```

### [gt] getElementsByTagName

```javascript
${1:document}.getElementsByTagName('${2:tag}');
```

### [ga] getAttribute

```javascript
${1:document}.getAttribute('${2:attr}');
```

### [sa] setAttribute

```javascript
${1:document}.setAttribute('${2:attr}', ${3:value});
```

### [ra] removeAttribute

```javascript
${1:document}.removeAttribute('${2:attr}');
```

### [ih] innerHTML

```javascript
${1:document}.innerHTML = '${2:elem}';
```

### [tc] textContent

```javascript
${1:document}.textContent = '${2:content}';
```

### [qs] querySelector

```javascript
${1:document}.querySelector('${2:selector}');
```

### [qsa] querySelectorAll

```javascript
${1:document}.querySelectorAll('${2:selector}');
```

## Loop

### [fe] forEach

```javascript
${1:myArray}.forEach(function(${2:elem}) {
	${3}
});
```

### [fi] for in

```javascript
for (${1:prop} in ${2:obj}) {
	if (${2:obj}.hasOwnProperty(${1:prop})) {
		${3}
	}
}
```

## Function

### [fn] function

```javascript
function ${1:methodName}(${2:arguments}) {
	${3}
}
```

### [afn] anonymous function

```javascript
function(${1:arguments}) {
	${2}
}
```

### [pr] prototype

```javascript
${1:ClassName}.prototype.${2:methodName} = function(${3:arguments}) {
	${4}
}
```

### [iife] immediately-invoked function expression

```javascript
(function(window, document, undefined) {
	${1}
})(window, document);
```

### [call] function call

```javascript
${1:methodName}.call(${2:context}, ${3:arguments})
```

### [apply] function apply

```javascript
${1:methodName}.apply(${2:context}, [${3:arguments}])
```

### [ofn] function as a property of an object

```javascript
${1:functionName}: function (${2:arguments}) {
	${3}
}
```

## Timer

### [si] setInterval

```javascript
setInterval(function() {
	${2}
}, ${1:delay});
```

### [st] setTimeout

```javascript
setTimeout(function() {
	${2}
}, ${1:delay});
```

## NodeJS

### [source] basic expressjs endpoint
exports.$1 = function (req, res, next) {
 var data = util.get_data([$2], [$3], req.${4:query}),

  start = function () {
   if (!req.access_token) {
    return next('access_token is missing');
   }

   if (typeof data === 'string') {
    return next(data);
   }

   $5
  },
  send_response = function (err, result) {
   if (err) {
    return next(err);
   }

   res.send(result);
  };

 start();
};

### [ase] assert.equal

```javascript
assert.equal(${1:actual}, ${2:expected});
```

### [asd] assert.deepEqual

```javascript
assert.deepEqual(${1:actual}, ${2:expected});
```

### [asn] assert.notEqual

```javascript
assert.notEqual(${1:actual}, ${2:expected});
```

### [me] module.exports

```javascript
module.exports = ${1:name};
```

### [pe] process.exit

```javascript
process.exit(${1:code});
```

### [re] require

```javascript
require('${1:module}');
```
## BDD

### [desc] describe

```javascript
describe('${1:description}', function() {
	${2}
});
```
### [ita] it asynchronous

```javascript
it('${1:description}', function(done) {
	${2}
});
```

### [its] it synchronous

```javascript
it('${1:description}', function() {
	${2}
});
```

### [itp] it pending

```javascript
it('${1:description}');
```

## Misc

### [us] use strict

```javascript
'use strict';
```

### [al] alert

```javascript
alert('${1:msg}');
```

### [co] confirm

```javascript
confirm('${1:msg}');
```

### [pm] prompt

```javascript
prompt('${1:msg}');
```

### [ifor] for statement

```javascript
for (var i = 0, len = ${1:arr}.length; i < len; i++) {
    ${2:$1[i]}$3
```

## License

Forked from [MIT License](http://zenorocha.mit-license.org/) © Zeno Rocha
