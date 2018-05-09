# Middleware for NodeJS

Zero dependencies middleware implementation. Each middleware function shall be called with any number of arguments, reference to next function shall be passed as the last argument;

### Installation

```
npm install --save middleware-nodejs
```

### Usage

import:
```javascript
const middleware = require('middleware-js')();
```

pass middleware function:

```javascript
middleware.use((req, res, next) => {
	//...
    next();
});
```

**note** that next() call is required to continue chain execution.

to kick of the chain run:
```javascript
middleware.handle(req, res);
```