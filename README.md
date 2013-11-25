# SPIDEY

[![Build Status](https://travis-ci.org/fabiocicerchia/spidey.png)](https://travis-ci.org/fabiocicerchia/spidey)
[![Dependency Status](https://gemnasium.com/fabiocicerchia/spidey.png)](https://gemnasium.com/fabiocicerchia/spidey)
[![Coverage Status](https://coveralls.io/repos/fabiocicerchia/spidey/badge.png)](https://coveralls.io/r/fabiocicerchia/spidey)

[![NPM](https://nodei.co/npm/spidey.png?downloads=true&stars=true)](https://nodei.co/npm/spidey/)

[![Spidey - Web Crawler in Node.js to spider dynamically whole websites.](http://jpillora.com/github-twitter-button/img/tweet.png)](https://twitter.com/intent/tweet?text=Spidey+-+Web+Crawler+in+Node.js+to+spider+dynamically+whole+websites.&url=https%3A%2F%2Fgithub.com%2Ffabiocicerchia%2Fspidey&hashtags=spidey&original_referer=http%3A%2F%2Fgithub.com%2F&tw_p=tweetbutton)

Web Crawler in Node.js to spider dynamically whole websites.

It helps you to map / process entire websites, spidering them and parsing each
page in a smart way. It follows all the links and test several times the form
objects. In this way is possible to check effectively the whole website.

Few suggestion about its usage:

 * Improve the legacy code
  * Check the dead code (enabling the code coverage server-side)
  * Discover 500 Internal Server Errors
  * Discover notices and warnings
 * Testing
  * Process forms (it'll create easy test cases to be manually compiled)
  * Process automatically JS events attached to DOM nodes
 * Scraping
  * Get the page content for each URL
  * Get the screenshot for each URL
 * Enumeration
  * URLs list
  * Execution times
  * Page output
  * Page load
 * ...

## Features

 * Command Line Interface
 * Reorder query string params for get and post for uniqueness
 * HTTP authentication
 * Handle events bound with `addEventListener`, HTML attributes (`on*`)
 * Exclude external URIs in the crawling
 * Process the page using PhantomJS
 * Generate report for each page crawled
  * Screenshot
  * HTTP header
  * HTTP method
  * Data sent
  * Page output
  * Execution time
  * Console messages
  * Alerts, Confirmations & Prompts
  * Errors
  * List of requests

## Dependencies

Here the list of main dependencies:

 * [Node.js](http://nodejs.org/download/)
 * [PhantomJS](http://phantomjs.org/download.html) / [CasperJS](http://casperjs.org/)
 * [Redis](http://redis.io/download)

## Installation

You can install it directly from npm:

```
[user@hostname ~]$ npm install spidey -g
```

or you can download the source code from GitHub and run these commands:

```
[user@hostname ~/spidey]$ npm install
```

## Configuration

Change the file `src/config.js` accordingly to your needs.

## Usage

```
              __     __
.-----.-----.|__|.--|  |.-----.--.--.
|__ --|  _  ||  ||  _  ||  -__|  |  |
|_____|   __||__||_____||_____|___  |
      |__|                    |_____|

SPIDEY v0.2.1

Copyright (C) 2013 Fabio Cicerchia <info@fabiocicerchia.it>

Web Crawler in Node.js to spider dynamically whole websites.
Usage: ./bin/spidey

Options:
  --uri              The URI to be crawled             [required]
  -u, --username     Username for HTTP authentication
  -p, --password     Password for HTTP authentication
  -d, --details      Store details for each page       [default: false]
  --help             Show the help
```

## Examples

```
[user@hostname ~]$ spidey --uri "http://www.google.com"
[user@hostname ~]$ spidey --uri "www.google.com"
[user@hostname ~]$ spidey --uri "/tmp/file.html"
[user@hostname ~]$ spidey --uri "file.html"
```

## Tests

```
[user@hostname ~/spidey]$ npm test
```

## Bugs

For a list of bugs please go to the [GitHub Issue Page](https://github.com/fabiocicerchia/spidey/issues?labels=Bug&page=1&state=open).

## Licence

Copyright (C) 2013 Fabio Cicerchia <info@fabiocicerchia.it>

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
