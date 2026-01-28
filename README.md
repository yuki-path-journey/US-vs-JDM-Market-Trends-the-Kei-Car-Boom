# US-vs-JDM-Market-Trends-the-Kei-Car-Boom
「このプロジェクトでは、1.4GBの巨大な中古車データを扱う際に、以下の3つの壁にぶつかりましたが、それぞれコードで解決しました。」  Memory Wall: 全データを読み込むとメモリがパンクするため、usecols で必要な項目だけを救出。  Parsing Wall: 文末の引用符が壊れていたため、quoting=3（QUOTE_NONE）で強引に突破。  Encoding Wall: 標準のUTF-8では読み込めない特殊文字があったため、encoding='latin1' を採用。  「これらのエラーを一つずつ潰した結果、10,709台の日本車お宝データを抽出することに成功しました。」
# The Kei Car Boom Analysis (1991-1996)
今回はアメリカで急増している「軽トラ」需要を深掘りしました。 分析の結果、1991年式のホンダ・アクティが平均**1万ドル（約150万円）**近い高値で取引されていることが判明。 25年ルールを完全にクリアした個体に明確なプレミアムがついており、「法的に公道を走れること」が価値の決定打になっていることを証明しました。
<img width="883" height="553" alt="image" src="https://github.com/user-attachments/assets/cbb724b5-d235-4ad1-bac6-5c4d5985fbd4" />
<img width="1027" height="553" alt="image" src="https://github.com/user-attachments/assets/2ea04bd3-7760-4314-8158-ee9dd6b3afa4" />
<img width="863" height="553" alt="image" src="https://github.com/user-attachments/assets/6a1b5f88-5b63-4ff7-a311-75a21bdfa69c" />
# JDM Mini Truck Market Analysis (US) 

アメリカ市場における日本の軽トラ（Kei-truck）の人気を、1.4GBの膨大なデータから解き明かしました。

 分析結果のハイライト

1. 日本のメンテナンスへの絶大な信頼
走行距離が **10万マイル（約16万km）** を超えても、平均価格は **8,100ドル（約120万円）以上** を維持しています。これは、日本の車検制度や丁寧な整備が、アメリカのバイヤーから「伝説的な耐久性」として高く評価されている証拠です。

<img src="mileage_analysis.png" width="600">

2. 「働く車」から「遊ぶ車」へ：キャンパー需要の台頭
モデル名に「Camper」や「Van」の要素が含まれる車両は、標準的な軽トラよりも高い価格で取引されています。単なる農作業用としてだけでなく、DIYキャンピングカーのベース車両としての新しい価値が生まれています。

<img src="camper_analysis.png" width="600">
<img width="713" height="471" alt="image" src="https://github.com/user-attachments/assets/58b38a74-190b-41c2-b821-a9f162d04df6" />
<img width="713" height="471" alt="image" src="https://github.com/user-attachments/assets/069d39d6-a604-4ed2-91c8-9152325ad111" />

使用技術
* **Language:** Python
* **Libraries:** Pandas, Matplotlib, Seaborn
* **Dataset:** 1.4GB Raw Market Data

> **分析のこだわり:** > データの読み込みからグラフ化まで、3つのレシピ（絞り込み、グループ化、新しい情報作成）を組み合わせて分析を繰り返しました。
## 🔍 Deep Dive: Brand Value in the US
さらにデータを絞り込み、純粋な「軽トラ」のみを抽出してメーカー別に分析しました。
<img width="892" height="553" alt="image" src="https://github.com/user-attachments/assets/ace58af7-61ec-4676-b94d-a9e008a53781" />
### 🏆 Manufacturer Price Battle
アメリカ市場における平均取引価格の比較：
* **Honda (Acty): $8,368**
* **Mitsubishi (Minicab): $7,500**
<img width="859" height="548" alt="image" src="https://github.com/user-attachments/assets/498796fe-65aa-4565-a359-fc1dffcb13a1" />
## 💎 Findings: The "Diamond" in 1.4GB Data

1.4GBもの膨大な米国中古車データを解析した結果、軽トラ（Kei-truck）は非常に希少な存在であることが判明しました。

### 📊 希少な実例の抽出
数万件のデータから、執念のフィルタリングにより以下の2台を特定しました：
- **Honda Acty**: $8,368 (Average)
- **Mitsubishi Minicab**: $7,500 (Average)

### 🧐 分析の結論
一般的な米国の中古車市場（Craigslist等）において、日本産軽トラは「絶滅危惧種」レベルの希少性を持っています。このことは、軽トラが一般的な流通ルートではなく、専門のインポーター等を通じて取引されている可能性を強く示唆しています。

> **Lesson Learned**: データの量よりも、その中にある「真実」を見つけ出すプロセスの重要性を学びました。
ホンダ・アクティが三菱を抑え、高いブランド価値を維持していることが判明しました。これは、ホンダ独自のミッドシップレイアウトやエンジン性能が、アメリカのユーザーに評価されている可能性を示唆しています。

### 🧹 Data Cleaning (Noise Reduction)
今回の分析では、1.4GBの巨大データに含まれる「タンドラ」や「タコマ」といったフルサイズトラック、および「走行距離1,000万マイル」といった異常値（ノイズ）を排除し、軽トラ市場の真実を浮き彫りにしました。
### Project: US Kei Truck Market Analysis

