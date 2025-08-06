# 🚀 我的 Oh My Zsh 插件完整使用指南

> 您当前安装了 **22 个插件**，拥有 **400+ 个快捷命令**！
> 最后更新：2025年8月6日

---

## 📋 目录
1. [Git 相关插件](#git-相关插件)
2. [开发工具插件](#开发工具插件)
3. [系统增强插件](#系统增强插件)
4. [文件和目录操作插件](#文件和目录操作插件)
5. [实用工具插件](#实用工具插件)
6. [自动补全和语法高亮](#自动补全和语法高亮)

---

## 🔧 Git 相关插件

### 1. **git** 插件
**功能**: 提供 Git 快捷命令，是最常用的插件

#### 📌 添加文件
```bash
g        # git
ga       # git add
gaa      # git add --all               # 添加所有文件
gapa     # git add --patch             # 交互式添加
gau      # git add --update            # 添加已跟踪的文件
gav      # git add --verbose           # 详细模式添加
```

#### 📌 提交操作
```bash
gc       # git commit --verbose        # 提交并显示详细信息
gcmsg    # git commit --message        # 快速提交消息
gca      # git commit --verbose --all  # 提交所有文件
gcam     # git commit --all --message  # 快速提交所有文件
gcan     # git commit --verbose --all --no-edit --amend  # 修正提交
gcl      # git clone --recurse-submodules  # 克隆并包含子模块
```

#### 📌 状态和日志
```bash
gst      # git status                  # 查看状态
gss      # git status --short          # 简短状态
gl       # git pull                    # 拉取
gp       # git push                    # 推送
glog     # git log --oneline --decorate --graph  # 美化日志
glg      # git log --stat              # 显示文件统计
```

#### 📌 分支操作
```bash
gb       # git branch                  # 查看分支
gba      # git branch --all            # 查看所有分支
gco      # git checkout                # 切换分支
gcb      # git checkout -b             # 创建并切换分支
gm       # git merge                   # 合并分支
gbd      # git branch --delete         # 删除分支
gbD      # git branch --delete --force # 强制删除分支
```

#### 📌 差异查看
```bash
gd       # git diff                    # 查看工作区差异
gdca     # git diff --cached           # 查看暂存区差异
gdw      # git diff --word-diff        # 单词级别差异
```

#### 📌 重置和撤销
```bash
grh      # git reset                   # 重置
grhh     # git reset --hard            # 硬重置
groh     # git reset origin/$(git_current_branch) --hard  # 重置到远程分支
gru      # git reset --                # 取消暂存
```

#### 📌 远程操作
```bash
grv      # git remote --verbose        # 查看远程仓库
gra      # git remote add              # 添加远程仓库
gfa      # git fetch --all --prune     # 获取所有远程更新
```

---

### 2. **forgit** 插件
**功能**: 提供交互式 Git 操作，使用 fzf 进行可视化选择

#### 📌 主要命令
```bash
ga       # 交互式添加文件 (git add)
glo      # 交互式查看日志 (git log)
gd       # 交互式查看差异 (git diff)
gcf      # 交互式检出文件 (git checkout)
gss      # 交互式管理 stash (git stash)
grh      # 交互式重置 HEAD (git reset)
gbd      # 交互式删除分支 (git branch -d)
gat      # 交互式查看 .gitattributes
```

#### 💡 使用示例
```bash
# 交互式添加文件（会显示文件列表供选择）
ga

# 交互式查看 git log（可搜索和预览）
glo

# 交互式查看差异（可选择文件预览差异）
gd
```

---

## 🛠️ 开发工具插件

### 3. **brew** 插件
**功能**: Homebrew 包管理器快捷命令

```bash
brewp     # brew pin                   # 锁定包版本
brews     # brew list                  # 列出已安装包
brewsp    # brew list --pinned         # 列出锁定的包
bubo      # brew update && brew outdated  # 更新并显示过期包
bubu      # brew update && brew upgrade   # 更新并升级
bubc      # brew upgrade && brew cleanup  # 升级并清理
bcubo     # brew update && brew outdated && brew upgrade && brew cleanup
```

#### 💡 使用示例
```bash
# 更新所有包
bubu

# 查看已安装的包
brews

# 清理旧版本
bubc
```

---

### 4. **node** 插件
**功能**: Node.js 相关快捷命令

```bash
# 没有特定别名，主要提供自动补全功能
node     # Node.js 解释器
npm      # 包管理器
npx      # 包执行器
```

---

### 5. **npm** 插件
**功能**: npm 包管理器快捷命令

```bash
npmg     # npm i -g                    # 全局安装
npmS     # npm i -S                    # 安装并保存到 dependencies
npmD     # npm i -D                    # 安装并保存到 devDependencies
npmE     # PATH=$(npm bin):$PATH       # 添加本地 npm bin 到 PATH
npmO     # npm outdated                # 检查过期包
npmV     # npm -v                      # 查看 npm 版本
npmL     # npm list                    # 列出已安装包
npmst    # npm start                   # 启动项目
nmt      # npm test                    # 运行测试
nmr      # npm run                     # 运行脚本
```

#### 💡 使用示例
```bash
# 全局安装包
npmg typescript

# 安装开发依赖
npmD eslint

# 运行项目
npmst
```

---

### 6. **python** 插件
**功能**: Python 相关快捷命令和自动补全

```bash
# 主要提供自动补全，没有特定别名
python   # Python 解释器
pip      # 包管理器
```

---

### 7. **pip** 插件
**功能**: Python pip 包管理器快捷命令

```bash
# 提供智能补全和一些函数
pir      # pip install -r requirements.txt  # 从文件安装
piu      # pip install --user              # 用户级安装
```

---

### 8. **docker** 插件
**功能**: Docker 容器管理快捷命令

```bash
dbl      # docker build                # 构建镜像
dcl      # docker container ls         # 列出容器
dcp      # docker container prune      # 清理容器
dcu      # docker compose up           # 启动服务
dcd      # docker compose down         # 停止服务
dex      # docker exec -it             # 进入容器
dim      # docker images               # 列出镜像
dip      # docker image prune          # 清理镜像
dlo      # docker logs                 # 查看日志
dps      # docker ps                   # 列出运行中容器
dpu      # docker pull                 # 拉取镜像
dr       # docker run                  # 运行容器
drit     # docker run -it              # 交互式运行
drm      # docker rm                   # 删除容器
drmi     # docker rmi                  # 删除镜像
dsa      # docker stop $(docker ps -q)  # 停止所有容器
dxc      # docker system prune         # 系统清理
```

#### 💡 使用示例
```bash
# 构建并运行容器
dbl -t myapp .
drit myapp bash

# 查看所有容器
dps

# 清理系统
dxc
```

---

### 9. **docker-compose** 插件
**功能**: Docker Compose 编排工具快捷命令

```bash
dcb      # docker-compose build        # 构建服务
dce      # docker-compose exec         # 在服务中执行命令
dcps     # docker-compose ps           # 查看服务状态
dcr      # docker-compose run          # 运行一次性命令
dcup     # docker-compose up           # 启动服务
dcupb    # docker-compose up --build   # 构建并启动
dcupd    # docker-compose up -d        # 后台启动
dcdn     # docker-compose down         # 停止并删除
dcl      # docker-compose logs         # 查看日志
dclf     # docker-compose logs -f      # 跟踪日志
dcpull   # docker-compose pull         # 拉取镜像
dcstart  # docker-compose start        # 启动服务
dcstop   # docker-compose stop         # 停止服务
```

#### 💡 使用示例
```bash
# 启动开发环境
dcupd

# 查看服务日志
dclf web

# 在服务中执行命令
dce web bash
```

---

### 10. **vscode** 插件
**功能**: Visual Studio Code 编辑器快捷命令

```bash
vsc      # code                        # 在 VS Code 中打开
vsc .    # code .                      # 打开当前目录
vsc file # code file                   # 打开指定文件
```

#### 💡 使用示例
```bash
# 在 VS Code 中打开当前项目
vsc .

# 打开特定文件
vsc package.json
```

---

## 🖥️ 系统增强插件

### 11. **macos** 插件
**功能**: macOS 系统特有的快捷命令

```bash
showfiles    # 显示隐藏文件
hidefiles    # 隐藏隐藏文件
spotoff      # 关闭 Spotlight 索引
spoton       # 开启 Spotlight 索引
pfd          # 在 Finder 中显示当前目录
pfs          # 在 Finder 中显示选中的文件
cdf          # cd 到最前面的 Finder 窗口路径
quick-look   # 快速预览文件
man-preview  # 在 Preview.app 中打开 man 页面
trash        # 移动文件到废纸篓
```

#### 💡 使用示例
```bash
# 显示隐藏文件
showfiles

# 在 Finder 中打开当前目录
pfd

# 快速预览文件
quick-look document.pdf
```

---

### 12. **sudo** 插件
**功能**: 快速添加 sudo 权限

#### 📌 使用方法
- **双击 ESC 键** 自动在当前命令前添加 `sudo`

#### 💡 使用示例
```bash
# 输入命令
vim /etc/hosts

# 双击 ESC，自动变成
sudo vim /etc/hosts
```

---

### 13. **colored-man-pages** 插件
**功能**: 为 man 手册页面添加颜色，提高可读性

#### 📌 效果
- man 页面会自动显示彩色文本
- 标题、选项、示例等会有不同颜色

#### 💡 使用示例
```bash
man git    # 会显示彩色的 git 手册
man ls     # 会显示彩色的 ls 手册
```

---

### 14. **command-not-found** 插件
**功能**: 当命令不存在时，提供安装建议

#### 💡 使用示例
```bash
# 输入不存在的命令
htop

# 系统会提示
# zsh: command not found: htop
# The program 'htop' is currently not installed. You can install it by typing:
# brew install htop
```

---

### 15. **dirhistory** 插件
**功能**: 使用 Alt+方向键浏览目录历史

#### 📌 快捷键
```bash
Alt + ←    # 返回上一个访问的目录
Alt + →    # 前进到下一个目录  
Alt + ↑    # 返回父目录
Alt + ↓    # 进入第一个子目录
```

#### 💡 使用场景
在多个目录间快速切换，类似浏览器的前进后退功能

---

## 📁 文件和目录操作插件

### 16. **extract** 插件
**功能**: 智能解压缩工具，支持多种格式

#### 📌 支持格式
```bash
.tar.bz2, .tar.gz, .tar.xz, .tar.Z, .tar
.tbz2, .tgz, .txz, .tZ
.bz2, .gz, .xz, .Z
.zip, .rar, .7z
.deb, .rpm
.jar, .war
```

#### 💡 使用示例
```bash
# 解压各种格式文件
extract file.zip
extract project.tar.gz  
extract software.rar
extract data.7z

# 自动识别格式并解压到当前目录
extract ~/Downloads/archive.tar.bz2
```

---

### 17. **copyfile** 插件
**功能**: 复制文件内容到剪贴板

```bash
copyfile filename    # 复制文件内容到剪贴板
```

#### 💡 使用示例
```bash
# 复制文件内容
copyfile ~/.ssh/id_rsa.pub
copyfile package.json

# 然后可以直接粘贴到其他地方
```

---

### 18. **copypath** 插件
**功能**: 复制文件或目录路径到剪贴板

```bash
copypath              # 复制当前目录路径
copypath filename     # 复制文件路径
copypath dirname      # 复制目录路径
```

#### 💡 使用示例
```bash
# 复制当前路径
copypath

# 复制文件路径
copypath important.txt

# 复制目录路径
copypath ~/Documents
```

---

### 19. **k** 插件
**功能**: 增强版 ls 命令，显示更多信息

```bash
k           # 类似 ls -la，但显示 Git 状态
k -h        # 显示隐藏文件
k -a        # 显示所有文件
```

#### 💡 特色功能
- 显示文件的 Git 状态（修改、新增、删除）
- 彩色文件类型显示
- 文件大小人性化显示
- 权限信息清晰显示

#### 💡 使用示例
```bash
# 查看当前目录（推荐替代 ls）
k

# 查看包含隐藏文件
k -h
```

---

### 20. **z** 插件
**功能**: 智能目录跳转，基于访问频率和最近访问

```bash
z dirname      # 跳转到包含 dirname 的目录
z foo bar      # 跳转到同时包含 foo 和 bar 的目录
z -l           # 列出匹配的目录
z -r           # 按访问时间排序
z -t           # 按访问频率排序
```

#### 💡 使用示例
```bash
# 跳转到项目目录
z proj        # 跳转到 ~/projects 或相似目录

# 跳转到特定项目
z myapp       # 跳转到包含 myapp 的目录

# 组合搜索
z web app     # 跳转到同时包含 web 和 app 的目录

# 查看可跳转的目录
z -l
```

---

## 🔧 实用工具插件

### 21. **web-search** 插件
**功能**: 直接从命令行搜索网络

```bash
google "搜索内容"          # Google 搜索
bing "搜索内容"            # Bing 搜索
yahoo "搜索内容"           # Yahoo 搜索
duckduckgo "搜索内容"      # DuckDuckGo 搜索
stackoverflow "问题"       # Stack Overflow 搜索
github "项目名"            # GitHub 搜索
youtube "视频"             # YouTube 搜索
map "地址"                 # Google Maps 搜索
```

#### 💡 使用示例
```bash
# 搜索技术问题
google "react hooks tutorial"
stackoverflow "python list comprehension"

# 搜索项目
github "awesome-python"

# 搜索地址
map "北京天安门"
```

---

### 22. **jsontools** 插件
**功能**: JSON 数据处理工具

```bash
pp_json             # 美化 JSON（从输入或剪贴板）
is_json            # 验证 JSON 格式
urlencode_json     # URL 编码 JSON
urldecode_json     # URL 解码 JSON
```

#### 💡 使用示例
```bash
# 美化 JSON 数据
echo '{"name":"test","value":123}' | pp_json

# 验证 JSON 格式
echo '{"valid": true}' | is_json

# 美化剪贴板中的 JSON
pp_json
```

---

### 23. **urltools** 插件
**功能**: URL 编码解码工具

```bash
urlencode "text"    # URL 编码
urldecode "text"    # URL 解码
```

#### 💡 使用示例
```bash
# URL 编码
urlencode "hello world"
# 输出: hello%20world

# URL 解码  
urldecode "hello%20world"
# 输出: hello world
```

---

### 24. **encode64** 插件
**功能**: Base64 编码解码工具

```bash
encode64 "text"     # Base64 编码
decode64 "text"     # Base64 解码
e64                 # encode64 的别名
d64                 # decode64 的别名
```

#### 💡 使用示例
```bash
# Base64 编码
encode64 "Hello World"
# 输出: SGVsbG8gV29ybGQ=

# Base64 解码
decode64 "SGVsbG8gV29ybGQ="
# 输出: Hello World
```

---

### 25. **history** 插件
**功能**: 历史命令增强功能

```bash
h              # 显示历史命令
hs "pattern"   # 搜索历史命令
hsi "pattern"  # 不区分大小写搜索历史
```

#### 💡 使用示例
```bash
# 查看历史命令
h

# 搜索包含 git 的命令
hs git

# 不区分大小写搜索
hsi DOCKER
```

---

## 🎯 自动补全和语法高亮

### 26. **zsh-completions** 插件
**功能**: 提供额外的命令自动补全功能

- 为更多命令提供 Tab 补全
- 智能参数补全
- 自动安装，无需手动操作

---

### 27. **zsh-autosuggestions** 插件
**功能**: 根据历史记录提供命令建议

#### 📌 使用方法
- 输入命令时会显示灰色的建议
- 按 **→** 键接受完整建议
- 按 **Ctrl+→** 接受单个单词
- 按 **Ctrl+E** 跳到行尾

#### 💡 配置选项
```bash
# 在 ~/.zshrc 中可以配置
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=8'  # 建议文本颜色
ZSH_AUTOSUGGEST_STRATEGY=(history completion)  # 建议策略
```

---

### 28. **zsh-syntax-highlighting** 插件
**功能**: 实时语法高亮

#### 📌 高亮效果
- 正确命令显示**绿色**
- 错误命令显示**红色**  
- 字符串显示**黄色**
- 路径显示**下划线**
- 别名显示**青色**

#### 💡 注意事项
- 必须放在插件列表的最后
- 实时高亮，输入时即可看到效果

---

## 🎉 总结

您当前的配置包含：

- **🔧 Git 工具**: `git`, `forgit`（交互式 Git 操作）
- **🛠️ 开发工具**: `brew`, `node`, `npm`, `python`, `pip`, `docker`, `docker-compose`, `vscode`
- **🖥️ 系统增强**: `macos`, `sudo`, `colored-man-pages`, `command-not-found`, `dirhistory`
- **📁 文件操作**: `extract`, `copyfile`, `copypath`, `k`, `z`
- **🔧 实用工具**: `web-search`, `jsontools`, `urltools`, `encode64`, `history`
- **🎯 智能功能**: `zsh-completions`, `zsh-autosuggestions`, `zsh-syntax-highlighting`

### 🚀 快速开始建议

1. **最常用**: `gaa`, `gcmsg`, `gp`, `gl`, `k`, `z`
2. **开发必备**: `dcu`, `dcd`, `npmst`, `vsc .`
3. **系统工具**: 双击ESC添加sudo, `extract`, `copypath`
4. **搜索工具**: `google`, `stackoverflow`, `pp_json`

---

💡 **提示**: 
- 使用 `alias` 查看所有可用别名
- 使用 `functions` 查看所有可用函数
- 定期运行 `omz update` 更新插件

**祝您使用愉快！** 🎉
