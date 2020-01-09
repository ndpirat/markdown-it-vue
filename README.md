# markdown-it-vue

[![Build Status](https://travis-ci.org/ravenq/markdown-it-vue.svg?branch=master)](https://travis-ci.org/ravenq/markdown-it-vue)

> The vue lib for markdown-it.

## Demo online

[http://www.aqcoder.com/markdown](http://www.aqcoder.com/markdown)

## Install

```sh
npm install markdown-it-vue
```

## Supports

- Official markdown syntax.
- GFM TOC
- GFM style
- emoji
- Flowcharts.js
- Subscript/Superscript
- [AsciiMath](http://asciimath.org/)
- info | error | warning message tip

## Plugin list

- markdown-it
- markdown-it-emoji
- markdown-it-sub
- markdown-it-sup
- markdown-it-footnote
- markdown-it-deflist
- markdown-it-abbr
- markdown-it-ins
- markdown-it-mark
- markdown-it-katex
- markdown-it-task-lists
- markdown-it-highlight
- markdown-it-latex
- markdown-it-container
- markdown-it-github-toc
- markdown-it-source-map
- markdown-it-link-attributes

internal plugin list:

- markdown-it-plugin-flowchart

## Options

use `options` property to specify the options of markdow-it and markdown-it-plugins.

```html
<markdown-it-vue class="md-body" :content="content" :options="options" />
```

```js
options: {
  markdownIt: {
    linkify: true
  },
  linkAttributes: {
    attrs: {
      target: '_blank',
      rel: 'noopener'
    }
  }
}
```

more markdown-it options see <https://markdown-it.github.io/markdown-it/>.

amd default plugins options:

```js
{
  linkAttributes: {
    attrs: {
      target: '_blank',
      rel: 'noopener'
    }
  },
  katex: {
    throwOnError: false,
    errorColor: '#cc0000'
  }
}
```

## More plugins

it can add your plugin to markdown-it-vue by the `use` method.

```js
this.$refs.myMarkdownItVue.use(MyMarkdownItPlugin)
```

## Usage

```vue
<template>
  <div>
    <markdown-it-vue class="md-body" :content="content" />
  </div>
</template>

<script>
import MarkdownItVue from 'markdown-it-vue'
import 'markdown-it-vue/dist/markdown-it-vue.css'
export default {
  components: {
    MarkdownItVue
  },
  data() {
    return {
      content: '# your markdown content'
    }
  }
}
</script>
```

## ScreenShot

![markdown-it-vue](https://github.com/ravenq/markdown-it-vue/blob/master/doc/markdown-it-vue.png?raw=true)

## License

[MIT](https://github.com/ravenq/markdown-it-vue/blob/master/LICENSE)
