# C. Appendix: Organizing Modules

Mantra有个百分百[基于模块](#sec-Mantra-Modules)程序结构。这应该至少有一个模块。

我们已经讨论了在一个模块内怎么组织文件并且怎么使用它们。但是，我们还没有讨论怎么组织模块。

那是因为程序和程序间是不同的。

然而，我建议一些潜在的形式，使用它能组织模块。
However, we are suggesting some potential patterns that can be used to organize modules.

## Single Core Module

对于简单的程序，我们将所有代码写入一个叫`core`的单个模块。这将对简单程序较小的客户端代码库工作。

## Core Module & Multiple Feature Modules

这是一个对于上面"单核心模块"以外的模式。它是：

* 我们有一个核心模块包含所有核心客户端代码，包含所有程序路由。
* 然后我们有不同模块对程序中主要的功能。这些模块不包含路由。

## Multi Modules

这钟多模块方法没有核心模块。
This the multi-module approach where there is no single core module.

* 这里有多个模块对程序中的不同功能。
* 他们中的每一个都有自己的路由。

## Pages Module

请注意：这个能和上述其他模式一起使用。

有时，我们需要一些UI页面。他们没有自己的actions, routes, 或configrations。他们只有包含一些UI代码。这些可以使UI组件或一些containers。
Sometimes, we need to show some UI pages. They don't have their own actions, routes, or configurations. They only contain some UI code. These can be either UI components or some containers.

对于这个目的，我们能使用一个[implicit module](#sec-Implicit-Modules)。

