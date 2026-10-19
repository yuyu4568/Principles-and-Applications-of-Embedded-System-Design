# 嵌入式系统设计原理与应用 · 课程笔记

本仓库收录课堂录音转写整理后的学习笔记，已归纳重点并扩充解析，可在手机或电脑上直接阅读。**所有课程笔记整合在同一个页面**，无需切换多个链接。

## 在线阅读

- [课程笔记（第 1–8 课 合一页）](https://yuyu4568.github.io/Principles-and-Applications-of-Embedded-System-Design/)

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `index.html` | 移动端网页，包含全部课程笔记（第 1–8 课） |
| `嵌入式系统设计原理与应用-第1课笔记.md` | 第 1 课 Markdown 笔记（扩展版） |
| `嵌入式系统设计原理与应用-第2课笔记.md` | 第 2 课 Markdown 笔记 |
| `嵌入式系统设计原理与应用-第3课笔记.md` | 第 3 课 Markdown 笔记（详细版） |
| `嵌入式系统设计原理与应用-第4课笔记.md` | 第 4 课 Markdown 笔记（详细版） |
| `嵌入式系统设计原理与应用-第5课笔记.md` | 第 5 课 Markdown 笔记（gcc 编译与 Makefile） |
| `嵌入式系统设计原理与应用-第6课笔记.md` | 第 6 课 Markdown 笔记（Samba 服务器与 Shell 编程） |
| `嵌入式系统设计原理与应用-第7课笔记.md` | 第 7 课 Markdown 笔记（条件测试与流程控制） |
| `嵌入式系统设计原理与应用-第8课笔记.md` | 第 8 课 Markdown 笔记（Linux 文件 I/O 函数，含完整可编译代码） |

## 内容概览

### 第 1 课：嵌入式系统概述与开发入门

1. 嵌入式系统的定义、特点与组成
2. ARM 与嵌入式微处理器（三种含义、IP 核、产业链、8051 背景）
3. 冯·诺依曼 vs 哈佛架构、RISC vs CISC、Cortex 三系
4. 开发流程、自顶向下/自底向上设计、交叉编译
5. VMware + Ubuntu 环境与网络模式
6. Linux 目录结构、权限与常用指令
7. 处理器分类选型、RTOS 与实时性、调试手段（扩充）
8. 应用领域、学习路线、术语表（扩充）

### 第 2 课：Linux 指令进阶

1. 用户管理：useradd / passwd / userdel / 组管理
2. 文件管理：ls / cd / touch / mkdir / cp / pwd（重中之重）
3. 绝对路径与相对路径
4. Tab 自动补齐、history 等效率技巧
5. 易错点复盘、课堂操作流程、自测题含答案

### 第 3 课：Linux 文件操作进阶（更详细）

1. mv 移动：与 cp 的区别、时间戳保留、目录无需 -r
2. rm 删除：文件/目录参数区别、-r / -f / -rf
3. 文件类型识别：ll 首字符（- / d / l / c / b / p）
4. 权限 rwx 详解：u/g/o 三组、数字换算（r=4 w=2 x=1）
5. chmod：字符方式与数字方式、教材例题（761）
6. ln 链接：硬链接 vs 软链接详细对比
7. 网络命令简介：ifconfig / ping
8. 易错点、操作复盘、自测题含答案、命令速查表

> 笔记基于课堂录音自动转写整理，已归纳重点并适当补充背景知识；原始转写可能存在口语化或同音字识别误差。

### 第 4 课：网络配置 / 压缩打包 / 进程查看 / vi 编辑器（更详细）

1. 网络配置与测试：ifconfig 查看网卡/IP/掩码、网卡 up/down、临时改 IP、桥接/NAT/仅主机、ping 连通测试
2. 压缩与打包：打包 vs 压缩的区别、tar cfv/tfv/xfv、tar czvf/xzvf（.tar.gz）、gzip 与 bzip2 对比
3. 进程查看：ps aux 查看系统进程、PID 不连续的成因
4. vi/vim 编辑器：标准/插入/底行三种模式、i/a/o 进入插入、Esc、:wq / :q! / :set nu、标准模式快捷键（0/$/G/gg/nG/dd/yy/p/u 等）
5. 作业讲评：架构组成、嵌入式定义、处理器分类与选型、冯·诺依曼 vs 哈佛
6. 易错点、操作复盘、自测题含答案

### 第 5 课：gcc 编译器与编译流程 / make 与 Makefile（更详细）

1. vi 复习：三种模式与切换规则（插入⇄底行不能直接互转）、权限、cat 查看代码
2. IDE 集成开发环境：Keil / Dev-C++ / Code::Blocks / VS Code，UI 与底层封装
3. gcc 编译器：支持 C/C++/Java、跨平台；单文件编译 `gcc hello.c -o hello`
4. 编译四阶段 ★：预处理(-E→.i) → 编译(-S→.s) → 汇编(-c→.o) → 链接(→可执行文件)
5. 多文件工程：`gcc main.c input.c add.c -o main`
6. make 与 Makefile ★：目标:依赖、Tab 缩进、M 大写、clean 目标、三大作用
7. gdb 调试了解、教材页码对照、易错点、操作复盘、自测题、命令速查表

### 第 6 课：Samba 服务器配置 / Shell 编程基础（更详细）

1. 服务器概述：TFTP / NFS（Linux 间）、Samba（Linux↔Windows）；C/S 架构
2. Samba 配置七步 ★：装包 → 建共享目录 → 建账户 → 改 smb.conf → 重启 smbd → 通网 → Windows 登录
3. Shell 概述：用户与内核的桥梁，命令解析器 + 高级程序设计语言；sh/csh/ksh/bash
4. 脚本创建与运行 ★：`#!/bin/bash`；五种执行方式（sh / ./ / source / . / bash）
5. Shell 变量 ★：命名规则、环境变量/位置参数变量/用户自定义变量、`$` 引用、赋值、expr 与 let
6. 易错点、操作复盘、自测题、命令速查表

### 第 7 课：Shell 通配符 / 条件测试 / 流程控制（更详细）

1. 课前复习：Samba 七步、Shell 概念与脚本五种运行方式
2. 通配符 ★：`*`、`?`、`[abc]`、`[!abc]`、`[a-z]`
3. 元字符与转义字符：`=`、`$`、`>`、`>>`、`<`、`&`、`\n`、`\t`、`\a`
4. 单引号 / 双引号 / 反引号 ★：全屏蔽、保留功能、命令替换
5. 条件测试 ★：`test` 与 `[ ]`；真=0、假=非0；`$?`
6. 测试分类：文件（`-f/-d/-e/-r/-w/-x`）、字符串（`-z/-n/=/!=`）、数值（`-eq/-ne/-lt/-gt`）、逻辑（`!/-a/-o`）
7. 条件语句：`if…then…fi`、`if…else…fi`、`if…elif…else…fi`
8. select 菜单与 case 多分支（`;;`、`esac`）
9. 循环 ★：for 带/不带列表、C 风格 for、while
10. break / continue、易错点、操作复盘、自测题、速查表

### 第 8 课：Linux 文件 I/O——目录操作与文件操作函数（更详细）

1. 导入 ★：硬件 IO（引脚 0/1 电平）→ 文件 IO（数据流）；输入/输出是**相对方向**
2. 文件基础回顾：`ls -l` 七字段、UGO 权限与 8421、七种文件类型、硬链接 vs 软链接（`ln` / `ln -s`）
3. 两套 API ★：标准 I/O（`fopen/fread/fwrite/fclose`）vs 文件 I/O（`open/read/write/close`）；系统级头文件 `<sys/stat.h>`、`<unistd.h>`、`<fcntl.h>`
4. 函数三要素与铁律：返回值类型 + 函数名 + 参数；**成功 0 / 失败 −1**；`errno` + `perror` + `strerror`
5. 文件描述符 `fd`（句柄）：0/1/2 被标准流占用，新文件从 3 开始
6. 目录操作 ★：`mkdir`（含 `argc/argv`）、`rmdir`（仅空目录）、`getcwd`、`opendir/readdir/closedir`（扩充）
7. `stat` / `fstat` / `lstat` ★：`struct stat` 成员表、`S_IS*` 类型判断宏
8. 文件操作 ★：`access`（0/1/2/4）、`creat`、`open`（`O_RDONLY/O_WRONLY/O_RDWR/O_CREAT/O_EXCL/O_TRUNC/O_APPEND`）、`close`、`read`、`write`、`lseek`（扩充）、`unlink`
9. 权限陷阱 ★：`umask` 削权——`0777 & ~022 = 0755`
10. 课本例题逐行解析 + 8 个完整可编译程序（mkdir / getcwd / stat / creat / 存在判断 / 读写 / 文件复制 / 目录遍历）
11. 易错点复盘、课堂操作复盘、自测题含答案、函数速查表