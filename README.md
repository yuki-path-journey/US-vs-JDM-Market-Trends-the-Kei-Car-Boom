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
