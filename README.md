# CORE MODULES:
	http, https, fs, os, path.
# Useful resources:
	Official Node.js Docs: 
	https://nodejs.org/en/docs/guides/

	Full Node.js Reference (for all core modules): 
	https://nodejs.org/dist/latest/docs/api/

	More about the Node.js Event Loop: 
	https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/

	Blocking and Non-Blocking Code: 
	https://nodejs.org/en/docs/guides/dont-block-the-event-loop/

# You can basically differentiate between:

	Global features: Keywords like const or function but also some global objects like process

	Core Node.js Modules: Examples would be the file-system module ("fs"), the path module ("path") or the Http module ("http")

	Third-party Modules: Installed via npm install - you can add any kind of feature to your app via this way

	Global features are always available, you don't need to import them into the files where you want to use them.

	Core Node.js Modules don't need to be installed (NO npm install is required) but you need to import them when you want to use features exposed by them.

	Example:

	const fs = require('fs');

	You can now use the fs object exported by the "fs" module.

	Third-party Modules need to be installed (via npm install in the project folder) AND imported.

	Example (which you don't need to understand yet - we'll cover this later in the course):

	// In terminal/ command prompt
	npm install --save express-session
	// In code file (e.g. app.js)
	const sessions = require('express-session');
	
 # Autorestart the server:
 	Using nodemon
	To install nodemon we have to use following commands
	npm i nodemon -g
	
 # To add debug configuration
 	to restart debugger whenever you change in the file, you need to add some configuration in file
	Run -> Add Configuration -> select enviroment
	then in the launch.js file need to add some properties
	
	"configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "Launch Program",
            "skipFiles": [
                "<node_internals>/**"
            ],
            "program": "${workspaceFolder}\\app.js",
            "restart": true,
            "runtimeExecutable": "nodemon",
            "console": "integratedTerminal",
        }
    ]
    
    This article will be very helpful: 
    https://code.visualstudio.com/docs/nodejs/nodejs-debugging
    
# What is Express.Js
	Writing server side logic is complex so express js help us to write simple code.
	command tu install express js:
	npm i --save express

