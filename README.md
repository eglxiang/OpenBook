【Overleaf】菜单(Menu) → Compiler 选 XeLaTeX（包内 latexmkrc 也会自动切换）；主文件 main.tex。若仍报 fandol 字体错误，说明是 pdfLaTeX 在编译，请在 Menu 里手动改为 XeLaTeX。

# 开放环境模型持续适应与演化理论 — LaTeX 工程

编译：`xelatex main.tex`（运行两次以生成目录）。需要 ctex 宏包（TeX Live / MiKTeX / Overleaf 默认自带）。
Overleaf：上传 zip，编译器选 XeLaTeX，主文件 main.tex。

结构：main.tex（总控）、preamble.tex（宏包）、chapters/ch1–ch4.tex（四章，章节顺序按前半部分 Word 版）。
正文来自前 44 页（Word 版），公式来自后 42 页（知乎截图版）逐页对照录入。

## 需要您核对的公式（已在对应 .tex 中处理，标注如下）
1. 标签平滑后的向量 [0.9, 0.033, 0.033, 0.033]（ch2，YOLOOC）——网页截图被浮层遮挡，数值是按可见部分推断的。
2. DML 中 MaxCosine / MaxNorm 的具体定义（ch1）——原文只给了 DML = λ·MaxCosine + MaxNorm，本工程未另行展开定义。
3. Purification Loss 的求和范围与归一化 N（ch4，PTTA）、总目标中的权重系数 α——截图部分被遮挡。
4. FADG 频域分解（ch4）：“其中：”之后关于 X=DFT(x)、高斯滤波 G、m1/m2、λ 的符号说明在网页版被遮挡，已留 `% TODO` 注释。
5. RAA 的 ω 采样分布（ch3）：原文只说“随机采样”，未写分布。

## 配图
- figures/ 下共 32 张图，来自网页截图版，已按 Word 版的图位和图注插入各节。
- 网页版中图片在 PDF 里被页宽裁切或分辨率较低的有：PTTA 流程图（右侧文字被截）、DEM 解耦图（仅 262×190，右侧公式被截）、HypKnowe 流形/双曲网格图（右侧被截）。这几张建议您用原图替换同名文件即可（文件名不变）。
- Word 版第 38 页的图注“动态测试时自适应”对应的图，在网页版 PDF 中没有对应图片，未插入。
- 部分图带有知乎水印。

## 未包含
- 原稿中的疑似笔误未改动（如“答题有效”“分部内”“Lanscape”等，保留原样以便您自行修订）。
