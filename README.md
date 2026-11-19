# input-pinyin-data

[Input 输入法](https://milletcode.com) 拼音词库数据仓库。按开源协议要求本仓库公开，
**构建产物不进 git**：`.github/workflows/build.yml` 每次运行从上游拉取源文件打包，
以固定 tag `data` 的 Release 附件分发。

- 上游源：[fcitx5-android/prebuilt](https://github.com/fcitx5-android/prebuilt) 仓库
  `libime/data/`（上游 libime 官方构建产物）
- 产物：`pinyin-dict.tar.bz2`（顶层含 `sc.dict` + `zh_CN.lm` 两文件）
- 稳定下载地址：
  `https://github.com/milletcode/input-pinyin-data/releases/download/data/pinyin-dict.tar.bz2`
- tar 固定 mtime/属主/排序，同样输入产出相同 sha256，App 端清单校验哈希可长期不变

触发方式：push 到 main 自动构建；也可在 Actions 页面手动 Run workflow。
产物 sha256 / 体积见每次运行 Summary。
