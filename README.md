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
実装リポジトリは本リポジトリには含めず、リンクで参照して管理する。

```text
VoiceNote-System/
├── README.md                 : 本ファイル（プロジェクト概要）
└── docs/
    ├── システム設計書.md      : システム設計書
    └── img/                  : 設計書で利用する画像
```

## 関連リポジトリ（リンク）

- VoiceNote-FPGA: [ここをクリック](https://github.com/kiiisy/VoiceNote-FPGA.git)
- VoiceNote-HLS: [ここをクリック](https://github.com/kiiisy/VoiceNote-HLS.git)
- VoiceNote-Ref-C: [ここをクリック](https://github.com/kiiisy/VoiceNote-Ref-C.git)
- VoiceNote-SW: [ここをクリック](https://github.com/kiiisy/VoiceNote-SW.git)
- VoiceNote-Algo: [ここをクリック](https://github.com/kiiisy/VoiceNote-Algo.git)

## ドキュメント

- 📘 [システム設計書](docs/システム設計書.md)

各実装の詳細については、上記の関連リポジトリを参照すること。

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
