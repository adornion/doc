---
title: Quick start
description: A quick start tutorial to step you through the process of setting up a Hugo website using the Adornion theme
---

{{< article-open >}}
{{< single-column-band-open >}}

Create a website for company `Quick Start`. The source of the website will be stored in a folder '`quick-start-website`' on your computer.

Steps:
1. **Hugo**\
Install the latest extended release of [Hugo](https://gohugo.io/installation/).
1. **Embedded Dart Sass**\
Install [Embedded Dart Sass](https://www.brycewray.com/posts/2022/05/using-dart-sass-hugo-nitty-gritty/) and make sure it works with Hugo.
1. **Git**\
[Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
1. **Website source folder**\
Create the folder which will hold the source for your Hugo website.  Make this your current directory.
    ```shell
    md quick-start-website
    cd quick-start-website
    ```
1. **Git Ignore**\
Create the file `.gitignore` which will specify the files which should not be added to your GIT repository. Use a text editor to populate it with the following lines:
    ```sh
    # Add any directories, files, or patterns you don't want to be tracked by version control
    /resources/
    /public/
    .hugo_build.lock
    ```
1. **Adornion**\
Install the Adornion Hugo theme as a Git submodule
    ```shell
    git submodule add https://github.com/adornion/adornion.git themes/adornion
    ```
1. **Hugo config folder**\
Create the folder `config/_default` which will hold the Hugo configuration file. Make this folder your current directory.
    ```shell
    md config
    cd config
    md _default
    cd _default
    ```
1. **Hugo config file**\
Create the file `hugo.yaml` in this default config folder and use a text editor to populate it with the following text:
    ```txt
    baseURL: https://quick-start.com/
    languageCode: en-us
    title: Quick Start
    theme: adornion
    ```
1. **Return to root**\
Return to the root folder of your Hugo website source.
    ```shell
    cd ../..
    ```
1. **Content folder**\
Create the folder `content`. This will hold the markdown content files for your website. Make this folder your current directory.
    ```shell
    md content
    cd content
    ```
1. **Home page**\
Create the file `_index.md` in the root of the `content` folder and use a text editor to populate it with the following text:
    ```txt
    ---
    title: Quick Start Home
    description: Quick Start Corporation website home page
    ---

    {{</* article-open */>}}
    {{</* single-column-band-open */>}}

    Welcome to **Quick Start**.
    <Add more markdown>

    {{</* single-column-band-close */>}}
    {{</* article-close */>}}
    ```
1. **Test**\
Start the development server
    ```shell
    hugo server
    ```
    and then view the home web page in your browser using URL: `http://localhost:1313/`

For more information see:
* [https://gohugo.io/getting-started/quick-start/](https://gohugo.io/getting-started/quick-start/)
* [Adornion Use]({{< ref "/use" >}})

{{< single-column-band-close >}}
{{< article-close >}}