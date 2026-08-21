initial code
check
git remote -v  
git config --global user.name
git config --global user.email 

add
git config --global user.name "username"
git config --global user.email "email" 
git remote add origin https://github.com/Shakana25/Test-React   

remove
git config --global --unset user.name
git config --global --unset user.email
git remote remove origin


echo "# Test-React" >> README.md
git init
git add README.md // git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Shakana25/Test-React.git
git push -u origin main

Generate token Manual Navigation
If you want to find it from your GitHub profile page:
Click your profile icon in the top-right corner of GitHub.
Click Settings.Scroll all the way down on the left sidebar to Developer Settings (at the very bottom).Click Personal access tokens, click Tokens (classic).
Click Generate new token, click Generate new token (classic).
Check the repo box, generate it, copy the code, and paste it into that window!

if a code is put into production need to bundle/ optimised/ minimised/compressed our code. (ex: remove comment/ consolelog)

create react app will create React project immidiately.
not only react there are some other package help us to make react code fast.
npm means node package manager, which manages the packages
npm is a standered repository for the all packages.
npm take care the version of all packages. 

now i want to get npm 
npm init 
or
npm init -y     ( this code ommit some step create project easily)


package name: (react-day2) 
version: (1.0.0) 
description: this is start of react project creation
entry point: (app.js) 
test command: jest
git repository: (https://github.com/Shakana25/Test-React.git) 
keywords: test, react, first
author: shakana
license: (ISC) 
type: (commonjs) 

package.json created: configuration for npm
get any packages from npm: start installing our dependency(package)

most importtant package is bundler(webpack/ vite/parcel):  bundle/ optimised/ minimised/compressed/clean our code & host the project

npm install -D parcel :- like this way we can install any dependency(package) from npm. 
 -D mean dev dependency, use for develepment phase.

if -D not mention then it's a Regular dependency

  "devDependencies": {
    "parcel": "^2.16.4"
  }

  ^ caret- parcel automatically update 2.16.5 - minor upgrade //safe
  ~ tilde- atomatically update major version- 3.1.1 // not safe- lot of things is break"
  "parcel": "2.16.4"- no upgrade, fix version

  parcel instalation created package-lock.json - keep the exact version of packages.

  "node_modules/@parcel/bundler-default": {
      "version": "2.16.4",
      "resolved": "https://registry.npmjs.org/@parcel/bundler-default/-/bundler-default-2.16.4.tgz",
      "integrity": "sha512-Nb8peNvhfm1+660CLwssWh4weY+Mv6vEGS6GPKqzJmTMw50udi0eS1YuWFzvmhSiu1KsYcUD37mqQ1LuIDtWoA==",
      "dev": true,
      "license": "MIT",
      "dependencies": {
        "@parcel/diagnostic": "2.16.4",
        "@parcel/graph": "3.6.4",
        "@parcel/plugin": "2.16.4",
        "@parcel/rust": "2.16.4",
        "@parcel/utils": "2.16.4",
        "nullthrows": "^1.1.1"
      },}
      integrity: sometimes developer's said it work on local, but break in production it bcz of version mismatch. this integrity keep exact version for development , production.

      and node modules also created when install parcel. package json, package-lock json contain only the version, node module like a database contain all the packages which installed - very heavy

      our project need parcel, parcel need some other dependency(packages)- this is call as transitive dependency. all this dependencies get inside node modules folder.

      how it know what are the dependency use in parcel? parcel package-lock json contain all the dependecies & versions which use in parcel.
      our project have 1 package json,1 package-lock json, similarly each and every transitive packages have their unique package, package-lock.

      go to the projected created folder, check the size of node module, it is huge.
      we can't put this huge node module folder into git hub/ production. 
      and the nodemodule folder can be regenerate when you have package.json, package-lock.json by running code npm install.
      so we don't add node-modules in the github and have to add package, package-lock.json in git.
      so we will create git ignore file and add /node_modules.
      what ever files we can re generate, which are not to add in git.

      Source control: provide the exact count of files you have changed and are ready to upload to GitHub.
      check source control files count before and after ignore node_modules.

      npx parcel index.html : can run in local host: our file hosted on server:
      parcel give server. parcel host our app in the server.

      npm- packege manage
      npx- execute package

      another way get react into our app using npm.

----------------------------------by me--------------------------------------------------------------------------
      npm install react
      npm install react-dom
      
-----------------------------------------------------------------------------------------------------------------# IT3133_practical