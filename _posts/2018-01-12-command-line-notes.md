---
title: Command Line Notes
---

* TOC
{:toc}

Windows Command Prompt & PowerShell
-----
Remove characters from folder (first 1 for example below)
```
get-childitem *.txt | rename-item -newname { [string]($_.name).substring(1) }
```
