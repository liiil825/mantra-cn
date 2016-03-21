# B. Appendix: Server-Side Directory Layout

这是你的项目服务端的目录结构。这**不是**Mantra的核心部分，但是它遵循我们程序中使用过的客户端目录结构。

在服务端，我有4个目录和一个叫`main.js`的JavaScript文件。

```
* methods
* publications
* libs
* configs
* main.js
```

让我们来看看这些目录和文件。

## methods

这个目录是程序中我们放置methods的地方。这是这些文件在目录中的样子：

```
* posts.js
* index.js
* tests
  - posts.js
```

这里我们有一个称为`posts.js`的文件，它有程序中针对`posts`特性的methods。根据你的应用，我们有不同的文件。

在这个JavaScript文件中，我们有一个default函数输出。Meteor methods被定义在那个函数中。

当命名在`posts.js`里面的methods是，总是前缀的方法名称。那个前缀文件名称包含一个句号(.)。

在我们例子中，前缀是`post.`。

举个例子，这里有一些methods在`posts.js`中：

```js
import {Posts, Comments} from '/lib/collections';
import {Meteor} from 'meteor/meteor';
import {check} from 'meteor/check';

export default function() {
  Meteor.methods({
    'posts.create'(_id, title, content) {
      //  method body
    }
  });

  Meteor.methods({
    'posts.createComment'(_id, postId, text) {
      //  method body
    }
  });
}
```

最后，这里有一个命名为`index.js`的文件，它引入其他所有在这个目录下的模块并且调用他们default输出。所以，当引入methods时，我们能只引入一个。

这有个简单`index.js`文件：

```js
import posts from './posts';
import admin from './admin';

export default function () {
  posts();
  admin();
}
```

### Tests

我们能在tests目录里为methods编写测试。因此，进行集成测试比单元测试要好。

因此，你能使用[Gagarin](https://github.com/anticoders/gagarin)。

## publications

这个目录和`methods`目录一样，但是我们写publications代替methods。

## libs

这个目录包含我们在服务器内部能使用的通用函数。

## configs

这个地方我们能写程序的配置信息。这些配置文件应该有一个default函数输出，这个函数能被引入并调用。配置信息需要在这个函数信息里。

这里有个配置的示例：

```js
export default function() {
  //  invoke the configuration here
}
```

## main.js

这个地方是我们程序中开始的入口。在这个文件里我们将调用引入methods, publications和configuration。
This is the place where we can start as the entry point for our app. We'll import methods, publications and configuration inside this file and invoke.

这里有个`main.js`文件的示例：

```js
import publications from './publications';
import methods from './methods';
import addInitialData from './configs/initial_adds.js';

publications();
methods();
addInitialData();
```

请注意：去看看这个[简单程序](https://github.com/mantrajs/mantra-sample-blog-app/tree/master/server)了解它实现这些指导方针。

