json-yaml
=========

`./json-yaml -h`

    Usage: json-yaml [OPTIONS] [FILE]
    
    Convert JSON into YAML
    Uses standard input if no filename is supplied.
    
    Options:
    -v, --version   print version number and exit
    -h, --help      print this message and exit


Examples
--------

`./json-yaml sample.json`

    firstName: John
    lastName: Smith
    isAlive: true
    age: 25
    address:
      streetAddress: 21 2nd Street
      city: New York
      state: NY
      postalCode: 10021-3100
    phoneNumbers:
    - type: home
      number: 212 555-1234
    - type: office
      number: 646 555-4567
    - type: mobile
      number: 123 456-7890
    children: []
    spouse: null

`curl -s http://api.icndb.com/jokes/random | ./json-yaml`

    type: success
    value:
      id: 415
      joke: When Chuck Norris wants an egg, he cracks open a chicken.
      categories: []


Installing
----------

On OS X, you can use [Homebrew](http://brew.sh):

    brew tap yokattana/tap
    brew install json-yaml

For other platforms, consult the _Building_ section below.


Building
--------

You need [libyaml](http://pyyaml.org/wiki/LibYAML) and [yajl](yajl). Then:

`make`

Other targets:

    make check
    make install
    make uninstall

See Makefile for variables.


Links
-----

Home page:
https://github.com/yokattana/json-yaml

Builds:
https://travis-ci.org/yokattana/json-yaml/

[![Build Status](https://travis-ci.org/yokattana/json-yaml.svg?branch=master)](https://travis-ci.org/yokattana/json-yaml)


Authors
-------

 * By iku@yokattana.com, 2016.
