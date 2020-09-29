This module exports list-related schema elements and commands. The
commands assume lists to be nestable, with the restriction that the
first child of a list item is a plain paragraph.

@cn 本模块导出了列表相关的 schema 元素和命令。命令假设列表是可以被嵌套的，以及限制列表项的第一个元素必须为普通段落元素。

These are the node specs:

@cn 下面这些是节点配置对象：

@orderedList
@bulletList
@listItem

@addListNodes

Using this would look something like this:

@cn 本模块使用方式应该像下面这样：

```javascript
const mySchema = new Schema({
  nodes: addListNodes(baseSchema.spec.nodes, "paragraph block*", "block"),
  marks: baseSchema.spec.marks
})
```

The following functions are [commands](/docs/guide/#commands):

@cn 下列函数是 [命令](/docs/guide/#commands)：

@wrapInList
@splitListItem
@liftListItem
@sinkListItem
