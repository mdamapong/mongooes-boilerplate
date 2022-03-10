# mongooes-boilerplate

>>Open your VS Code and click on the settings button in the bottom-left corner.

<img width="1721" alt="1" src="https://user-images.githubusercontent.com/58996441/157767784-93e37c9b-e68d-4292-9507-4f986bcb6408.png">


>>Click on User Snippets.
<img width="1723" alt="2" src="https://user-images.githubusercontent.com/58996441/157767867-8f088177-5861-44c9-8e7b-8dd6d5853715.png">

>> You’ll see a dropdown at the top of a list of various JSON files.

<img width="1100" alt="3" src="https://user-images.githubusercontent.com/58996441/157767945-ee36f999-8682-4b77-93da-073e9ceed809.png">

>> Add JS code to JS.JSON file

<img width="1389" alt="4" src="https://user-images.githubusercontent.com/58996441/157768033-9a294d47-0416-44e2-a355-b32f1b1ea323.png">
>>> "prefix" is your shortcut

```
	"javascript snippets": {
		"prefix": "mongooseconnect",
		"body": [
"const mongoose = require('mongoose');",

"const Tweet = require('./tweet.js');",

"require('dotenv').config();",

"const db = mongoose.connection;",
"const mongoURI = process.env.DATABASE_URL;",

"mongoose.connect(mongoURI, () => {",
	"console.log('Connection with MongoDB is a go✅');",
		"});",

"db.on('error', (err) => console.log(err.message + ' is MongoDB not running?'));",
"db.on('connected', () => console.log('MongoDB connected on: ', mongoURI));",
"db.on('disconnected', () => console.log('MongoDB disconnected'));",


"//Code below is optional",
"setTimeout(() => {",
	"db.close();",
		"},",
		"5000);"

		],
		"description": "to produce the main snippet for mongoose connection"
	}
```
reference/credit https://www.geeksforgeeks.org/how-to-create-the-boilerplate-code-in-vs-code/
