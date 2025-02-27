## text

<!-- UTSCOMJSON.text.description -->

在app-uvue和app-nvue中，文本只能写在text中，而不能写在view的text区域。文本样式的控制也应该在text组件上写style，而不是在view的样式里写。

虽然app-uvue中写在view的text区域的文字，也会被编译器自动包裹一层text组件，看起来也可以使用。但这样会造成无法修改该text文字的样式，详见uvue的[样式不继承](uni-app-x/css/README.md#stylenoextends)章节。

<!-- UTSCOMJSON.text.attrubute -->

<!-- UTSCOMJSON.text.event -->

<!-- UTSCOMJSON.text.example -->

<!-- UTSCOMJSON.text.compatibility -->

## 子组件

text组件在web浏览器渲染（含浏览器、小程序webview渲染模式、app-vue）和uvue中，可以并只能嵌套text组件。

但注意，app-uvue的text组件嵌套后子组件也不继承父组件样式，这样使用会在编译到浏览器平台时产生差异。所以尽量避免使用text嵌套。

app-nvue中，text组件不能嵌套。

<!-- UTSCOMJSON.text.children -->

<!-- UTSCOMJSON.text.reference -->

## Bug & Tips@tips
- app-uvue不支持[HTML字符实体](https://developer.mozilla.org/zh-CN/docs/Glossary/Entity)。
- app-uvue的selectable开启后，仅支持全部文字复制，不支持自由调整光标选择文字。如需自由选择文字，请使用[rich-text组件](rich-text.md)。