# nf-journal

KaiRA（京都大学人工知能研究会）が京都大学11月祭にて販売した会誌のソースコードレポジトリです。

## 概要

このリポジトリには、KaiRAが毎年11月祭で発行・販売している会誌のLaTeXソースコードが含まれています。各年の会誌には、サークルメンバーが取り組んだ機械学習・AI関連のプロジェクトや研究成果がまとめられています。

## ディレクトリ構成

```
nf-journal/
├── 2024/          # 2024年版会誌（vol.8）
│   ├── nf2024.tex      # メインファイル
│   ├── Makefile        # ビルド用Makefile
│   ├── cover.png       # 表紙画像
│   ├── introduction.tex
│   └── [各章のディレクトリ]/
├── 2025/          # 2025年版会誌（vol.9）
│   ├── nf2025.tex      # メインファイル
│   ├── Makefile        # ビルド用Makefile
│   ├── cover.png       # 表紙画像
│   ├── introduction.tex
│   └── [各章のディレクトリ]/
├── LICENSE        # ライセンス情報（Unlicense）
└── README.md      # このファイル
```

## 収録内容

### 2024年版（vol.8）

1. カメラ入力を用いた強化学習によるライントレーサの実現
2. 目線で操るマウスカーソル
3. KaiRAくんを動かそう
4. 最強じゃんけんAI
5. 京大シラバス検索RAGシステム - システム概要編
6. 京大シラバス検索RAGシステム - 検索手法編
7. お絵描き予測AI

### 2025年版（vol.9）

1. ニューラルネットワーク入門
2. 画像生成入門
3. 事前学習済みTransformerを用いた化学反応収率のベイズ最適化
4. Agenticな京大シラバス検索・時間割作成システム
5. 音楽と自然言語の類似度測定システムの開発
6. 顔認識で操作するゲーム
7. 歩くKaiRA君：強化学習を用いた二足歩行ロボットの歩行制御

## ビルド方法

### 必要な環境

- TeX Live または W32TeX などのLaTeX環境
- 2024年版: `platex`, `pbibtex`, `dvipdfmx`
- 2025年版: `uplatex`, `upbibtex`, `dvipdfmx`

### ビルド手順

#### 2024年版をビルドする場合

```bash
cd 2024
make compile
```

または手動で：

```bash
cd 2024
platex nf2024.tex
pbibtex nf2024
platex nf2024.tex
platex nf2024.tex
dvipdfmx nf2024.dvi
```

#### 2025年版をビルドする場合

```bash
cd 2025
make compile
```

または手動で：

```bash
cd 2025
uplatex nf2025.tex
upbibtex nf2025
uplatex nf2025.tex
uplatex nf2025.tex
dvipdfmx nf2025.dvi
```

#### クリーンアップ

2025年版では、生成されたファイルを削除するためのターゲットが用意されています：

```bash
cd 2025
make clean
```

## ライセンス

このプロジェクトは[Unlicense](LICENSE)の下で公開されています。パブリックドメインとして自由に利用できます。

## 京都大学人工知能研究会 KaiRA について

- **公式サイト**: https://kyoto-kaira.github.io/
- **メールアドレス**: kyoto.kaira@gmail.com
- **X (旧Twitter)**: https://x.com/kyoto_kaira
- **活動内容**: 機械学習に関する本の輪読会、コード読み・実装会、Kaggleへの参加など
- **入会資格**: 大学、学部、回生問わず、AIに興味がある方（会費無料）

## お問い合わせ

会誌の内容やサークルに関するお問い合わせは、上記の連絡先までお願いします。
