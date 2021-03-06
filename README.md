# procyclingstats-scraping
A script to scrap data from UCI cycling teams in Procycling Stats.

Disclaimer: I use the scraped data for teaching purposes only.

## Table of contents

<!-- toc -->

- [Usage](#usage)
- [Dependencies](#dependencies)
- [Webgraphy](#webgraphy)
- [TODO](#todo)

<!-- tocstop -->

## Usage
```bash
# Scrap Images and data from teams, from 4th to 9th team, current season
npm run scrap true true 3 9 
```

```bash
# Scrap Images and data from all teams of season 2005
npm run scrap true true 0 99 2005
```

## Dependencies
```bash
npm i
```

## Webgraphy
 * https://www.donnywals.com/build-a-simple-web-scraper-with-node-js/
 * https://www.freecodecamp.org/news/the-ultimate-guide-to-web-scraping-with-node-js-daa2027dcd3/
 * Howto download images, https://stackoverflow.com/questions/12740659/downloading-images-with-node-js
 * https://stackoverflow.com/questions/42706584/eslint-error-parsing-error-the-keyword-const-is-reserved

## TODO
> BUGS
- [ ] Have a look at argv capture to see how to use it for configuration
- [x] Debug errors in promises (when all data is required in a single execution) --> SOLVED: avoid sending all requests simultaneously
- [x] Normalize names of properties and variables (English)

> UPGRADE:
- [ ] Capture the image of the cyclist in the rider's page instead of team's page (because now it's downloading all the images of the team every time!)
- [ ] Change `Promise.all` by a method that executes the promises with a random delay, to avoid being detected/blocked by the server
- [ ] [Tor request](https://www.npmjs.com/package/tor-request) to avoid being detected
- [ ] Now is making a request for all team ids everytime it looks for info for 1 team only in `index.js`. Should make the team ids requests only once
- [ ] Create & Publish package: add bin.js, directory structure, SOLID principles, etc. + `babel-node`, etc.
- [ ] Parse dates using https://www.npmjs.com/package/date-and-time
- [x] Created an `/api` route to get json from files inside `_output` directory.
- [x] Set _delays_ between promises to avoid massive sending of simultaneous async Requests 
- [x] Added a property `image:` with the name of image file
- [x] Add `season` to get cyclists for every year
- [x] Separate `cheerio` functions in separated folders
- [ ] Change default parameter 99 to say that we want maximum number of cyclists

> REFACTORING:
- [x] Linting
- [ ] Automate Tests
- [ ] Include exceptions in file functions
- [ ] Use `path` module to standarize paths
- [ ] Const `CYCLISTS_PER_TEAM` should go in configuration file of options (like in json-server code)

> DONE:
- [x] Added a self-invoking function to avoid creating variables in Global object and interferences with local vars
- [x] Bug: linia 77, no agafa els elements img
- [x] File functions should be in separated file
- [x] toc generator (markdown-toc package)
