[![Build Status Badge](https://circleci.com/gh/mozilla/newtab-layouts.svg?style=svg)](https://app.circleci.com/pipelines/github/mozilla/newtab-layouts)

# Newtab Layouts

**Remote layouts microservice for Firefox Newtab**

## Running Locally

### Running for local development

Requirements: `node`

- `npm i`
- `cp example.env .env`
- `npm start`

## Configuring Firefox to use a local layout

- Open `about:conf`
- Edit Firefox preference `browser.newtabpage.activity-stream.discoverystream.config` and set keys `hardcoded_layout` to `false` and `layout_endpoint` to point to one of the layouts eg `http://localhost:1234/collection.json`
- Edit Firefox preference `browser.newtabpage.activity-stream.discoverystream.endpoints` to `http,https`
- Open a new tab (note: changes to a local layout will require editing `browser.newtabpage.activity-stream.discoverystream.config` to bust the previously cached layout. Adding or removing a space to the end of the JSON value will work.)
