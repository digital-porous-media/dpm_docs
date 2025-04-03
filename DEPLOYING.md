# How to Deploy

Deploys rely on [GitHub Pages](https://pages.github.com/) and [MkDocs command `gh-deploy`](https://www.mkdocs.org/user-guide/deploying-your-docs/).

0. [Install dependencies](https://tacc.github.io/mkdocs-tacc/test/#test-locally).
1. Run the command to build and trigger a deploy.
    ```shell
    mkdocs gh-deploy
    ```
2. Wait for [GitHub action](https://github.com/wesleyboar/Digital-Rocks-Docs/actions) to complete.
3. Load https://wesleyboar.github.io/Digital-Rocks-Docs/.
