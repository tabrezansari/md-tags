# md-tags

[![NPM version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]
[![Coveralls Status][coveralls-image]][coveralls-url]
[![Dependency Status][depstat-image]][depstat-url]
[![DevDependency Status][depstat-dev-image]][depstat-dev-url]

> Extract tags from your markdown article

## Install

    npm install --save md-tags

## Usage

```js
import mdTags from 'md-tags';

const post = `
# Title

_January 30, 2016_

#nodejs, #markdown, #my-tag`;

const tags = mdTags(post);
tags.text;    // nodejs, markdown, my-tag
tags.list;    // ["nodejs", "markdown", "my-tag"]

```

## API

### tagsForPost(post)

Return object `{text:String, list: Array}`.

#### post

*Required*  
Type: `String`

Markdown string.

### postsForTag(tag, posts)

Return `list: Array` array of posts in markdown syntax, which matches by tag.

#### tag

*Required*  
Type: `String`

Tag for searching in posts.

#### posts

*Required*  
Type: `Array`

Array of posts in markdown syntax

## License

MIT © [Aleksandr Filatov](https://alfilatov.com/)

[npm-url]: https://npmjs.org/package/md-tags
[npm-image]: https://img.shields.io/npm/v/md-tags.svg?style=flat-square

[travis-url]: https://travis-ci.org/greybax/md-tags
[travis-image]: https://img.shields.io/travis/greybax/md-tags/master.svg?style=flat-square

[coveralls-url]: https://coveralls.io/r/greybax/md-tags
[coveralls-image]: https://img.shields.io/coveralls/greybax/md-tags/master.svg?style=flat-square

[depstat-url]: https://david-dm.org/greybax/md-tags
[depstat-image]: https://david-dm.org/greybax/md-tags.svg?style=flat-square

[depstat-dev-url]: https://david-dm.org/greybax/md-tags
[depstat-dev-image]: https://david-dm.org/greybax/md-tags/dev-status.svg