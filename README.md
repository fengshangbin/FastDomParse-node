# FastDomParse-node
hello
fast dom parse for node.js  
GitHub Pages: https://github.com/fengshangbin/FastDomParse-node

# 如何使用 FastDomParse-node

```
npm install --save fastdomparse-node
...
const fastdom = require("fastdomparse-node");

let dom = new fastdom(htmlString);

//单目标查询
let element = dom.querySelector("div.page li[name=1]");

//多目标查询
let elements = dom.querySelectorAll("div.page li");

//目标子查询
let sun = element.querySelector("div.page li[name=1]");
let suns = element.querySelectorAll("div.page li[name=1]");

//element属性
let inner = element.getInnerHTML();
element.setInnerHTML("hello fast dom parse");

let outer = element.getOuterHTML();
element.setOuterHTML("<div>hello fast dom parse<div>");

let attr = element.getAttribute("id");
element.setAttribute("id", "content");
let hasID = element.hasAttribute("id");

//获取整个dom内容
dom.html
```

熟悉的味道，一样的配方，和原生 DOM 一样的语法，无需新学习，使用简单。
