﻿# ES6 - Modules
related: [http://exploringjs.com/es6/ch_modules.html](http://exploringjs.com/es6/ch_modules.html)

### export and import
```javascript
// m.js
export var username = 'xiaofeng';
export const gender = 'male';
export function saySomething(something) {
    console.log(something);
}

// index.js
import {username, gender, saySomething} from './m'; 
console.log(username); // xiaofeng
console.log(gender);  // male
saySomething('I am ' + username); // I am xiaofeng
```

### import the complete module
```javascript
import * as lib from './m';

console.log(lib.gender);
lib.saySomething(lib.username);
```

### export default
```javascript
// m.js
export default function(something) {
    console.log(something);
}

// index.js
import saySomething from './m';

saySomething('hehe'); // hehe
```

### alias via as
```javascript
import {username as name} form 'm';
```

### imports are hoisted
```javascript
saySomething('hehe');

import saySomething from './m';
```


