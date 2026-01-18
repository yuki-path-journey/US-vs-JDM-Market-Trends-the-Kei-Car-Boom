# US-vs-JDM-Market-Trends-the-Kei-Car-Boom
「このプロジェクトでは、1.4GBの巨大な中古車データを扱う際に、以下の3つの壁にぶつかりましたが、それぞれコードで解決しました。」  Memory Wall: 全データを読み込むとメモリがパンクするため、usecols で必要な項目だけを救出。  Parsing Wall: 文末の引用符が壊れていたため、quoting=3（QUOTE_NONE）で強引に突破。  Encoding Wall: 標準のUTF-8では読み込めない特殊文字があったため、encoding='latin1' を採用。  「これらのエラーを一つずつ潰した結果、10,709台の日本車お宝データを抽出することに成功しました。」
