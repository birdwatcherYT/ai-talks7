```mermaid
graph LR
  subgraph データ保存時
    data(データ発生)--**加工処理**--> DB
  end
  subgraph データ取得時
     input(入力)--**検索クエリ**--> DB
     input-->LLM
     DB--検索結果-->
     LLM--応答-->USER
  end
```
