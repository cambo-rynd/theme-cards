---
title: "Think twice before you think again..."
description: "This is for testing purposes-- Kyle sucks"
# linkTitle:
date: 2024-12-02T11:47:31+08:00
draft: false
noindex: false
featured: true
pinned: true
nav_weight: 1
nav_icon:
  vendor: bootstrap
  name: cloud-download
  color: green
series:
  - Docs
categories:
tags:
  - Installation
images:
  - images/hqdefault.jpg
# menu:
#   main:
#     weight: 100
#     params:
#       icon:
#         vendor: bs
#         name: book
#         color: '#e24d0e'
authors:
  - cr
---

This is still just a staging site with shenanigans going on.

{{< bs/alert danger >}}
{{< markdownify >}}
Please run these commands from [PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows) or a Linux terminal such as WSL or Git Bash.
{{< /markdownify >}}
{{< /bs/alert >}}

## Requirements
- a 9-Iron
- ice cubes
- Go
- Hugo extended version
- Node.js `16` or later

Read more on [not clicking random links](https://www.youtube.com/watch?v=dQw4w9WgXcQ).

## Clone the Repository

```sh
git clone --depth 1 https://github.com/hbstack/theme-cards
```

## Copy the Example Site

```sh
cp -r theme-cards/exampleSite mysite
```

## Change Working Directory

```sh
cd mysite
```

## Tweak `go.mod`

{{< bs/alert >}}
{{< markdownify >}}
This guide uses `sed` command to edit the file, please feel free to open and edit the `go.mod` with your favorite editor.
{{< /markdownify >}}
{{< /bs/alert >}}

### Replace Module Path

The module path is the identifier of your site, which typically is your repo URL, take `github.com/user/repo` as an example, you'll need to replace the `module github.com/hbstack/theme-cards/exampleSite` with `module github.com/user/repo`.

```sh
sed -i '1s/.*/module github.com\/user\/repo/' go.mod
```

### Delete the `replace` Directive

To build the site successfully, you'll need to delete the internal used `replace` directive: `replace github.com/hbstack/theme-cards => ../`.

```sh
sed -i '/^replace/d' go.mod
```

## Install Dependencies

```sh
npm ci
```

## Hugo Module Proxy (Optional)

A [test](https://www.youtube.com/watch?v=dQw4w9WgXcQ) is required to see if you are still clicking random links.

## Preview Locally

```sh
npm run dev
```

## What's Next?

1. Tweak Configurations, such as `baseURL`, `giscus.*` and so on.
2. Remove testing content.
3. Read the [Do not click](https://www.youtube.com/watch?v=dQw4w9WgXcQ).
4. Find more [what did I just tell you](https://www.youtube.com/watch?v=dQw4w9WgXcQ)?

### Bingo Sucks
