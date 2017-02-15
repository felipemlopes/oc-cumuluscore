<p align="center"><img src="http://init.biz/storage/app/media/publiczne/cumulus.png"></p>

# Cumulus plugin
- [Introduction](#introduction)
- [Features](#features)
- [How-to (guards)](#howto)
  - [Modules](#modules)
- [Future plans](#futureplans)

<a name="introduction"></a>
## Introduction
The plugin is a skeleton for building B2B SaaS applications using OctoberCMS.

Its main purpose is to ease companies (developers) creating modules and manage permissions to frontend pages.

The plugin requires `RainLab.UserPlus` and extends its features.

The name origins from puffy clouds as it is used to build applications in cloud environments.

Cumulus needs community and contributors, so go ahead and share your ideas.

<a name="features"></a>
## Features
TODO

<a name="howto"></a>
## How-to (frontend components)
Working with pages in Cumulus is based on three levels of testing user privileges.
1. User is logged in
1. User can access to company's page
1. Company has access to the module

The most useful solution is to create two layouts:
* one with session component from `RainLab.UserPlus`
* second with session component and `CumulusGuard` component

Third, 4th and so on with a module guards.

<a name="modules"></a>
### Modules
In Cumulus all is about modules. Cumulus core provides managing privileges, companies and users while modules provide functionality. Modules are normal OctoberCMS plugins but have some things that helps communicating with Cumulus Core.

After installing Cumulus Core you can run command:

```php artisan cumulus:createmodule <namespace>.<modulename>```

For example:

```php artisan cumulus:createmodule InitBiz.CumulusContractors```

After creating such module (witch basically is OctoberCMS plugin), you will have to run

```php artisan plugin:refresh <namespace>.<modulename>```

in order to register module in Cumulus Core.

<a name="futureplans"></a>
## Future plans
It is still experimental plugin but we hope it has potential. We decided to publish the code in order to help OctoberCMS team with fixing a bug discovered while developing Cumulus.

The most important future plans:
* Complete this documentation (some features are not described here)
* Building menu is not beautiful but we have an idea how to make it better :)
* Provide example module that will help understand workflow with Cumulus
* Provide theme in marketplace that will singleclick-install whole base environment with example module and Cumulus Core ready to create new modules
