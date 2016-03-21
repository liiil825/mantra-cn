# D. Appendix: File Naming Conventions

在[目录结构](#sec-Directory-Layout)中，我们讨论一些方法能对不同组件组织文件。

这是我们讨论的方法的文件名称。
Here we discuss ways to name files.

## Source File Names

当我们从文件名称删除扩展，它能满足以下条件：

* 所有字符都是小写。
* 文件名称应该是[字母数字](https://en.wikipedia.org/wiki/Alphanumeric)并可以有`_`符号。
* 文件名应该以字母开始。

这里有以上规则的正则表达式：

```js
/^[a-z]+[a-z0-9_]+$/
```

## Test File Names

这是在`tests`目录里的文件命名。规则如下：

* 它应该在目标目录下是一个唯一文件名称。
* 如果没有，删除后缀时，应该有一个相同的源目录的文件名。

### Postfix

大多时候，对每一个资源文件我们有一个测试文件。优势，我们需要对一个资源文件创建多个测试文件。那时我们使用后缀。

如果那个资源文件是`posts.js`，然后后缀看起来是这样：

```
posts-part1.js
posts-part2.js
```

这是上述规则的正则表达式：

```js
/^([a-z]+[a-z0-9_]+)(\-[a-z]+[a-z0-9_]+)*$/
```

