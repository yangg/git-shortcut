# git-shortcut

[![Build Status](https://travis-ci.org/yangg/git-shortcut.svg?branch=master)](https://travis-ci.org/yangg/git-shortcut) [![Code Climate](https://codeclimate.com/github/yangg/git-shortcut/badges/gpa.svg)](https://codeclimate.com/github/yangg/git-shortcut) [![npm:](https://img.shields.io/npm/v/git-shortcut.svg?style=flat)](https://www.npmjs.com/packages/git-shortcut) [![Dependency Status](https://david-dm.org/yangg/git-shortcut.svg)](https://david-dm.org/yangg/git-shortcut)

git 命令行下快捷操作其它项目

git-shortcut helps you quickly run git commands work with multiple repos without switch directory

## Installation
```bash
npm install -g git-shortcut
```

## Usage

### 使用别名操作项目
```bash
g -s b ../blog    # 添加别名 add alias
g b status        # 使用别名 use alias
g b pull
g ../static pull  # 直接操作目录
g push            # 如果没有别名匹配时, g 相当于 git 的别名
                  # work as a alias for git if no alias matched
```

### 使用特殊别名 `-`，用于经常切换于两个 repo 之间时，操作相对应的另一个项目
### special alias `-`, work on the related repo, and vice versa
```bash
# cwd Main
g -s - ../static    # 添加`-'别名
g - status          #
cd ../static
g - st              # show status of Main
```

### 同时操作多个项目
```bash
g -p - pull           # pull current repo and alias `-'
g -p b pull           # pull current repo and alias `b'
g -p -,b pull         # pull current repo, alias `-' and `b'
```

![git-shortcut usage](https://cloud.githubusercontent.com/assets/409225/16899413/71c59dda-4c35-11e6-8d93-ad261a99fe8a.gif)

### Remove alias
```bash
g -s b ''
```

### Config file
`~/.git-shortcut.yml`


## License
MIT
