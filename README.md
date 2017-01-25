Description
-----------

This cookbook will install [Google Android SDK](http://developer.android.com/sdk/index.html).

The **default** recipe of this Chef cookbook will:

* Download and install/upgrade Android SDK (not ADT)
* Update SDK dependencies to install *some* Android platforms (`--filter` list can be customized in cookbook attributes)
* Define a default `ANDROID_HOME` environment variable
* Add `ANDROID_HOME/tools` and `ANDROID_HOME/platform-tools` to default `PATH` environment variable

Requirements
------------

* Depends on **ark**, **java**, **homebrew**, **chef-sugar**, **expect** and **bash** cookbooks
* This cookbook currently supports Ubuntu 12.04+ and CentOS 7+, Mac OS X, Windows

Attributes
----------

TODO (work in progress)

Installation and Usage
----------------------

This cookbook is released at https://supermarket.chef.io/cookbooks/android-sdk and its original git repository is https://github.com/gildegoma/chef-android-sdk.

* Find your favourite way ([Berkhelf](http://berkshelf.com/), [Librarian-Chef](https://github.com/applicationsonline/librarian#readme), knife-github-cookbooks, Git submodule, Opscode community API or even tarball download) to install this cookbook (and its dependency).
* Include the `android-sdk::default` recipe to your run list or inside your cookbook.
* Provision!

Quality Assurance
-----------------

### Continous Integration

This Cookbook is being _tested_ by Travis CI: [![Build Status](https://secure.travis-ci.org/gildegoma/chef-android-sdk.png?branch=master)](https://travis-ci.org/gildegoma/chef-android-sdk)

Automated validations are following:
  * Static Analysis of Ruby code with [tailor](https://github.com/turboladen/tailor#readme) lint tool
  * Static Analysis of Chef Cookbooks with [foodcritic](http://acrmp.github.com/foodcritic/) lint tool
  * `knife cookbook test` in a very basic sandbox
  * _PENDING:_ Expectations described with RSpec examples with [ChefSpec](https://github.com/acrmp/chefspec)
  * [ServerSpec](http://serverspec.org/) integration testing
  * Run true chef (matrix) on travis VM with ServerSpec test

### Development and Testing

During development, this cookbook is locally tested in following environments:
 * Development with *recent* versions of Chef-Solo and Ubuntu (with great help of Berkshelf, Vagrant and Virtualbox and other tools provided by the Chef community).
 * Integration with great help of Opscode [test-kitchen](https://github.com/opscode/test-kitchen)

License and Credits
-------------------

* Thanks to:: [All Contributors](https://github.com/gildegoma/chef-android-sdk/graphs/contributors)
* Thanks to:: [Ralf Kistner](https://github.com/rkistner), for all relevant information to create original cookbook
* Thanks to:: [Andrew Rosa](https://github.com/andrewhr), for all relevant information to improve this cookbook
* Thanks to:: [Travis CI Project](http://github.com/travis-ci/travis-cookbooks), for motivating the creation of this cookbook

* Copyright:: 2013-2014, Gilles Cornu

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
