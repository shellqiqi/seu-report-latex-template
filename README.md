# SEU LaTeX Template

LaTeX template for Southeast University

## 使用简介

支援且推荐使用 [TeX Live](http://www.tug.org/texlive/)，并推荐使用 xetex 引擎编译。

## 使用Visual Studio Code（可选）

安装 [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)，并在用户设置内添加以下内容：

```js
{
    "latex-workshop.chktex.enabled": false,
    "latex-workshop.latex.toolchain": [
        {
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        }
    ],
    "[latex]": {
        "editor.wordWrap": "on"
    }
}
```
