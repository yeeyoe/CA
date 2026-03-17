
#内容：
index.qmd 前言
chapter1 第一章 其中包含 Chap1_index.qmd 合并各节的内容

#输出到docs文件夹，包括index.html和pdf

#辅助文件：
_quarto.yml 总的配置文件
latex-preamble.tex 编译pdf时的latex配置
mathjax-preamble.html 编译html时的mathjax配置
.gitignore 指定哪些文件不用同步到云端
glossary.lyx 是给IDE记忆的符号约定，以便自动补全


quarto render --to pdf
quarto render --to html

quarto render chapter1/Chap1_index.qmd

quarto render chapter1/Chap1_index.qmd --profile slides --to revealjs