# Rust 语言基础环境配置

## 环境设置

### 安装 Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### 安装配套组件

```shell
cargo install cargo-generate
pipx install pre-commit
cargo install --locked cargo-deny
cargo install typos-cli
cargo install git-cliff
cargo install cargo-nextest --locked
```

### 安装 VSCode 插件

- crates: Rust 包管理
- Even Better TOML: TOML 文件支持
- Better Comments: 优化注释显示
- Error Lens: 错误提示优化
- GitLens: Git 增强
- Github Copilot: 代码提示
- indent-rainbow: 缩进显示优化
- Prettier - Code formatter: 代码格式化
- REST client: REST API 调试
- rust-analyzer: Rust 语言支持
- Rust Test lens: Rust 测试支持
- Rust Test Explorer: Rust 测试概览
- TODO Highlight: TODO 高亮
- vscode-icons: 图标优化
- YAML: YAML 文件支持

### 安装 cargo generate

cargo generate 是一个用于生成项目模板的工具。它可以使用已有的 github repo 作为模版生成新的项目。

```bash
# apt install pkg-config openssl libssl-dev
cargo install cargo-generate
```

新的项目会使用 `changaolin/rust_template` 模版生成基本的代码：

```bash
cargo generate changaolin/rust_template
```

### 安装 pre-commit

pre-commit 是一个代码检查工具，可以在提交代码前进行代码检查。

```bash
pipx install pre-commit
```

安装成功后运行 `pre-commit install` 即可。

### 安装 Cargo deny

Cargo deny 是一个 Cargo 插件，可以用于检查依赖的安全性。
[介绍](https://github.com/EmbarkStudios/cargo-deny)

```bash
cargo install --locked cargo-deny
cargo deny init
cargo deny check
```

### 安装 typos

typos 是一个拼写检查工具。
[介绍](https://github.com/crate-ci/typos)

```bash
cargo install typos-cli
```

### 安装 git cliff

git cliff 是一个生成 changelog 的工具。
[介绍](https://www.conventionalcommits.org/en/v1.0.0/#summary)
fix: 修复 bug
feat: 新增功能
docs: 文档更新
style: 代码格式化
refactor: 代码重构
perf: 性能优化
test: 测试
chore: 其他

```bash
cargo install git-cliff
```

### 安装 cargo nextest

cargo nextest 是一个 Rust 增强测试工具。

```bash
cargo install cargo-nextest --locked
```
