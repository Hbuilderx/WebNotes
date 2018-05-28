# DOM节点

## 按关系来划分

### 祖先节点

### 父亲节点

### 兄弟节点

## 按节点类型划分

使用nodeType来查看节点的类型，会返回一个数字
使用nodeValue查看属性的值
使用nodeName查看属性的名称
使用childNodes 获得某个节点下面的所有子节点，是个类数组)
使用attributes 属性来获取节点的属性，是个类数组

### 元素节点

#### nodeType返回1

### document

#### nodeType返回9

### 文本节点

包括文字换行和空格等

#### nodeType返回3

### 注释节点

#### nodeType返回8

### 属性节点

#### nodeType返回2
