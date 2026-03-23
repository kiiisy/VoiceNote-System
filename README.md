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

- 📘 [システム設計書](docs/システム設計書.md)

各サブモジュールの詳細については、それぞれのリポジトリを参照すること。

## Push / PR ルール

GitHub Actionsを利用しているため、`main` へは直接pushせず、作業ブランチ経由でPull Requestを作成してください。

### 基本ルール

1. `main` から作業ブランチを作成する
2. 作業ブランチに commit / push する
3. Pull Request を作成する
4. GitHub Actions が成功してからレビュー・マージする
5. `main` への直接 push は行わない

### 推奨手順

```bash
# main を最新化
git checkout main
git pull origin main

# 作業ブランチ作成
git checkout -b dev-tmp

# 変更をコミット
git add .
git commit -m "chore: add push and PR workflow"

# リモートへ push
git push -u origin dev-tmp
```
