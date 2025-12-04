# OKN 同心円トレーニング

<p align="center">
  <img src="FNT512.png" alt="FNT Logo" width="120">
</p>

<p align="center">
  <strong>Functional Neuro Training</strong><br>
  同心円オプティックフローによる視覚-前庭統合トレーニング
</p>

<p align="center">
  <a href="#特徴">特徴</a> •
  <a href="#神経科学的背景">神経科学的背景</a> •
  <a href="#臨床応用">臨床応用</a> •
  <a href="#使用方法">使用方法</a> •
  <a href="#インストール">インストール</a>
</p>

---

## 概要

同心円パターンのオプティックフロー刺激を用いた、視運動性眼振（OKN）と姿勢制御のトレーニングアプリケーションです。PWA（Progressive Web App）として設計されており、オフラインでも動作します。

## 特徴

- 🎯 **収束型・発散型・交互モード** - 目的に応じた刺激パターン選択
- ⚡ **完全オフライン対応** - 一度インストールすればネット不要
- 📱 **クロスプラットフォーム** - iOS / Android / PC対応
- 🎨 **カスタマイズ可能** - 速度、リング数、カラーモード、太さを調整
- ⏱️ **タイマー機能** - 30秒〜5分、または無制限
- 🔴 **中心注視点** - 視線固定のガイド表示

---

## 神経科学的背景

### 🧠 オプティックフローと脳

同心円パターンは**背側視覚経路（MT/MST野）**を活性化し、前庭-視覚-体性感覚の統合を促進します。

### ▶ 発散型（Outward）= 前進の視覚体験

強い自己運動感（vection）を誘発し、**姿勢安定性が向上**します。人は前方への運動を日常的に経験するため、発散型刺激に対して前庭-視覚統合が最適化されています。

> Nooij, S. A., et al. (2018). Vection and postural stability

### ◀ 収束型（Inward）= 後退の視覚体験

体が"後ろに引かれる"感覚により、**姿勢揺動が増加**します。後退運動の経験が乏しいため、重力方向の内部モデルが不確実になります。

> Sukkar, G., et al. (2024). Postural responses to optic flow

### ⚖️ 重力参照の再キャリブレーション

視覚運動刺激の方向が、重力ベクトルの信頼度と重みづけを変化させます。これは**「重力知覚の運動方向依存性（directional anisotropy in gravity perception）」**と呼ばれる現象です。

> Ward, B. K., et al. (2017). Gravity perception and vestibular function

---

## 臨床応用

| 刺激タイプ | 推奨対象 | 期待される効果 |
|:---:|:---|:---|
| 🔴 **収束型** | 前傾姿勢が強い・背側筋群が硬い方 | 後方重心の再学習、体幹伸展促通 |
| 🟢 **発散型** | 後傾姿勢・過伸展傾向の方 | 前方重心の安定促進、前庭-視覚協調改善 |
| 🟡 **交互** | バランス訓練全般 | 重力参照の柔軟性向上（reweighting training） |

---

## 使用方法

### 基本操作

1. **メニューボタン** をタップして設定画面を開く
2. パターン方向、速度、リング数などを設定
3. **トレーニング開始** をタップ
4. カウントダウン後、トレーニングスタート
5. **反転ボタン** で方向を即座に切り替え可能
6. **停止ボタン** または設定時間経過で終了

### 設定項目

| 項目 | 選択肢 |
|:---|:---|
| パターン方向 | 収束型 / 発散型 / 交互 |
| 速度 | ゆっくり / 普通 / 速い / とても速い |
| リング数 | 8 / 12 / 16 / 20本 |
| カラーモード | モノクロ / グラデーション / レインボー / 高コントラスト |
| トレーニング時間 | 30秒 / 1分 / 2分 / 3分 / 5分 / 無制限 |
| 注視点 | 表示 / 非表示 |
| リングの太さ | 20% 〜 100% |

### キーボードショートカット（PC）

| キー | 動作 |
|:---:|:---|
| `Space` | 方向を反転 |
| `Esc` | トレーニング停止 |

---

## インストール

### GitHub Pagesでホスティング

1. このリポジトリをフォークまたはクローン
2. 以下のファイルをアップロード:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `FNT512.png`（白背景ロゴ）
   - `FNT512-transparent.png`（透明背景ロゴ）
3. Settings → Pages → Source: `main` branch を選択
4. 公開URLにアクセス

### ホーム画面への追加

#### iOS (Safari)
1. Safariでアプリを開く
2. 共有ボタン（□↑）をタップ
3. 「ホーム画面に追加」を選択

#### Android (Chrome)
1. Chromeでアプリを開く
2. メニュー（⋮）→「ホーム画面に追加」
3. または表示されるインストールバナーをタップ

#### PC (Chrome/Edge)
1. ブラウザでアプリを開く
2. アドレスバーのインストールアイコンをクリック
3. 「インストール」を選択

---

## ファイル構成

```
okn-concentric/
├── index.html          # メインアプリケーション
├── manifest.json       # PWAマニフェスト
├── sw.js              # Service Worker（オフライン対応）
├── FNT512.png         # ロゴ（白背景）
├── FNT512-transparent.png  # ロゴ（透明背景）
└── README.md          # このファイル
```

---

## 技術仕様

- **フレームワーク**: Vanilla JavaScript（依存関係なし）
- **描画**: HTML5 Canvas API
- **PWA**: Service Worker + Web App Manifest
- **対応ブラウザ**: Chrome, Safari, Firefox, Edge, Samsung Browser

---

## 参考文献

1. Nooij, S. A., et al. (2018). Vection is the main contributor to motion sickness induced by visual yaw rotation. *PLOS ONE*.
2. Sukkar, G., et al. (2024). Effects of optic flow direction on postural control. *Gait & Posture*.
3. Ward, B. K., et al. (2017). Vestibular stimulation and gravity perception. *Journal of Neurophysiology*.

---

## ライセンス

© 2024 Functional Neuro Training. All rights reserved.

---

<p align="center">
  <strong>Functional Neuro Training</strong><br>
  科学に基づいた神経トレーニング
</p>
