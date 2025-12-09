# Robotics Rigid Body Mechanics

机器人刚体力学讲义，涵盖机器人学中刚体运动与动力学的核心理论。

## 内容

- 旋转与姿态表示（Rotation）
- 螺旋理论（Screw Theory）
- 刚体动力学（Dynamics）
- 多体系统（Multibody Systems）

## 构建 PDF

### 依赖

需要安装 TeX 发行版（如 TeX Live 或 MiKTeX）。

**Ubuntu/Debian:**

```bash
sudo apt install texlive-xetex texlive-lang-chinese texlive-lang-greek texlive-latex-extra texlive-science texlive-pictures
```

**macOS (Homebrew):**

```bash
brew install --cask basictex
sudo tlmgr update --self
sudo tlmgr install ctex standalone mathtools textgreek greek-fontenc fancyhdr footmisc enumitem cbfonts
```

### 编译

使用 `xelatex` 编译（需要编译两次以生成目录）：

```bash
xelatex main.tex
xelatex main.tex
```

或使用 `latexmk` 自动处理多次编译：

```bash
latexmk -xelatex main.tex
```

编译成功后会生成 `main.pdf`。

## 目录结构

```
.
├── main.tex          # 主文档
├── sections/         # 各章节内容
│   ├── cover.tex     # 封面
│   ├── foreword.tex  # 前言
│   ├── intro.tex     # 简介
│   ├── rotation.tex  # 旋转
│   ├── screw.tex     # 螺旋理论
│   ├── dynamics.tex  # 动力学
│   └── multibody.tex # 多体系统
└── images/           # 图片资源
```

## License

MIT
