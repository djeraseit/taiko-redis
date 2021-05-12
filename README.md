# Taiko Redis Plugin
A taiko plugin to interact with a redis database.
## Install redis-cli dependency
This plugin uses redis-cli to cointeract with the redis server. It requires rediscli to be available from the command line and a redis server.
### Mac OS X
### Ubuntu
### CentOS
### Windows
## Install Taiko Redis Plugin
## Example

Add this script in a file `script.js`.
`
const { openBrowser, closeBrowser, click, goto, video } = require('taiko');

(async () => {
  try {
    await openBrowser();
    // Connect to Redis Server
    await redis.connectServer('redis15.localnet.org',{port:6379,database:0});
    // Check if Redis is Working
    await redis.Ping();
    await goto('https://www.linkedin.com/in/theodisbutler/');
    // Set key
    await redis.Set({key:'website',value:'https://www.linkedin.com/in/theodisbutler/'});
    // Update key with value
    await redit.Update({key:'website',value:'https://theodis.com'});
    // Delete key
    await redit.Delete('websitekey');
    // Get key value
    await redis.Get(websitekey);
    
  } finally {
    // Disconnect from Redis Server
    await redis.disconnectServer();
    await closeBrowser();
  }
})();
`
