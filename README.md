# apparmor

**SaltaIT/eyp-apparmor**: [![Build Status](https://travis-ci.org/SaltaIT/eyp-apparmor.png?branch=master)](https://travis-ci.org/SaltaIT/eyp-apparmor)

#### Table of Contents

1. [Overview](#overview)
2. [Module Description](#module-description)
3. [Setup](#setup)
    * [What barman affects](#what-barman-affects)
    * [Setup requirements](#setup-requirements)
    * [Beginning with barman](#beginning-with-barman)
4. [Usage](#usage)
5. [Reference](#reference)
5. [Limitations](#limitations)
6. [Development](#development)
    * [Contributing](#contributing)

## Overview

Manages AppArmor

## Module Description

Allows you to enforce a global mode for AppArmor.

**Ubuntu**:
* complain
* enforce
* disable (default)

**SuSE**:
* complain (default)
* enforce

## Setup

### What apparmor affects

Installs apparmor-utils to be able to manage AppArmor

### Setup Requirements

This module requires pluginsync enabled

### Beginning with apparmor

```puppet
class { 'apparmor':
  mode => 'disable',
}
```

## Usage

Just a single class to set apparmor to disable, complain or enforce

## Reference

### classes

#### apparmor

* **mode**: disable, complain, enforce

## Limitations

Tested on:
* Ubuntu 14.04
* SLES 11 SP3

## Development

We are pushing to have acceptance testing in place, so any new feature should
have some test to check both presence and absence of any feature

### Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
