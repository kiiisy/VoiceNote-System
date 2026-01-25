# VoiceNote-System

VoiceNote-System は、Zynq SoC（PS + PL）を題材に、
音声の録音・再生やリアルタイム処理を試しながら遊ぶ個人開発プロジェクトです。

FPGA（PL）で音声をゴリゴリ処理しつつ、
CPU（PS）側でGUIや制御を行うことで、
SoCならではのオーディオシステムを作っています。

> 本プロジェクトは個人開発のため、設計について
> 「なぜこうしたのか」「なぜ別案にしなかったのか」といったことは考えないでください。
> そのような気になった点があっても「そういうもの」として見てもらえると助かります😌

## リポジトリ構成

本リポジトリは、システム全体を統括する**親リポジトリ**として位置付ける。
実装は用途ごとにサブモジュールとして分離して管理する。

```text
VoiceNote-System/
├── README.md                  : 本ファイル（プロジェクト概要）
├── docs/
│   └── system_design.md       : システム設計書
├── VoiceNote-FPGA/            : FPGA実装
├── VoiceNote-HLS/             : HLS実装
├── VoiceNote-Ref-C/           : HLSのリファレンスC実装
├── VoiceNote-Algo/            : アルゴリズム検討
└── VoiceNote-SW/              : ソフトウェア実装
```

## ドキュメント

- 📘 システム設計書
  - docs/system_design.md

各サブモジュールの詳細については、それぞれのリポジトリを参照すること。
