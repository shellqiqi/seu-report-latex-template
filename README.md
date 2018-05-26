# SEU LaTeX Template

东南大学 LaTeX 模板

LaTeX template for Southeast University

## 使用简介

支援且推荐使用 [TeX Live](http://www.tug.org/texlive/)，并推荐使用 xetex 引擎编译。

## 中文字体需求

默认采用[思源宋体](https://github.com/adobe-fonts/source-han-serif/tree/release)作为衬线字体，[更纱黑体](https://github.com/be5invis/Sarasa-Gothic/tree/releases)作为非衬线与等宽字体。

## 使用Visual Studio Code

安装 [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)，并在用户设置内添加以下内容：

```conf
{
    "latex-workshop.chktex.enabled": false,
    "latex-workshop.latex.tools": [
        {
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ],
            "name": "Step 1: xelatex"
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "toolchain",
            "tools": [
                "Step 1: xelatex"
            ]
        }
    ],
    "[latex]": {
        "editor.wordWrap": "on"
    }
}
```
