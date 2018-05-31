[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/standard/standard)

# What's This?

This Project contains 'boilerplate' open source code which can be customised to create command line applications which interact with the SAFE Network. It uses [pkg](http://npmjs.com/package/pkg) to create packaged executables for Linux, Windows and Mac OS.

The [SAFE Network](https://safenetwork.org/) is a truly autonomous, decentralised internet. A new basis for an open internet aligned with the original vision held by its creators and early users, with security, net neutrality and unmediated open access, all baked in. The Secure Access For Everyone (SAFE) Network tackles the increasing risks to individuals, business and nation states arising from over centralisation, domination by commercial monopolies, security risks from malware, hacking, surveillance and so on.

# Get the source
If you are not yet familiar with developing for SAFE Network, or have not previously used the 'mock' SAFE Browser to develop and test your code, I recommend that you try the [SAFE Network Nodejs](https://hub.safedev.org/platform/nodejs/) Tutorial *before* proceeding. Doing so will ensure you have all the pre-requisites and help you understand anything not made explicit in the instructions below.

Clone this repository into safe-cli-boilerplate:
```
git clone https://github.com/theWebalyst/safe-cli-boilerplate
cd safe-cli-boilerplate
```

# Build for mock network

Install the dependencies:
```
export NODE_ENV=dev
npm install
```

Build an executable for the host OS only, the default (output in ./dist/mock):
```
export NODE_ENV=dev
npm run build-mock
```
For Linux, Mac and Windows targets:
```
export NODE_ENV=dev
npm run buildall-mock
```
## To test with mock
Start the SAFE Browser in another terminal with:
```
export NODE_ENV=dev
safe-browser
```
In the browser, create an account on the mock network.

In your development terminal, in your build directory type:
```
export NODE_ENV=dev
./dist/mock/safecmd
```
You should see output to the terminal generated by the example code in `cli.js` which lists the directory contents, similar to the following:
```
.gitignore - 992 B
LICENSE - 34.32 KB
README.md - 96 B
cli.js - 3.59 KB
dist - 4 KB
example.example.log - 4 B
node_modules - 4 KB
package-lock.json - 57.46 KB
package.json - 1010 B
safe-app-cli.js - 3.38 KB
yarn-error.log - 39.76 KB
```
The SAFE Browser window should then activate and ask you to authorise the example app. If you click `Allow` the app will continue and print more output to the console before exiting, as follows:
```
Quick Setup Completed
New file is created and saved to the network successfully
The file has been opened and read
The content of the file which has been read: Hello Safe World
```

# Build for live network

Install the dependencies:
```
export NODE_ENV=
npm install
```

Build an executable for the host OS only, the default (output in ./dist/prod):
```
export NODE_ENV=
npm run build
```
For Linux, Mac and Windows targets:
```
export NODE_ENV=
npm run buildall
```

# Problems?
Before requesting help here, please follow the [SAFE Network Nodejs Tutorial](https://hub.safedev.org/platform/nodejs/) and ensure you are able to build a desktop app. That should ensure you have all the pre-requisites, and help you to understood how to test using a **mock** SAFE Network.

# Contributions
Pull requests are welcome for outstanding issues and feature requests. Please note that contributions must be subject to the Project License (see below), and that if an incompatible license is present in your contribution it will be rejected.

**IMPORTANT:** By submitting a pull request, you will be offering code under either the Project License or a license that is compatible with and does not restrict the Project License of any existing files in the Project, or of any code in the Project that is substantially similar to your contribution. If your submission is not compatible with the Project License, the license specified below (under 'License') will apply to your submission by default.

Before submitting your code please consider using `Standard.js` formatting. You may also find it helps to use an editor with support for Standard.js when developing and testing. An easy way is just to use [Atom IDE](https://atom.io/packages/atom-ide-ui) with the package [ide-standardjs] (and optionally [standard-formatter](https://atom.io/packages/standard-formatter)). Or you can install NodeJS [Standard.js](https://standardjs.com/).

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/standard/standard)

# Project License
This project is made available under the [GPL-3.0 LICENSE](https://opensource.org/licenses/GPL-3.0) except for individual files which contain their own license so long as that file license is compatible with GPL-3.0. 

The responsibility for checking this licensing is valid and that your use of this code complies lies with any person and organisation making any use of it.
