# javascript-error-handler

- install 
```js
npm install chalk 
```
```js
//Anti Error
const chalk = require('chalk');
module.exports = async (client) =>{
    process.on('unhandledRejection', async(reason, p) =>{
        console.log(chalk.red.bold("[Anti-crash] ") + chalk.white.bold("Unhandled Rejection/Catch"));
        console.log(reason, p);
    });

    process.on('uncaughtException', async(err, origin) =>{
        console.log(chalk.red.bold("[Anti-crash] ") + chalk.white.bold("Uncaught Exception/Catch"));
        console.log(err, origin);
    });

    process.on('uncaughtExceptionMonitor', async(err, origin) =>{
        console.log(chalk.red.bold("[Anti-crash] ") + chalk.white.bold("Uncaught Exception/Catch (MONITOR)"));
        console.log(err, origin);   
    });
}
```
