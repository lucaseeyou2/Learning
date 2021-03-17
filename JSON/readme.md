# JSON
JSON is the acronym for *JavaScript Object Notation*. JSON files are used in many languages such as C++, Javascript, and Java. These types of files can store data under many forms (strings, arrays, numbers etc). Data can be added, removed or retrieved by different methods depending on what language you use. JSON files use the file extension of `.json` or their alternative `.jsonc` which is a bit different. `.jsonc` is not so different to JSON because both are same, but `.json` doesn't support comments and `.jsonc` does. Here is a basic template for a JSON file : 
```json
{
    "name": "value", 
    "number" : 1234,
    "bolean": true,
    "array": [
    "abc", 
    123, 
    true
    ], 
    "other_things": null
}
```
Here you can see multiple values being stored. Arrays, strings, boleans and other values can be stored here. To retrieve this data, see in the languages, to get the specific syntax for the language that you are searching for. Now we are going to explain the others features of JSON. First, different arrays types in JSON. Here is a demonstration of this array : 
```json
{
"something":{
    "html_element":{
        "id": "someelement", 
        "class": "", 
        "name": "p"
    }
}
}
```
These arrays are different from the normal arrays, they have a different notation but are the same, technicaly. These are only slightly different arrays, one with the brackets are the normal arrays, and the ones with the square brackets are classified as objects. Let's dive a bit deeper now. Let's start by the `$schema` and `$id`. These are some JSON values that can be important because they define how the JSON file shall be written. They are not normal propreties due to the dollar signs starting them with. Here is a standard JSON document containing one of these values : 

```json 
{
    "$schema": "http://json-schema.org/schema", 
    "$id": "1"
}
```
###### *You can learn more about this here : https://json-schema.org/learn/getting-started-step-by-step*;

## Special files
JSON have some special files, they named `package.json` or `package-lock.json`. These files are relative to npm, and are used to describe a node package. Let's start with the first file, named `package.json`. `package.json` is created when using the npm command `npm init` which initialises the creation of a new node package . You are obligated to only fill the name of your package and also the version of that one. Here is the process of creating a `package.json` file : 

```node
npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: project
version: (1.0.0)
description:
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
About to write to (dir*):

{
  "name": "project",
  "version": "1.0.0",
  "description": "",
  "main": "index",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes)
```
###### here dir* represents the directory that the file will be created at. 
You can see here that the command line asks you question that you can fill. If no value was provided, the command line will take the default value (inside the parethesis) and set it into your `package.json` file. To accept a value on the command line, press the `ENTER` key to accept that value. As you can see here, it has a name (name of the project), a version (the version that you are operating with), a description (the description of your project) an entry point and others. This is used to get more information for your package and can serve a lot. Now lets move on with `package-lock.json`. This file is used to track the changes made to the `node_module` tree (your node.js dependancies) or to `package-lock.json`. Here is an example of how `package-lock.json` looks like and can be changed : 

So here I will install EJS :
```
npm install ejs

+ ejs@3.1.6
added 15 packages from 8 contributors and audited 15 packages in 1.28s
found 0 vulnerabilities
```

Then `package-lock.json` was create inside there were dependancies here some of them 
```jsonc
{
  "name": "project",
  "version": "1.0.0",
  "lockfileVersion": 1,
  "requires": true,
  "dependencies": {
    "ansi-styles": {
      "version": "3.2.1",
      "resolved": "https://registry.npmjs.org/ansi-styles/-/ansi-styles-3.2.1.tgz",
      "integrity": "sha512-VT0ZI6kZRdTh8YyJw3SMbYm/u+NqfsAxEpWO0Pf9sq8/e94WxxOpPKx9FR1FlyCtOVDNOQ+8ntlqFxiRc+r5qA==",
      "requires": {
        "color-convert": "^1.9.0"
      }
    },
    "async": {
      "version": "0.9.2",
      "resolved": "https://registry.npmjs.org/async/-/async-0.9.2.tgz",
      "integrity": "sha1-rqdNXmHB+JlhO/ZL2mbUx48v0X0="
    },
    "balanced-match": {
      "version": "1.0.0",
      "resolved": "https://registry.npmjs.org/balanced-match/-/balanced-match-1.0.0.tgz",
      "integrity": "sha1-ibTRmasr7kneFk6gK4nORi1xt2c="
    },

    // other dependancies 

  }
```
###### *Sources : https://docs.npmjs.com/cli/v7/configuring-npm/package-lock-json & https://docs.npmjs.com/cli/v7/configuring-npm/package-json*
