# api documentation for  [unfluff (v1.1.0)](https://github.com/ageitgey/node-unfluff)  [![npm package](https://img.shields.io/npm/v/npmdoc-unfluff.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-unfluff) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-unfluff.svg)](https://travis-ci.org/npmdoc/node-npmdoc-unfluff)
#### A web page content extractor

[![NPM](https://nodei.co/npm/unfluff.png?downloads=true)](https://www.npmjs.com/package/unfluff)

[![apidoc](https://npmdoc.github.io/node-npmdoc-unfluff/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-unfluff_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-unfluff/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-unfluff/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-unfluff/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Adam Geitgey",
        "email": "ageitgey@gmail.com"
    },
    "bin": {
        "unfluff": "bin/unfluff"
    },
    "bugs": {
        "url": "https://github.com/ageitgey/node-unfluff/issues"
    },
    "dependencies": {
        "cheerio": "~0.17.0",
        "lodash": "~2.4.1",
        "optimist": "~0.6.1",
        "xregexp": "~2.0.0"
    },
    "description": "A web page content extractor",
    "devDependencies": {
        "coffee-script-redux": "2.0.0-beta7",
        "commonjs-everywhere": "0.9.x",
        "deep-equal": "~0.2.1",
        "mocha": "~1.12.1",
        "scopedfs": "~0.1.0",
        "semver": "~2.1.0"
    },
    "directories": {
        "bin": "bin",
        "lib": "lib",
        "test": "test"
    },
    "dist": {
        "shasum": "5f0c1aaf8ef103836c6468113eb716ff59c0b4bb",
        "tarball": "https://registry.npmjs.org/unfluff/-/unfluff-1.1.0.tgz"
    },
    "engines": {
        "node": "0.8.x || 0.9.x || 0.10.x"
    },
    "gitHead": "e757cda5c7f490d0f245d829bd1a58b4fefcb0b1",
    "homepage": "https://github.com/ageitgey/node-unfluff",
    "keywords": [
        "content extraction",
        "html",
        "scraping",
        "scrape",
        "web page",
        "body text"
    ],
    "licenses": [
        {
            "type": "Apache",
            "url": "https://github.com/ageitgey/node-unfluff/blob/master/LICENSE"
        }
    ],
    "main": "lib/unfluff.js",
    "maintainers": [
        {
            "name": "ageitgey",
            "email": "ageitgey@gmail.com"
        }
    ],
    "name": "unfluff",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/ageitgey/node-unfluff.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "1.1.0",
    "warnings": [
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.8.x || 0.9.x || 0.10.x"
            },
            "pkgid": "unfluff@1.1.0"
        },
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.8.x || 0.9.x || 0.10.x"
            },
            "pkgid": "unfluff@1.1.0"
        }
    ]
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module unfluff](#apidoc.module.unfluff)
1.  [function <span class="apidocSignatureSpan">unfluff.</span>lazy (html, language)](#apidoc.element.unfluff.lazy)
1.  object <span class="apidocSignatureSpan">unfluff.</span>extractor

#### [module unfluff.extractor](#apidoc.module.unfluff.extractor)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>author (doc)](#apidoc.element.unfluff.extractor.author)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>calculateBestNode (doc, lang)](#apidoc.element.unfluff.extractor.calculateBestNode)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>canonicalLink (doc)](#apidoc.element.unfluff.extractor.canonicalLink)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>copyright (doc)](#apidoc.element.unfluff.extractor.copyright)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>date (doc)](#apidoc.element.unfluff.extractor.date)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>description (doc)](#apidoc.element.unfluff.extractor.description)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>favicon (doc)](#apidoc.element.unfluff.extractor.favicon)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>image (doc)](#apidoc.element.unfluff.extractor.image)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>keywords (doc)](#apidoc.element.unfluff.extractor.keywords)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>lang (doc)](#apidoc.element.unfluff.extractor.lang)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>links (doc, topNode, lang)](#apidoc.element.unfluff.extractor.links)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>publisher (doc)](#apidoc.element.unfluff.extractor.publisher)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>softTitle (doc)](#apidoc.element.unfluff.extractor.softTitle)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>tags (doc)](#apidoc.element.unfluff.extractor.tags)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>text (doc, topNode, lang)](#apidoc.element.unfluff.extractor.text)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>title (doc)](#apidoc.element.unfluff.extractor.title)
1.  [function <span class="apidocSignatureSpan">unfluff.extractor.</span>videos (doc, topNode)](#apidoc.element.unfluff.extractor.videos)



# <a name="apidoc.module.unfluff"></a>[module unfluff](#apidoc.module.unfluff)

#### <a name="apidoc.element.unfluff.lazy"></a>[function <span class="apidocSignatureSpan">unfluff.</span>lazy (html, language)](#apidoc.element.unfluff.lazy)
- description and source-code
```javascript
lazy = function (html, language) {
  return {
    title: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.title_ ? this.title_ : this.title_ = extractor.title(doc);
    },
    softTitle: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.softTitle_ ? this.softTitle_ : this.softTitle_ = extractor.softTitle(doc);
    },
    date: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.date_ ? this.date_ : this.date_ = extractor.date(doc);
    },
    copyright: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.copyright_ ? this.copyright_ : this.copyright_ = extractor.copyright(doc);
    },
    author: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.author_ ? this.author_ : this.author_ = extractor.author(doc);
    },
    publisher: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.publisher_ ? this.publisher_ : this.publisher_ = extractor.publisher(doc);
    },
    favicon: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.favicon_ ? this.favicon_ : this.favicon_ = extractor.favicon(doc);
    },
    description: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.description_ ? this.description_ : this.description_ = extractor.description(doc);
    },
    keywords: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.keywords_ ? this.keywords_ : this.keywords_ = extractor.keywords(doc);
    },
    lang: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.language_ ? this.language_ : this.language_ = language || extractor.lang(doc);
    },
    canonicalLink: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.canonicalLink_ ? this.canonicalLink_ : this.canonicalLink_ = extractor.canonicalLink(doc);
    },
    tags: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.tags_ ? this.tags_ : this.tags_ = extractor.tags(doc);
    },
    image: function () {
      var doc;
      doc = getParsedDoc.call(this, html);
      return null != this.image_ ? this.image_ : this.image_ = extractor.image(doc);
    },
    videos: function () {
      var doc, topNode;
      if (null != this.videos_)
        return this.videos_;
      doc = getCleanedDoc.call(this, html);
      topNode = getTopNode.call(this, doc, this.lang());
      return this.videos_ = extractor.videos(doc, topNode);
    },
    text: function () {
      var doc, topNode;
      if (null != this.text_)
        return this.text_;
      doc = getCleanedDoc.call(this, html);
      topNode = getTopNode.call(this, doc, this.lang());
      return this.text_ = extractor.text(doc, topNode, this.lang());
    },
    links: function () {
      var doc, topNode;
      if (null != this.links_)
        return this.links_;
      doc = getCleanedDoc.call(this, html);
      topNode = getTopNode.call(this, doc, this.lang());
      return this.links_ = extractor.links(doc, topNode, this.lang());
    }
  };
}
```
- example usage
```shell
...
  "favicon": "http://cdn1.vox-cdn.com/community_logos/42931/favicon.ico",
  "links": [
    { "text": "Six Thirty", "href": "http://www.sixthirty.co/" }
  ]
}
'''

#### 'extractor.lazy(html, language)'

Lazy version of 'extractor(html, language)'.

The text extraction algorithm can be somewhat slow on large documents.  If you
only need access to elements like 'title' or 'image', you can use the
lazy extractor to get them more quickly without running the full processing
pipeline.
...
```



# <a name="apidoc.module.unfluff.extractor"></a>[module unfluff.extractor](#apidoc.module.unfluff.extractor)

#### <a name="apidoc.element.unfluff.extractor.author"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>author (doc)](#apidoc.element.unfluff.extractor.author)
- description and source-code
```javascript
author = function (doc) {
  var authorCandidates, authorList, cache$, cache$1, cache$2, cache$3, cache$4, cache$5, fallbackAuthor;
  authorCandidates = doc("meta[property='article:author'],     meta[property='og:article:author'], meta[name='author'],     meta
[name='dcterms.creator'],     meta[name='DC.creator'],     meta[name='DC.Creator'],     meta[name='dc.creator'],     meta[name='
creator']");
  authorList = [];
  authorCandidates.each(function () {
    var author, cache$, cache$1;
    author = null != (cache$ = doc(this)) && null != (cache$1 = cache$.attr('content')) ? cache$1.trim() : void 0;
    if (author)
      return authorList.push(author);
  });
  if (authorList.length === 0) {
    fallbackAuthor = (null != (cache$ = doc("span[class*='author']").first()) ? cache$.text() : void 0) || (null != (cache$1 = doc
("p[class*='author']").first()) ? cache$1.text() : void 0) || (null != (cache$2 = doc("div[class*='author']").first()) ? cache$2
.text() : void 0) || (null != (cache$3 = doc("span[class*='byline']").first()) ? cache$3.text() : void 0) || (null != (cache$4 =
doc("p[class*='byline']").first()) ? cache$4.text() : void 0) || (null != (cache$5 = doc("div[class*='byline']").first()) ? cache
$5.text() : void 0);
    if (fallbackAuthor)
      authorList.push(cleanText(fallbackAuthor));
  }
  return authorList;
}
```
- example usage
```shell
...
data = extractor.lazy(my_html_data, 'en');

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
...
```

#### <a name="apidoc.element.unfluff.extractor.calculateBestNode"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>calculateBestNode (doc, lang)](#apidoc.element.unfluff.extractor.calculateBestNode)
- description and source-code
```javascript
calculateBestNode = function (doc, lang) {
  var bottomNegativescoreNodes, cnt, i, negativeScoring, nodesNumber, nodesToCheck, nodesWithText, parentNodes, startingBoost, topNode
, topNodeScore;
  topNode = null;
  nodesToCheck = doc('p, pre, td');
  startingBoost = 1;
  cnt = 0;
  i = 0;
  parentNodes = [];
  nodesWithText = [];
  nodesToCheck.each(function () {
    var highLinkDensity, node, textNode, wordStats;
    node = doc(this);
    textNode = node.text();
    wordStats = stopwords(textNode, lang);
    highLinkDensity = isHighlinkDensity(doc, node);
    if (wordStats.stopwordCount > 2 && !highLinkDensity)
      return nodesWithText.push(node);
  });
  nodesNumber = nodesWithText.length;
  negativeScoring = 0;
  bottomNegativescoreNodes = nodesNumber * .25;
  _.each(nodesWithText, function (node) {
    var booster, boostScore, negscore, parentNode, parentParentNode, textNode, upscore, wordStats;
    boostScore = 0;
    if (isBoostable(doc, node, lang) === true)
      if (cnt >= 0) {
        boostScore = 1 / startingBoost * 50;
        startingBoost += 1;
      }
    if (nodesNumber > 15)
      if (nodesNumber - i <= bottomNegativescoreNodes) {
        booster = bottomNegativescoreNodes - (nodesNumber - i);
        boostScore = -1 * Math.pow(booster, 2);
        negscore = Math.abs(boostScore) + negativeScoring;
        if (negscore > 40)
          boostScore = 5;
      }
    textNode = node.text();
    wordStats = stopwords(textNode, lang);
    upscore = Math.floor(wordStats.stopwordCount + boostScore);
    parentNode = node.parent();
    updateScore(parentNode, upscore);
    updateNodeCount(parentNode, 1);
    if (parentNodes.indexOf(parentNode[0]) === -1)
      parentNodes.push(parentNode[0]);
    parentParentNode = parentNode.parent();
    if (parentParentNode) {
      updateNodeCount(parentParentNode, 1);
      updateScore(parentParentNode, upscore / 2);
      if (parentNodes.indexOf(parentParentNode[0]) === -1)
        parentNodes.push(parentParentNode[0]);
    }
    cnt += 1;
    return i += 1;
  });
  topNodeScore = 0;
  _.each(parentNodes, function (e) {
    var score;
    score = getScore(doc(e));
    if (score > topNodeScore) {
      topNode = e;
      topNodeScore = score;
    }
    if (topNode === null)
      return topNode = e;
  });
  return doc(topNode);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.unfluff.extractor.canonicalLink"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>canonicalLink (doc)](#apidoc.element.unfluff.extractor.canonicalLink)
- description and source-code
```javascript
canonicalLink = function (doc) {
  var tag;
  tag = doc('link[rel=canonical]');
  if (null != tag)
    return tag.attr('href');
}
```
- example usage
```shell
...
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''

Some of these data elements require calculating intermediate representations
of the html document. Everything is cached so looking up multiple data elements
...
```

#### <a name="apidoc.element.unfluff.extractor.copyright"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>copyright (doc)](#apidoc.element.unfluff.extractor.copyright)
- description and source-code
```javascript
copyright = function (doc) {
  var cache$, copyright, copyrightCandidates, text;
  copyrightCandidates = doc("p[class*='copyright'], div[class*='copyright'], span[class*='copyright'], li[class*='copyright'],
p[id*='copyright'], div[id*='copyright'], span[id*='copyright'], li[id*='copyright']");
  text = null != copyrightCandidates && null != (cache$ = copyrightCandidates.first()) ? cache$.text() : void 0;
  if (!text) {
    text = doc('body').text().replace(/\s*[\r\n]+\s*/g, '. ');
    if (!(text.indexOf('\xa9') > 0))
      return null;
  }
  copyright = text.replace(/.*?©(\s*copyright)?([^,;:.|\r\n]+).*/gi, '$2').trim();
  return cleanText(copyright);
}
```
- example usage
```shell
...

data = extractor.lazy(my_html_data, 'en');

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
...
```

#### <a name="apidoc.element.unfluff.extractor.date"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>date (doc)](#apidoc.element.unfluff.extractor.date)
- description and source-code
```javascript
date = function (doc) {
  var cache$, cache$1, cache$2, cache$3, cache$4, dateCandidates;
  dateCandidates = doc("meta[property='article:published_time'],     meta[itemprop*='datePublished'], meta[name='dcterms.modified
'],     meta[name='dcterms.date'],     meta[name='DC.date.issued'],  meta[name='dc.date.issued'],     meta[name='dc.date.modified
'], meta[name='dc.date.created'],     meta[name='DC.date'],     meta[name='DC.Date'],     meta[name='dc.date'],     meta[name='date
'],     time[itemprop*='pubDate'],     time[itemprop*='pubdate'],     span[itemprop*='datePublished'],     span[property*='datePublished
'],     p[itemprop*='datePublished'],     p[property*='datePublished'],     div[itemprop*='datePublished'],     div[property*='datePublished
'],     li[itemprop*='datePublished'],     li[property*='datePublished'],     time,     span[class*='date'],     p[class*='date'],
div[class*='date']");
  return (null != dateCandidates && null != (cache$ = dateCandidates.first()) && null != (cache$1 = cache$.attr('content')) ? cache
$1.trim() : void 0) || (null != dateCandidates && null != (cache$2 = dateCandidates.first()) && null != (cache$3 = cache$2.attr('
datetime')) ? cache$3.trim() : void 0) || cleanText(null != dateCandidates && null != (cache$4 = dateCandidates.first()) ? cache
$4.text() : void 0) || null;
}
```
- example usage
```shell
...
extractor = require('unfluff');

data = extractor.lazy(my_html_data, 'en');

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
...
```

#### <a name="apidoc.element.unfluff.extractor.description"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>description (doc)](#apidoc.element.unfluff.extractor.description)
- description and source-code
```javascript
description = function (doc) {
  var cache$, cache$1, tag;
  tag = doc("meta[name=description], meta[property='og:description']");
  if (null != tag && null != (cache$ = tag.first()) && null != (cache$1 = cache$.attr('content')))
    return cache$1.trim();
}
```
- example usage
```shell
...
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''

Some of these data elements require calculating intermediate representations
of the html document. Everything is cached so looking up multiple data elements
and looking them up multiple times should be as fast as possible.
...
```

#### <a name="apidoc.element.unfluff.extractor.favicon"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>favicon (doc)](#apidoc.element.unfluff.extractor.favicon)
- description and source-code
```javascript
favicon = function (doc) {
  var tag;
  tag = doc('link').filter(function () {
    var cache$;
    return (null != (cache$ = doc(this).attr('rel')) ? cache$.toLowerCase() : void 0) === 'shortcut icon';
  });
  return tag.attr('href');
}
```
- example usage
```shell
...
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''

Some of these data elements require calculating intermediate representations
of the html document. Everything is cached so looking up multiple data elements
and looking them up multiple times should be as fast as possible.

### Demo
...
```

#### <a name="apidoc.element.unfluff.extractor.image"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>image (doc)](#apidoc.element.unfluff.extractor.image)
- description and source-code
```javascript
image = function (doc) {
  var images;
  images = doc("meta[property='og:image'], meta[itemprop=image], meta[name='twitter:image:src'], meta[name='twitter:image'], meta
[name='twitter:image0']");
  if (images.length > 0 && images.first().attr('content'))
    return images.first().attr('content');
  return null;
}
```
- example usage
```shell
...
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''
...
```

#### <a name="apidoc.element.unfluff.extractor.keywords"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>keywords (doc)](#apidoc.element.unfluff.extractor.keywords)
- description and source-code
```javascript
keywords = function (doc) {
  var tag;
  tag = doc('meta[name=keywords]');
  if (null != tag)
    return tag.attr('content');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.unfluff.extractor.lang"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>lang (doc)](#apidoc.element.unfluff.extractor.lang)
- description and source-code
```javascript
lang = function (doc) {
  var cache$, l, tag, value;
  l = null != (cache$ = doc('html')) ? cache$.attr('lang') : void 0;
  if (!l) {
    tag = doc('meta[name=lang]') || doc('meta[http-equiv=content-language]');
    l = null != tag ? tag.attr('content') : void 0;
  }
  if (l) {
    value = l.slice(0, +1 + 1 || 9e9);
    if (/^[A-Za-z]{2}$/.test(value))
      return value.toLowerCase();
  }
  return null;
}
```
- example usage
```shell
...
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''

Some of these data elements require calculating intermediate representations
of the html document. Everything is cached so looking up multiple data elements
and looking them up multiple times should be as fast as possible.
...
```

#### <a name="apidoc.element.unfluff.extractor.links"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>links (doc, topNode, lang)](#apidoc.element.unfluff.extractor.links)
- description and source-code
```javascript
links = function (doc, topNode, lang) {
  var gatherLinks, links;
  links = [];
  gatherLinks = function (doc, topNode) {
    var nodes;
    nodes = topNode.find('a');
    return nodes.each(function () {
      var href, text;
      href = doc(this).attr('href');
      text = doc(this).html();
      if (href && text)
        return links.push({
          text: text,
          href: href
        });
    });
  };
  if (topNode) {
    topNode = postCleanup(doc, topNode, lang);
    gatherLinks(doc, topNode);
  }
  return links;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.unfluff.extractor.publisher"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>publisher (doc)](#apidoc.element.unfluff.extractor.publisher)
- description and source-code
```javascript
publisher = function (doc) {
  var cache$, cache$1, publisherCandidates;
  publisherCandidates = doc("meta[property='og:site_name'],     meta[name='dc.publisher'],     meta[name='DC.publisher'],     meta
[name='DC.Publisher']");
  if (null != publisherCandidates && null != (cache$ = publisherCandidates.first()) && null != (cache$1 = cache$.attr('content')))
    return cache$1.trim();
}
```
- example usage
```shell
...

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
...
```

#### <a name="apidoc.element.unfluff.extractor.softTitle"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>softTitle (doc)](#apidoc.element.unfluff.extractor.softTitle)
- description and source-code
```javascript
softTitle = function (doc) {
  var titleText;
  titleText = rawTitle(doc);
  return cleanTitle(titleText, [
    '|',
    ' - ',
    '\xbb'
  ]);
}
```
- example usage
```shell
...
'''javascript
extractor = require('unfluff');

data = extractor.lazy(my_html_data, 'en');

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
...
```

#### <a name="apidoc.element.unfluff.extractor.tags"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>tags (doc)](#apidoc.element.unfluff.extractor.tags)
- description and source-code
```javascript
tags = function (doc) {
  var elements, tags;
  elements = doc("a[rel='tag']");
  if (elements.length === 0) {
    elements = doc("a[href*='/tag/'], a[href*='/tags/'], a[href*='/topic/'], a[href*='?keyword=']");
    if (elements.length === 0)
      return [];
  }
  tags = [];
  elements.each(function () {
    var el, tag;
    el = doc(this);
    tag = el.text().trim();
    tag.replace(/[\s\t\n]+/g, '');
    if (tag && tag.length > 0)
      return tags.push(tag);
  });
  return _.uniq(tags);
}
```
- example usage
```shell
...
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''
...
```

#### <a name="apidoc.element.unfluff.extractor.text"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>text (doc, topNode, lang)](#apidoc.element.unfluff.extractor.text)
- description and source-code
```javascript
text = function (doc, topNode, lang) {
  if (topNode) {
    topNode = postCleanup(doc, topNode, lang);
    return formatter(doc, topNode, lang);
  } else {
    return '';
  }
}
```
- example usage
```shell
...
// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
...
```

#### <a name="apidoc.element.unfluff.extractor.title"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>title (doc)](#apidoc.element.unfluff.extractor.title)
- description and source-code
```javascript
title = function (doc) {
  var titleText;
  titleText = rawTitle(doc);
  return cleanTitle(titleText, [
    '|',
    ' - ',
    '\xbb',
    ':'
  ]);
}
```
- example usage
```shell
...

'''javascript
extractor = require('unfluff');

data = extractor.lazy(my_html_data, 'en');

// Access whichever data elements you need directly.
console.log(data.title());
console.log(data.softTitle());
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
...
```

#### <a name="apidoc.element.unfluff.extractor.videos"></a>[function <span class="apidocSignatureSpan">unfluff.extractor.</span>videos (doc, topNode)](#apidoc.element.unfluff.extractor.videos)
- description and source-code
```javascript
videos = function (doc, topNode) {
  var candidates, results, urls, videoList;
  videoList = [];
  candidates = doc(topNode).find('iframe, embed, object, video');
  candidates.each(function () {
    var candidate, tag;
    candidate = doc(this);
    tag = candidate[0].name;
    if (tag === 'embed') {
      if (candidate.parent() && candidate.parent()[0].name === 'object') {
        return videoList.push(getObjectTag(doc, candidate));
      } else {
        return videoList.push(getVideoAttrs(doc, candidate));
      }
    } else if (tag === 'object') {
      return videoList.push(getObjectTag(doc, candidate));
    } else if (tag === 'iframe' || tag === 'video') {
      return videoList.push(getVideoAttrs(doc, candidate));
    }
  });
  urls = [];
  results = [];
  _.each(videoList, function (vid) {
    if (vid && vid.height && vid.width && urls.indexOf(vid.src) === -1) {
      results.push(vid);
      return urls.push(vid.src);
    }
  });
  return results;
}
```
- example usage
```shell
...
console.log(data.date());
console.log(data.copyright());
console.log(data.author());
console.log(data.publisher());
console.log(data.text());
console.log(data.image());
console.log(data.tags());
console.log(data.videos());
console.log(data.canonicalLink());
console.log(data.lang());
console.log(data.description());
console.log(data.favicon());
'''

Some of these data elements require calculating intermediate representations
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
