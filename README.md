# Mac 中使用小鹤双拼

## 安装 RIME

- 从 RIME 官网下载 [鼠须管](http://rime.im/)，直接双击安装。
- 通过 [Homebrew Cask](http://caskroom.io/) 安装 `brew cask install squirrel`

## 下载小鹤双拼 RIME 配置方案

从 [官方](http://flypy.ys168.com/) 下载最新版本的 '小鹤音形rime平台解决方案.zip' 或者克隆本仓库。
本仓库当前版本为 v8.3，会不定期更新。

## 配置小鹤双拼

进入鼠须管的用户设定目录，一般是 /Users/*your username*/Library/Rime。

将配置方案中的所有文件，全部拷贝到 '用户设定' 目录中。

**注意：**全部拷贝会替换默认的 default.yaml 文件，如果还想保留其他默认输入法，请编辑该文件，在`schema_list` 中添加以下两项：

```
  - schema: flypy
  - schema: flypyplus
```

## 重新部署鼠须管

然后重新部署鼠须管使小鹤双拼生效，操作键盘  control+option+`(键盘左上角 esc 下面那个键)。



## 分号引导快捷标点的使用（默认未添加）

1. 在 flypy.schema.yaml 文件内找到：

   ```
   speller:
     alphabet: 'zyxwvutsrqponmlkjihgfedcba'
     initials: 'abcdefghijklmnopqrstuvwxyz'
   ```

   在其末尾加上英文分号 `;`。

2. 在 flypy_user.txt 文件内末尾添加分号引导编码，如下

   ```
   # 分号引导编码
   ：	;
   ；	;;
   ！	;a
   %	;b
   ”	;c
   、	;d
   +	;e
   ·	;g
   ←	;o
   →	;p
   ‰	;q
   -	;r
   ……	;s
   =	;t
   ——	;v
   ？	;w
   ____	;x
   @	;y
   “	;z
   ```

3. 最后重新部署鼠须管即可，输入 `;;` 就可以输出 `；`。

