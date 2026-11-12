# IE5202 — Applied Forecasting Methods · Quiz 2

Independent student revision notes for Lectures 7–12: regression on time, exponential smoothing, ARMA, ARIMA/SARIMA, RNN/LSTM/GRU, attention, Transformers and related sequence models.

## Download and source

- [Download the public revision PDF](IE5202-Quiz2-Review-Public.pdf)
- [XeLaTeX source](main.tex)
- [Six independently generated ACF/PACF practice figures](figures/)
- [Build status and compiled artifacts](https://github.com/nkuwyk/NUS-ISE-Study-Notes/actions/workflows/build-latex.yml)

The public edition retains formulas, explanations, six ACF/PACF practice plots, ten independent worked exercises and an English–Chinese glossary. Teacher slide images and official assessment wording are excluded. Some explanations refer to course examples whose figures have been omitted. This is a study aid, not a complete substitute for authorized course materials.

## Reproduce the PDF

Compile from **this directory**, so that relative `figures/` paths resolve:

```bash
latexmk -xelatex -interaction=nonstopmode -halt-on-error -jobname=IE5202-Quiz2-Review-Public main.tex
```

Alternatively run XeLaTeX with the same job name until cross-references and the contents page stabilize (usually three passes on a clean build). On Overleaf, upload this directory with `figures/`, select `main.tex`, and choose XeLaTeX. Overleaf normally names the result `main.pdf`.

Ubuntu dependencies:

```bash
sudo apt-get install latexmk texlive-xetex texlive-lang-chinese texlive-latex-extra fonts-noto-core fonts-noto-mono
```

The source uses Noto Serif, Noto Sans, Noto Sans Mono and the TeX Live Fandol Chinese font set. The six PNG files are versioned source assets, not remotely linked images. Their original simulation-generation script is not available in this edition; the PDF can be rebuilt from the tracked assets, but regenerating the plots from simulated data is not yet supported.

## Automatic builds

The [XeLaTeX workflow](https://github.com/nkuwyk/NUS-ISE-Study-Notes/blob/main/.github/workflows/build-latex.yml) runs when source, figures or the workflow change, on relevant pull requests, and through **Actions → Build IE5202 revision PDF → Run workflow**. It runs latexmk until references stabilize and keeps a PDF artifact for 30 days. Successful main-branch builds also commit the PDF here, keeping the download link current. Pull requests compile without publishing a PDF commit. If repository policy blocks bot pushes, the build artifact remains available and the publish step reports a failure.

## Rights, academic integrity and contact

This is an independent, non-commercial student initiative, not an official NUS resource or an instructor-endorsed guide. Do not redistribute the personal edition, official slides or protected assessments without permission. Educational or non-commercial intent does not itself grant third-party permissions. Follow current course rules and verify formulas against authorized materials. Errors and changes in course coverage are possible.

Corrections or rights concerns: open an Issue or email **nkuwyk@gmail.com**.

---

# IE5202 Quiz 2 复习资料

学生独立整理的 Lecture 7–12 复习笔记，涵盖时间回归、指数平滑、ARMA、ARIMA/SARIMA、RNN/LSTM/GRU、Attention、Transformer 等。

## 下载与源码

- [公开版 PDF](IE5202-Quiz2-Review-Public.pdf)
- [LaTeX 源码](main.tex)
- [六张原创 ACF/PACF 练习图](figures/)
- [自动编译状态与构建产物](https://github.com/nkuwyk/NUS-ISE-Study-Notes/actions/workflows/build-latex.yml)

保留公式、中文解释、六道识图练习、十道独立编写的计算与概念练习，以及中英文术语表；移除了教师课件原图与官方试题原文。部分课堂案例仍保留文字说明，配图已省略。公开版不能替代获得授权的完整课程资料。

## 编译与维护

在本目录执行上方 `latexmk` 命令。首次编译应运行至目录和交叉引用稳定，通常需要三遍 XeLaTeX。Overleaf 上传本目录及 `figures/`，选择 `main.tex` 和 XeLaTeX 即可。字体和 Ubuntu 依赖见上方说明。

六张 PNG 为仓库内固定配图资源；当前没有原始模拟绘图脚本，因此能够从源码和图片重建 PDF，尚不能从模拟数据重新生成相同图片。

修改源码、图片或工作流后，GitHub Actions 自动编译；也可在 Actions 中手动运行。main 分支构建成功后自动更新本目录 PDF，构建产物另保留 30 天。PR 只编译验证，不自动发布。若仓库策略阻止机器人推送，可下载构建产物并查看发布步骤报错。

## 声明与联系

非官方、非商业的学生学习项目，不代表 NUS 或任课教师。请勿未经许可传播个人版、官方课件或受保护的试题；教育用途与非商业声明不等于版权授权。请遵守当期课程学术诚信规定，以获授权课程资料核验知识点。

纠错及版权反馈：提交 Issue 或联系 **nkuwyk@gmail.com**。
