# hexo-theme-world

#### [中文文档](README_zh.md) 
#### Demo : https://kiwirafe.github.io/hexo-theme-world

A theme devoted to i18n for [Hexo](https://hexo.io/)

## 安装
在网站的根目录下运行：
```bash
$ npm uninstall hexo-generator-index hexo-generator-archive hexo-generator-category hexo-generator-tag
$ npm install hexo-generator-plus --save
$ git clone https://github.com/kiwirafe/hexo-theme-world.git themes/world
```

## 使用方法
在 _config.yml 里将主题设置为world:
```yml
theme: world
```

然后取消代码高亮（使用CDN高亮）:
```yml
syntax_highlighter: 
```

如果您的网站仅包含一种语言，则无需执行其他操作。

## 国际化（i18n）
请按照以下步骤进行国际化：
1. 为每种语言创建一个新文件夹，并将所有文章和页面放入相应的文件夹中。例如：
```plaintext
sources/
  en/
    post1.md
    post2.md
  zh/
    post3.md
    post4.md
```
2. 在 _config.yml 中添加以下内容：
```yaml
generator_plus:
  language: ['first language', 'second language']
```
3. 将 _config.yml 中的 `new_post_name` 变量更改为 `new_post_name: :lang/:title.md`
4. 将 _config.yml 中的 `permalink` 变量更改为 `permalink: :lang/{这里原来的内容}`

### Front-Matter
这个主题支持分类和标签。你只需在 Front-Matter 中添加以下内容：
```yml
---
category: "My Category"
tag: "My Tag"
---
```

这个主题也支持 Mathjax：
```yml
---
mathjax: true
---
```