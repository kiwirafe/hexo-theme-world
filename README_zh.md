# hexo-theme-world

### 一个为i18n（双语言）量身定做的 Hexo 主题

#### Demo : https://kiwirafe.github.io/hexo-theme-world

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

2. 将 `theme/world/_config.world.yml` 文件中的内容复制到主配置文件 `_config.yml` 中。这部操作只会修改一小部分内容以支持 i18n（国际化）。

3. 在 `_config.yml` 文件的末尾，根据你的需求更改language部分：
```yml
generator_plus:
  language: ['first language', 'second language']
```

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
