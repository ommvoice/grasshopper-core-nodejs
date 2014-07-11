![Grasshopper Logo](https://s3.amazonaws.com/SolidInteractive/images/grasshopper/grasshopper-core.jpg)

---------------------------------------------------------------

[![NPM](https://nodei.co/npm/grasshopper-core.png)](https://nodei.co/npm/grasshopper-core/)

[![Build Status](https://travis-ci.org/Solid-Interactive/grasshopper-core-nodejs.png?branch=master)](https://travis-ci.org/Solid-Interactive/grasshopper-core-nodejs)


### What am I?

------------------------------------------------------------------

Grasshopper is a Data Management System (DMS). A DMS is a layer that sits on top of a database that makes working with the data easier for both administrators and developers. Grasshopper knows about data, schemas, data organization and permissions/roles. Since these concepts are core to grasshopper you will not have to figure them out for each of your applications.

Standardizing data management is very important if you are developing a lot of applications. The grasshopper project is a NodeJS library that can be used as part of your solution.

The most common implementation of grasshopper includes the admin project (dynamic UI that manages grasshopper data) and grasshopper-api (HTTP wrapper for core). If you are building a NodeJS project then grasshopper-core could be used natively in your application as well.


[GRASSHOPPER API](https://github.com/Solid-Interactive/grasshopper-api-js)

[GRASSHOPPER ADMIN](https://github.com/Solid-Interactive/grasshopper-admin)



### Core concepts

------------------------------------------------------------------

*Users* - most applications need the concept of users, grasshopper provides a standard way to create and extend user data. It also supports roles and node based permissions.

*Content Types* - or virtual schemas, since you are most likely using a NoSQL database you are not bound to any specific schema. Most applications still require data to be predictable so grasshopper allows the developer to create virtual schemas to accomplish data consistency.

*Nodes* - or directories, nodes can be created to organize content into buckets of your choosing.

*Content* - or an implementation of a content type. Many types of content make up an application.


### How would you use me?

------------------------------------------------------------------

Install
```
npm install grasshopper-core --save
```


Usage

```
var grasshopper = require('grasshopper-core');

grasshopper.configure(function(){
    this.config = {
        'crypto': {
            'secret_passphrase' : '{UNIQUE PASSPHRASE}'
        },
        'db': {
            'type': 'mongodb',
            'host': 'mongodb://localhost:27017/{YOUR DB}',
            'database': '{YOUR DB}',
            'username': '{YOUR USERNAME}',
            'password': '{YOUR PASSWORD}',
            'debug': false
        },
        'assets': {
            'default' : 'local',
            'tmpdir' : '/absolute path to temp directory',
            'engines': {
                'local' : {
                    'path' : '/absolute path to public directory',
                    'urlbase' : 'http://YOUR URL'
                }
            }
        },
        'identities' : {
            'google' : {
                'appId' : 'blahBlahBlackSheep',
                'secret' : 'ohhSooSecret',
                'redirectUrl' : '/this/that',
                'scopes' : [
                    'https://www.googleapis.com/auth/userinfo.profile',
                    'https://www.googleapis.com/auth/userinfo.email'
                ],
                'tokenEndpoint' : 'https://www.googleapis.com/oauth2/v1/userinfo?alt=json&access_token=',
                'oauthCallback' : 'http://localhost:3000/oauth2callback'
            }
        }
    };
```



### Running Tests

-------------------------------------------------------

* $: ```grunt test```


### Upcoming Features

-------------------------------------------------------

* Node based permissions
* Hooks are not yet supported
* Full node permissions for search criteria
* Cascading permissions for child nodes
* Deleting content when deleting a content type
* Registering new collections
* Security enhancements
* Publish content to other environments
* Content localization
* Content history
* Document merges
* Dynamic content model validation
* Plug in custom roles for advanced proxy implementations
* Document concurrency protection
* 3rd party authentication schemes
* more more more


## License

-------------------------------------------------------

Grasshopper CORE JS is released under a [MIT license](https://github.com/Solid-Interactive/grasshopper-core-nodejs/blob/master/LICENSE).

## Release Notes

* 0.1.6 - 2014-03-30 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.1.6_2014-03-30.md)
* 0.1.7 - 2014-03-29 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.1.7_2014-03-29.md)
* 0.1.9 - 2014-04-01 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.1.9_2014-04-01.md)
* 0.1.10 - 2014-04-01 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.1.10_2014-04-01.md)
* 0.1.11 - 2014-04-02 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.1.11_2014-04-02.md)
* 0.2.0 - 2014-04-02 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.2.0_2014-04-02.md)
* 0.2.3 - 2014-04-08 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.2.3_2014-04-08.md)
* 0.2.4 - 2014-04-10 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.2.4_2014-04-10.md)
* 0.3.1 - 2014-04-10 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.3.1_2014-04-10.md)
* 0.4.1 - 2014-04-11 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.1_2014-04-11.md)
* 0.4.2 - 2014-04-11 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.2_2014-04-11.md)
* 0.4.3 - 2014-04-14 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.3_2014-04-14.md)
* 0.4.4 - 2014-04-14 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.4_2014-04-14.md)
* 0.4.5 - 2014-04-15 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.5_2014-04-15.md)
* 0.4.6 - 2014-04-16 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.6_2014-04-16.md)
* 0.4.7 - 2014-04-17 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.7_2014-04-17.md)
* 0.4.8 - 2014-04-30 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.8_2014-04-30.md)
* 0.4.9 - 2014-04-21 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.9_2014-04-21.md)
* 0.4.10 - 2014-04-21 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.10_2014-04-21.md)
* 0.4.11 - 2014-04-21 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.11_2014-04-21.md)
* 0.4.12 - 2014-04-22 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.12_2014-04-22.md)
* 0.4.13 - 2014-04-23 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.4.13_2014-04-23.md)
* 0.11.18 - 2014-04-23 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.11.18_2014-04-23.md)
* 0.12.0 - 2014-06-11 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.12.0_2014-06-11.md)
* 0.12.1 - 2014-06-11 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.12.1_2014-06-11.md)
* 0.12.2 - 2014-06-11 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.12.2_2014-06-11.md)
* 0.13.0 - 2014-06-24 - [features](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.13.0_2014-06-24.md)
* 0.13.1 - 2014-06-24 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.13.1_2014-06-24.md)
* 0.13.2 - 2014-06-25 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.13.2_2014-06-25.md)
* 0.13.3 - 2014-06-26 - [patches](https://github.com/Solid-Interactive/grasshopper-core-nodejs/tree/master/release_notes/0.13.3_2014-06-26.md)


## Contributors (`git shortlog -s -n`)

* Travis McHattie
* Peter Ajtai
* Greg Larrenaga
* Eric Beringer


## Dev Notes

To create the readme, update the release notes dir and package.json.version at a minimum. If needed update README.template.md.
Then run `grunt readme`.

_Compiled file. Do not modify directly. Created: 2014-06-26 02:32:41_