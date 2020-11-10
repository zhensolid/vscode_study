Markdown 的预览中可以通过CSS实现图像及表格的居中。这和使用的编辑器及其采用的样式有关。

在 vscode 的 Markdown Preview Enhanced 中，要自定义 css，按下 cmd-shift-p
然后运行 Markdown Preview Enhanced: Customize Css，通过修改 style.less 实现。

图片居中可以通过添加以下代码实现：

// 图片居中
img {
    position: relative;
    left: 50%;
    transform: translateX(-50%);
}
其它的对其可以通过调用新添加的以下class实现：

.center {
  width: auto;
  display: table;
  margin-left: auto;
  margin-right: auto;
}

例如表格，可以写进div块里，然后通过以下方法实现：

<div class="center">

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |

</div>
虽然图像和文字居中也可以使用标签实现，但HTML5不支持使用标签，推荐使用css代替。