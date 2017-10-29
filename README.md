# MEAN stack based sample Web application

## Prerequisites
Node.js and npm are essential to run and deploy the applicaiton and to continue further.
    
<a href="https://docs.npmjs.com/getting-started/installing-node" target="_blank" title="Installing Node.js and updating npm">
Get it now</a> if it's not already installed on your machine.
 
**Verify that you are running at least node `v4.x.x` and npm `3.x.x`**
by running `node -v` and `npm -v` in a terminal/console window.
Older versions produce errors.

We recommend [nvm](https://github.com/creationix/nvm) for managing multiple versions of node and npm.


## Install npm packages

> See npm and nvm version notes above

Install the npm packages described in the `package.json` and verify that it works:

```shell
npm install
npm start
```

>Doesn't work in _Bash for Windows_ which does not support servers as of January, 2017.

The `npm start` command first compiles the application, 
then simultaneously re-compiles and runs the `lite-server`.
Both the compiler and the server watch for file changes.

Shut it down manually with `Ctrl-C`.

You're ready to write your application.

### npm scripts to compile .ts source to .js files in the Angular applicaiton(to be executed from Client dir as it is the Angular project)

We've captured many of the most useful commands in npm scripts defined in the `package.json`:

* `npm start` - runs the compiler and a server at the same time, both in "watch mode".


### node scripts to build and run the server
We've captured many of the most useful commands in npm scripts defined in the `package.json`:

* `nodemon` - This command should be run from the project's root dir(MEANDEMO). This runs the server in watch mode and checks for any changes in the source code to compile and deploy immediately. 

### Install bower js for frontend module dependency management
* `npm install -g bower` - This command will install bower.js globally
* `bower -version` - This should return the version if bower is installed globally and system's path is set
* Create a file called ".bowerrc" with a directory entry as below. Then open commandprompt at the current directory which contains the .bowerrc file. Then run `bower install -bootstrap --save` to install bootstrap and its dependencies under the below folder inside current directory.
   {directory: client/bower_components}
* `bower uninstall bootstrap` - This should remove bootstrap libraries from bower_components


### File path reference. The following path guidelines applicable for web.
* '/' represents root of frontend application. In this case it is 'client' dir. Means
*  / = https://localhost:3000/client 
*  /src/assets/styles.css = https://localhost:3000/client/src/assets/styles.css


### Current Issues:
* Angular loader or typescript not loading the files with the paths => ../ in the import statements
