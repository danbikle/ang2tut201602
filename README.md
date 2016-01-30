hello world

The purpose of this repo is to help me walk through the Angular2 tutorial which is listed here:

https://angular.io/docs/ts/latest/quickstart.html

I prefer to use Ubuntu 14.04 because it runs on both my laptop and on Amazon.

I start by installing Ubuntu 14.04 on my laptop.

The most recent version of Ubuntu which I like is at this URL:

http://releases.ubuntu.com/14.04.3/ubuntu-14.04.3-desktop-amd64.iso

The three general paths to install Ubuntu on a laptop are listed below:

- Remove Windows and install Ubuntu
- Ignore Windows and install Ubuntu on USB drive
- Install VirtualBox on Mac or Windows, Install Ubuntu inside VirtualBox

My favorite path is path2: Ignore Windows and install Ubuntu on USB drive.

Path2 works well with a new laptop should I want to maintain the warranty.

If you are new to the world of Ubuntu laptops I suggest you buy a cheap windows laptop from Walmart and run some experiments.

E-me if you need help: bikle101@gmail.com

When I install Ubuntu, it will ask who I am.

I tell Ubuntu that my name is ann.

Then, Ubuntu will create an account named ann which has useful privileges.

If you use a different initial account, you should create an account named ann after you boot the laptop.

The shell commands to create the ann account are listed below:
```bash
sudo useradd -m -s /bin/bash ann
sudo passwd ann
```

The first command creates ann.
The second command gives her a password.

After I create the ann account, I enhance and update Ubuntu.

The shell commands to do this are listed below:

```bash
sudo apt-get update
sudo apt-get upgrade

sudo apt-get install autoconf bison build-essential libssl-dev libyaml-dev \
libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm3       \
libgdbm-dev libsqlite3-dev gitk postgresql postgresql-server-dev-all  \
libpq-dev emacs wget curl chromium-browser openssh-server aptitude    \
ruby ruby-dev sqlite3

sudo apt-get update
sudo apt-get upgrade
```

After that I login as ann and I download Node.js.

wget https://nodejs.org/dist/v5.5.0/node-v5.5.0-linux-x64.tar.gz

Then I install it:
```bash
rm -rf  node
tar zxf node-v5.5.0-linux-x64.tar.gz
mv      node-v5.5.0-linux-x64 node
```

So, I did that on my laptop.

Then I did this:
```bash
cd ~ann
git clone ang2tut201602
cd        ang2tut201602
npm install
npm start
```

The console indicated that lite-server was serving at two URLs:

http://localhost:3000

http://localhost:3001

The first URL corresponded to my Angular2 app.

The second URL corresponded to an admin-UI for lite-server.

I saw this:
```bash
ann@nia111:~/ang2tut201602 $ 
ann@nia111:~/ang2tut201602 $ npm start

> angular2-quickstart@1.0.0 start /home/ann/ang2tut201602
> concurrent "npm run tsc:w" "npm run lite" 

[1] 
[1] > angular2-quickstart@1.0.0 lite /home/ann/ang2tut201602
[1] > lite-server
[1] 
[0] 
[0] > angular2-quickstart@1.0.0 tsc:w /home/ann/ang2tut201602
[0] > tsc -w
[0] 
[1] [BS] Access URLs:
[1]  ----------------------------------
[1]        Local: http://localhost:3000
[1]     External: http://10.0.2.15:3000
[1]  ----------------------------------
[1]           UI: http://localhost:3001
[1]  UI External: http://10.0.2.15:3001
[1]  ----------------------------------
[1] [BS] Serving files from: ./
[1] [BS] Watching files...
[0] 11:35:50 AM - Compilation complete. Watching for file changes.
[1] [BS] File changed: app/app.component.js
[1] [BS] File changed: app/boot.js
[1] 16.01.29 11:35:50 304 GET /./index.html (Unknown - 32ms)
[1] 16.01.29 11:35:51 404 GET /favicon.ico (Unknown - 234ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/angular2/bundles/angular2.dev.js (Unknown - 19ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/es6-shim/es6-shim.min.js (Unknown - 18ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/systemjs/dist/system-polyfills.js (Unknown - 19ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/angular2/bundles/angular2-polyfills.js (Unknown - 19ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/systemjs/dist/system.src.js (Unknown - 18ms)
[1] 16.01.29 11:35:51 304 GET /node_modules/rxjs/bundles/Rx.js (Unknown - 18ms)
[1] 16.01.29 11:35:52 200 GET /app/boot.js (Unknown - 89ms)
[1] 16.01.29 11:35:53 200 GET /app/app.component.js (Unknown - 330ms)
```

Also it brought up a browser and displayed the h1-element I had typed into app/app.component.ts.

And I noticed that it created some new files in my git repo:
```bash
app/app.component.js
app/app.component.js.map
app/boot.js
app/boot.js.map
```

The way I got started with Angular2 development is to memorize a set of words which I see in the tutorial.

This is a boring way to learn development but I need to know how to describe the internals of my Angular2 apps when I work with other people.

This is similar to learning a foreign language like French.

I need to start by memorizing some words.

For Angualar2, the words I need to memorize are listed below in alphabetical order:

* at-sign
* Apache Cordova
* CSS selector
* ES5
* ES6
* NativeScript
* RxJS 
* System
* System.config
* System.import
* SystemJS
* angular2/core
* angular2/platform/browser
* app
* boot.ts
* bootstrap
* class
* companion template
* component
* component metadata
* concurrent
* configuration object
* decorator
* dependencies
* devDependencies
* export
* file
* import
* index.html
* internet explorer polyfills
* lite-server
* module
* my-app
* noImplicitAny
* node_modules
* npm
* npm install
* npm package
* npm package manager 
* package.json
* platform-specific
* plunker
* pre-compilation
* project folder
* promise
* reactive extensions
* root component
* routing
* scripts section
* selector
* Separation of concerns
* system.src.js
* template
* template property
* transpile
* tsconfig.json
* typescript
* typescript compiler
* view
* view template
* webpack

My memorization strategy is simple.

First I form questions from the word.

Next, I will try building sentences from the word.

Then, I build some code snippets which are related to the word.

For example the first word is:

at-sign

I thought up four questions related to at-sign:

* Can I ignore at-sign or should I know about it?
* Where in the tutorial is at-sign?
* What should I call the at-sign?
* Why should I use the at-sign?

Next, I thought up some sentences related to at-sign:
* I see the at-sign in the tutorial when they describe how to write app.component.ts.
* The at-sign looks important; I should know about it.
* I should remember the at-sign as, "Some TypeScript syntax which helps me apply a function to a class as a decorator."
* This syntax is discussed at this URL:
* https://angular.io/docs/ts/latest/quickstart.html#component-metadata
* I use the at-sign to help me tell Angular that a class is an 'Angular Component'.
* The at-sign can be placed in front of a function named 'Component' which has been imported from angular2/core.
* Once I do that, I can call ```@Component()``` with some metadata as a parameter to create an 'Angular Component'.
* This metadata is a simple JS-object which contains a CSS-selector and a thing called a template which I see as some HTML-syntax.

Here is a code snippet related to the at-sign:
```javascript
import {Component} from 'angular2/core';
@Component({
    selector: 'my-app',
    template: '<h1>My First Angular 2 App</h1>'
})
```

So, I just demostrated how I route-memorize the idea behind the Angular2 at-sign:

* 4 Questions
* Some sentences
* A  code snippet

In the list above I see 77 words I want to memorize.

It would take me a long time to memorize them using my question-sentence-snippet technique.

But those memorized ideas should become useful as I start writing more Angular2 code.

