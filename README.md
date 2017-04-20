# nano-logger
[https://github.com/baontp/nano-logger.git](https://github.com/baontp/nano-logger.git)

## INSTALL
```
$  npm install nano-log --save
```

## SUMMARY
This logger utility is inspired by github.com/quirkey/node-logger
It can log onto file by date.

### Instantiation:
create a logger with tag:
```javascript
    let logger = require('nano-log').createLogger(TAG);
```

setup to log to file
```javascript
    let log = require('nano-log');
    log.initLogFile('log_file');
```

### Format:

[yyyy-mm-dd HH:MM:ss] [LEVEL] [TAG] [PREFIX]	 message

### Usage:

A logger has 5 different levels of logging in a specific order:

    'fatal', 'error', 'warn', 'info', 'debug'
    
Any of the logging methods take n arguments, which are each joined by ' ' (similar to console.log())

```javascript
    logger.info('This is a info message');
    logger.warn(username, 'already logged in server');
```

### Customization:

You can completely customize the look of the log by overriding the `format()` method on a logger.

    logger.format = function(level, date, message) {
      return date.getTime().toString() + "; " + message;
    };
    logger.debug('message');
    //=> 1276365362167;  message
    
## COMMENTS/ISSUES:

Fork it, if you like.

## LICENSE

MIT, see the source.
