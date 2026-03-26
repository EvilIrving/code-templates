# Changelog

避免过多解释，记录 situation reason solution 的格式，方便后续回顾，描述不必过多。

Q: github push 遇到 Invalid username or token. Password authentication is not supported for Git operations 问题，
A：查看 git remote -v 得知 remote url 被设置为 https，将其改成 ssh 连接即可："git remote set-url origin <git@github.com>:EvilIrving/svelte-high-tree.git"
