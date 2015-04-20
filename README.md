# lunr Index Builder with optional progressbar

A simple command line tool for building lunr indexes.

## Installation

    npm install lunr-index-build-silent

## Usage

    Generates a lunr.js index.

      lunr-index-build-silent -r id -f title:10 -f body < data.json > index.json

    Options:
      -f,  Specify a field to index                               [required]
      -r,  Specify the field that will be the document reference
      --with-progressbar : with progressbar

`lunr-index-builder-silent` reads your data from stdin and outputs a built index on stdout. You need to specify some fields to index from your input data and, optionally the ref for the documents. These options map directly to those of [lunr.js](http://lunrjs.com) itself so see that documentation for more details.

The input is expected to be valid JSON, with an array of document objects, e.g

    [{
        "id": 1,
        "title": "Foo"
    },{
        "id": 2,
        "title": "Bar"
    }]

### Example

    $ lunr-generator-silent -f title:10 -f tags:100 -f body -r id < data.json > index.json



