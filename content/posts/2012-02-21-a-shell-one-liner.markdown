---
categories: null
comments: true
date: "2012-02-21T00:00:00Z"
title: A shell one-liner
---

```bash
git log --grep <query> | sed -n '/^commit/p' | cut -d\  -f 2 | xargs git show
```

Show all changesets matching *query*. Useful for reviewing a series of related
changes over time. (Assuming consistent commit message habits.)

Don't fear the shell.
