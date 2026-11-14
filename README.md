# ds-hello

`dspm` 示例包。安装：

```bash
./dspm install ds-hello
# 或指定版本
./dspm install ds-hello@v0.1.0
```

使用（C 驱动已原生支持 `use`）：

```ds
use hello
p(hello.hello("Ds"))
```

输出：`hello, Ds`

## 包结构

```
ds-hello/
├── ds.toml          # name/version/exports/targets
└── src/hello.ds     # exports = ["hello"] → src/hello.ds
```

## 发布自己的包

1. 建 GitHub 仓库，根目录放 `ds.toml` 与 `src/<export>.ds`；
2. 打 tag（如 `v0.1.0`）；
3. 在 [yzxcrush/ds-packages](https://github.com/yzxcrush/ds-packages) 的 `index.json` 加一行（PR）；
4. 用户运行 `dspm install <你的包名>`。
