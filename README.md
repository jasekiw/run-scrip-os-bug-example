# run-script-os-bug-example


Steps to Reproduce:

1. npm i


You will get the following output:


```
$ npm i

> run-scrip-os-bug-example@1.0.0 prepare C:\projects\run-scrip-os-bug-example
> run-script-os

npm ERR! missing script: i:win32

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\Jason\AppData\Roaming\npm-cache\_logs\2019-09-06T16_19_16_431Z-debug.log
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! run-scrip-os-bug-example@1.0.0 prepare: `run-script-os`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the run-scrip-os-bug-example@1.0.0 prepare script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above

```

It is basing the npm script off of the install and not the prepare command that it was put under.


An easy fix for this would be to allow you to specify the script by using `run-escrip-os prepare` to allow the developer to 
control what command is ran.

