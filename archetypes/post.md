---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
# weight: 1
# aliases: ["/first"]
tags: []
author: "{{ .Site.Params.author }}"
showToc: true
tocOpen: false
draft: true
hidemeta: false
comments: false
description: ""
canonicalURL: ""
disableHLJS: false
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
  image: ""
  alt: ""
  caption: ""
  relative: false
  hidden: true
editPost:
  URL: "https://github.com/yourusername/yourrepo/content"
  Text: "Suggest Changes"
  appendFilePath: true
---
