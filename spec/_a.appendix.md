# A. Appendix: Prerequisite

这些资源将帮助你清楚的理解Mantra

## ES2015

ES2015是JavaScript2015版本的标准。它不是完全的被所有浏览器或服务器实现。但是，使用[babel](https://babeljs.io/)，我们今天就能使用ES2015。

请注意：Meteor内置支持ES2015

ES2015是发生在JavaScript最好的事。它介绍了大量特性和修复了常见问题。

* [学习ES2015: 你好ES2015](https://tutor.mantrajs.com/say-hello-to-ES2015/introduction)

## React

React是基于JavaScript的一个UI框架。基本上，你创建JavaScript的UI。首先，**它感觉很古怪**。但是你一旦学会基本的你将发现它非常有趣。

只是忘了片刻我们已经知道的HTML，并学习React。然后再思考。这里有些资源：

* [官方教程](https://facebook.github.io/react/docs/tutorial.html)
* [从Scotch.io开始学习React](https://scotch.io/tutorials/learning-react-getting-started-and-concepts)
* [React Components, Elements, and Instances](https://medium.com/@dan_abramov/react-components-elements-and-instances-90800811f8ca)

## React Containers

现在，我们在React组件很少使用state。相反，我们通过props接受props。React的[stateless组件](https://medium.com/@joshblack/stateless-components-in-react-0-14-f9798f8b992d)使它容易。

然后，我们组成React containers获取不同的数据源并且加载到UI组件。项目如[react-komposer](https://github.com/kadirahq/react-komposer)使用容易。检查下面的文章以了解更多信息：

* [让我们组成React Containers](https://voice.kadira.io/let-s-compose-some-react-containers-3b91b6d9b7c8#.my9ynz9e2)

## Meteor Basics

你需要有好的Meteor基础。为此，关注Meteor的 [官方教程](https://www.meteor.com/tutorials/react/creating-an-app).

请注意：Mantra使用以上技术有一点不同。例如，Meteor的React教程建议使用mixin来访问mongo数据库。但是Mantra使用一个container，一个更现代的使用React。