## 📌 概要
アメリカの広大な中古車市場データから、日本の「軽トラ（Kei Truck）」がどのように流通しているかを調査・分析したプロジェクトです。
Kaggleの巨大なデータセット（約1.45GB）を扱い、データ破損によるエラーを克服して、本物の日本製軽トラのデータを抽出しました。

## 🛠️ 挑戦した課題 (Key Challenges)
このプロジェクトでは、以下の技術的な困難を乗り越えました：
1. **巨大データの処理**: 1.45GBに及ぶ巨大なCSVファイルをメモリ効率を考慮して処理。
2. **データの破損回避 (Data Salvage)**: ダウンロード失敗によりファイルの終端（EOF）が破損している状態から、`chunksize`（分割読み込み）と `Exception Handling`（例外処理）を駆使して、無事なデータのみを救出。
3. **データクリーニング**: 2,200件以上の検索結果から、メーカー名やキーワードを用いて「本物の日本製軽トラ」186台を特定。

## 📊 分析結果のハイライト
- **救出された軽トラ**: 186台
- **平均価格**: $11,301.45
- **主要生息州**: 
  1. カリフォルニア州 (CA) - 83台
  2. メイン州 (ME) - 16台
  3. コロラド州 (CO) - 15台
- **考察**: 雪国や離島（ハワイ等）では需要が高く、価格が上昇する傾向が見られました。
# 🛻 US Craigslist Kei-Truck Market Analysis
**アメリカの中古車データから探る「軽トラ」の生息調査**

## 📌 プロジェクト概要
アメリカ最大の掲示板サイト「Craigslist」の中古車データ（約42万件）を解析し、日本から輸出された希少な「軽トラ（Kei-Truck）」の市場状況を調査しました。

## 🛠️ 解決した技術的課題
このプロジェクトでは、以下のステップでデータ解析を行いました。

1. **巨大データの処理 (1.4GB Handling)**
   - Google Colab環境で1.4GB（42万行）のCSVを処理。
   - `low_memory=False` や `on_bad_lines='skip'` を活用し、メモリ制限とデータ形式の不備を克服。
2. **ターゲットの特定 (Precise Filtering)**
   - 正規表現（Regex）を用い、モデル名から `carry`, `acty`, `sambar`, `hijet` 等のキーワードで軽トラのみを抽出。
   - 426,880台の中から、精鋭の**37台**を特定。
3. **データの可視化 (Data Visualization)**
   - `Seaborn` と `Matplotlib` を使用し、メーカーシェアと全米の生息分布をグラフ化。

## 📊 分析結果のハイライト
- **最多メーカー**: **Honda (Acty)** がアメリカ市場で最もポピュラーな軽トラであることが判明。
- **生息地**: テキサス州、オレゴン州、ニュージャージー州に多く分布。
- **奇跡の1台**: アリゾナ州にて、走行距離わずか **6,766マイル** の1993年製三菱ミニキャブを発見。

## 💻 使用技術
- **Language**: Python 3.12
- **Libraries**: Pandas, Matplotlib, Seaborn
- **Environment**: Google Colab / Kaggle Notebook

## 📈 可視化グラフ
<img width="1372" height="584" alt="image" src="https://github.com/user-attachments/assets/d89adc3d-0e47-4c09-8a2e-f756e77f5d5c" />
<img width="879" height="558" alt="image" src="https://github.com/user-attachments/assets/288cc6f6-f8ff-4856-9db7-70839dd213d7" />
<img width="1442" height="584" alt="image" src="https://github.com/user-attachments/assets/972e3875-478d-4e0e-bf9f-08526ca6ae3f" />
# 🛻 JDM Kei-Truck Treasure Hunter (USA)
42万件の全米中古車リストから、25年ルールをクリアした「本物の軽トラ」を救い出すプロジェクト。

## 🔎 プロジェクトの概要
アメリカの中古車市場データ（1.4GB / 42万件）を解析し、以下の条件に合致する「お宝個体」を抽出しています。
- **純粋な日本車メーカー**: Suzuki, Daihatsu, Honda, Subaru, Mitsubishi, Mazda
- **25年ルール適合**: 1999年以前のヴィンテージ個体を優先
- **ターゲット**: 軽トラ（Acty, Hijet, Carry, Sambar, etc.）

## 🚀 技術的な挑戦（Detective Intuition）
- **データの軽量化**: 1.4GBの巨大CSVから、ノイズ（Cherokee等）を除去し、精鋭の81台までフィルタリング。
- **データクレンジング**: メーカー名やモデル名のキーワード検索による純度100%のリスト作成。
- **可視化**: Plotlyを使用した価格帯・年式の分布分析。

## 📊 現在の分析状況
- [x] 42万件からの一次抽出（JDMキーワード）
- [x] ノイズ除去とメーカー特定（Pure Kei-truck filtering）
- [ ] 全米の州別・密集地帯マップの作成
- [ ] 掘り出し物価格（$5,000以下）のトレンド分析
<img width="800" height="400" alt="newplot (4)" src="https://github.com/user-attachme<img width="800" height="400" alt="newplot (5)" src="https://github.com/user-attachments/assets/7d64df84-ea2d-4355-b778-89423170adcb" />
nts/assets/2fd4c617-855a-4780-8ae8-18cfb2c1b821" />
<img width="800" height="400" alt="newplot (4)" src="https://github.com/user-attachments/assets/8aab0e07-1c99-43f1-8930-01ec78e8a456" />

