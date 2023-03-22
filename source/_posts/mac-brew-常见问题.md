---
title: mac brew 常见问题
date: 2023-02-24 17:56:28
tags:
---

使用brew时候报错

```
Warning: formula.json: update failed, falling back to cached version.
Error: Cannot download non-corrupt https://formulae.brew.sh/api/formula.json!
```

解决方法

```
export HOMEBREW_NO_INSTALL_FROM_API=1
```

