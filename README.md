# hexo-theme-world

### A Hexo theme devoted to i18n (multilingual support).

#### [中文文档](README_zh.md)  |  [Online Demo](https://kiwirafe.github.io/hexo-theme-world)

## Installation
In the root directory of your site:
```bash
$ npm uninstall hexo-generator-index hexo-generator-archive hexo-generator-category hexo-generator-tag
$ npm install hexo-generator-plus --save
$ git clone https://github.com/kiwirafe/hexo-theme-world.git themes/world
```

## Usage
Change the theme to world in _config.yml:
```yml
theme: world
```

and turn off syntax highlighter (the theme uses customized CDN instead):
```yml
syntax_highlighter: 
```

If your site contains only one language, there's no additional actions required. This package will generate files as normal.

### i18n
Please follow these steps for internationalization
1. Create a new folder for each language, and put all posts and pages in the corresponding folder. For example:
```plaintext
sources/
  en/
    post1.md
    post2.md
  zh/
    post3.md
    post4.md
```

2. Copy the content from `theme/world/_config.world.yml` into your main `_config.yml` file. This action will only modify a few lines to enable i18n support.

3. At the right end of your `_config.yml` file, change the language settings if needed:
```yml
generator_plus:
  language: ['first language', 'second language']
```

### Front-Matter
This theme supports categories and tags. All you have to do is add the following to front-matter:
```yml
---
category: "My Category"
tag: "My Tag"
---
```

This theme also supports Mathjax:
```yml
---
mathjax: true
---
```