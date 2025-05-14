# 06. シンプル構成と各層役割（Practice）


## 🗂️ シンプル推奨構成
```
src/
├── Application/    # ユースケース
├── Domain/         # ビジネスルール
├── Infrastructure/ # 永続化・外部連携
└── Presentation/   # UI・API窓口

```


## 🔍 各層の一言役割

- **Presentation**：ユーザー／外部との入出力
- **Application**：ユースケース実行のオーケストレーション
- **Domain**：エンティティ・VO でビジネスロジック定義
- **Infrastructure**：データ永続化や外部 API 呼び出しを隠蔽



> シンプルに層分けすることで、変更影響を最小化し、テストしやすい設計を実現します。

[README.md](../README.md)<br>
[05_pros_and_cons.md](./05_pros_and_cons.md)<br>
[07_core_components.md](./07_core_components.md)<br>
