# 武经七书 · 全书研读笔记
# The Seven Military Classics — full study notes

The source layer behind the [`doctrines/wujing/`](../doctrines/wujing/) lens pack: structured study notes for **all seven classics** — per-chapter summaries (原文要点 + 白话) plus concept deep-dives (`concepts/`) for each book's load-bearing ideas.

这是 lens 包背后的**原料层**:七书逐卷研读(原文要点+白话)+ 每书核心概念的专题笔记。lens 是提炼出的作战工具;这里是完整的书。

| Folder | 书 | 卷/概念 |
|---|---|---|
| [`sunzi/`](sunzi/) | 孙子兵法 | 十三篇 + 虚实/不战而屈人之兵 等 concepts |
| [`wuzi/`](wuzi/) | 吴子 | 六篇 + 以治为胜/料敌 等 concepts |
| [`sima-fa/`](sima-fa/) | 司马法 | 五篇 + 军礼/轻重 等 concepts |
| [`wei-liao-zi/`](wei-liao-zi/) | 尉缭子 | 二十四篇选读 + 制必先定/农战 等 concepts |
| [`san-lue/`](san-lue/) | 三略 | 上中下略 + 揽英雄/柔弱胜刚强 等 concepts |
| [`liu-tao/`](liu-tao/) | 六韬 | 文武龙虎豹犬六韬 + 六守三宝/文伐十二节/王翼 等 concepts |
| [`li-wei-gong-wen-dui/`](li-wei-gong-wen-dui/) | 李卫公问对 | 上中下卷 + 奇正相变/节制之师/主客治力 等 concepts |

**How the layers relate / 两层怎么配合:** the harness only loads `doctrines/wujing/` lenses at runtime (small, trigger-indexed). When a lens fires and you want the full context, follow it back here. Contributing a new lens? Mine these notes first — the best trigger patterns usually hide in the chapter you haven't quoted yet.

**Sources / 底本:** distilled from the public-domain originals as digitized by the **Chinese Text Project / 中国哲学书电子化计划** ([ctext.org](https://ctext.org)) — each chapter file links its exact source page. Notes are original commentary, licensed CC-BY-4.0 like the rest of `doctrines/`. 经文底本均取自中国哲学书电子化计划,特此致谢。
