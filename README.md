# MEAN Stack - Get started

This project is coding belong to the tutorial "How to get started on the MEAN stack" as link on [hackhands](https://hackhands.com/how-to-get-started-on-the-mean-stack/)

---------------------------------

What is MEAN, and why it's GOOD?
So, what is a MEAN stack? The idea is quite simple actually - you have 4 main parts:

* MongoDB as the database
* Express as the web framework
* AngularJS as the frontend framework, and
* Node.js as the server platform

These are some of the advantages of a MEAN stack:

* Single language is used in the whole application
* Support for the MVC pattern
* JSON is used for transfering data
* Node.js's huge module library
* Open source so you can tweak it to your preferences if you're an experienced user

Ok, enough with the chit-chat, now we'll go and install all the necessary parts.

## I. MongoDB
1. Installing
In order to download MongoDB, visit [MongoDB Homepage](http://mongodb.org/downloads)
The installation process outlined shortly is as follows:
a. Extract on Linux
Download and extract the archive file
Run mongod binary (usually located in the bin folder of the extracted archive)
Window
Just run msi file
b. Install
Create the folder to store the database files (the default folder is /data/db)
Make sure port 27017 is free to use

2. Using the MongoDB shell
To start the shell, you have to run the mongo executable in the bin folder of the archive file
. If all went well, the shell automatically conected to the local MongoDB server instance (to the test database) and the terminal in which we've started the mongod service earlier (notice the d) informs us that the new connection has been made

To test the database, lets create a new todos collection by inserting a JSON object with the title property:
$> db.todos.insert({title: "Write a blog post"})
To retrieve the todos object, execute:
$> db.todos.find()
which will output:
{ _id : ObjectId("543262a625cc94a488de8466"), title: "Write a blog post" }

## II. Node.js
1. Installing
In order to download Node.js, visit [Node Homepage](http://nodejs.org/download/)
Installation on Windows and Mac OS X is simple as you just have to run the installer and follow the instructions.
Check Node's version:
```
$> node -v
```
Check NPM's version:
```
$> npm -v
```
If youe npm don't work, please see [this tutorial](http://blog.teamtreehouse.com/install-node-js-npm-windows)

2. Running Node.js
After you successfully installed Node.js, you can execute the following command from your command line tool:
```
$ node
```
This will start the Node.js command-line interface (CLI) and wait for further commands. In order to test it you can execute the following command:
$ console.log('Hello World from Node.js');

which will output:
```
Hello World from Node.js
undefined
```

You can put the code sample from above in a JavaScript file and run it with node. Say for example you made a test.js file which contained the console.log statement from above, you would run it like this:
```
$ node test.js
```

and the output would be:
```
Hello World from Node.js.
```

## III.  Express
1. Installing
To install express all you have to do is execute the following command:
```
$ npm install express
```

NPM is a Node.js package manager, which acts as a registry for public packages (you can view the available public packages at https://npmjs.org/). NPM has two installation modes: local and global. Local mode installs the package to a node_modules folder inside the actual application, whilst the global mode installs the package globally on the system, thus making it available to any other Node.js application. The global mode will usually install the packages in the /usr/local/lib/node_modules folder for Unix-based systems and in the C:\Users\%USERNAME%\AppData\Roaming\npm\node_modules folder for Windows-based systems.

To install the package globally you have to add the -g flag to the npm install command, like this:
```
$ npm install -g <package_name>
```
2. Lets organize with package.json file

By putting a package.json file in the root of the application you get to define all the dependencies that your application needs, for example:
```
{
    "name" : "myMEANapplication",
    "version" : "1.0.0",
    "dependencies" : {
        "express" : "latest",
        "gulp" : "latest"
    }
}
```
and by issuing a simple
```
$ npm install
```

## IV.  AngularJS
AngularJS is a frontend JavaScript framework designed to build single-page applications using the MVC architecture. It's built and maintained by Google so this should give you a peace of mind. Few of the cool features are:

Two-way data binding, which synchronizes between models and views
Extended HTML with additional attributes, which bind the JavaScript objects with HTML elements
Improved code structure
Easier testing through dependency injection

In order to downlod AngularJS, you have to visit https://angularjs.org/ and upon clicking on the download button to download.

But, there is a better way to manage your frontend dependencies - with the tool called Bower. Bower is a package manager which makes it easier to download and maintain your frontend libraries. Since Bower is a Node.js module you can install it by executing: 
```
$> $ npm install -g bower
```

However, in order to use Bower, you will need to get [Git](http://en.wikipedia.org/wiki/Git(software)) (distributed version control system) by going to http://git-scm.com/ and download/install it on your machine (the installation is a simple Next, Next, Finished type of installation).

Once the Bower is installed you can use the following command to install Angular:
```
$> bower install angular
```

If you get error when connect to git server, run following command: 
```
$> git config --global url."https://".insteadOf git://
```