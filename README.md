# Develop 環境 123

## Git 小黑貓

Git 設定: [github sshkeyGen](http://wiki.csie.ncku.edu.tw/github)

gh-page: <https://quilaty.github.io/bookmark/>

## Markdown Note

[Udemy Class: Easy Markdown with VsCode](https://www.udemy.com/easy-markdown-with-vs-code/learn/v4/content)

* VsCode extension:
  * GFM Preview
  * Markdown PasteURL
  * Markdown Shortcuts
  * markdownlint

* Markdown 相關符號: [&whart discover your character](http://www.amp-what.com/unicode/search/fire)

## MkDocs Installation

MkDocs document: [Home](http://www.mkdocs.org/)

### 手動安裝管理工具

1. [Python 3.6.3](https://www.python.org/)
    1. 確認 Python 的系統環境變數是否有設定，可以在 bash的小黑框使用 python的指令
    1. 確認:

        ```bash
        $ python --version
        Python 2.7.2
        $ pip --version
        pip 1.5.2
        ```

1. 安裝 MkDocs

    ```bash
    pip install mkdocs
    ```

    1. 確認

        ```bash
        mkdocs --version
        ```

## 開始 project

1. 建立文件
    ```bash
    mkdocs new name-project
    ```
    1. 測試
    ```bash
    mkdocs serve
    ```
    `ctrl + c` 離開 serve模式

## 發佈到線上

1. 發佈到 Github Page
    ```bash
    mkdocs gh-deploy
    ```
