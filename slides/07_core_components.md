# 07. コアコンポーネント要約（Practice）

---

## 💡 主要コンポーネント

1. **Entity: User**
    - ドメインの振る舞いと状態を一括管理
```php
   class User {
     private UserId $id;
     private Email $email;

     public function changeEmail(Email $newEmail): void {
       $this->email = $newEmail;
     }
   }
````
2. **Value Object: Email**
    - メールアドレスの妥当性を保証し、不変性を担保
```php
class Email {
  private string $address;
  public function __construct(string $address) { /* バリデーション */ }
  public function getAddress(): string { return $this->address; }
}
```
2. **Use Case: ChangeUserEmail**
    - ユースケース毎に処理を分離し、テストしやすい設計


```php
class ChangeUserEmail {
  public function execute(string $userId, string $newEmail): void {
    // リポジトリ取得 → ドメイン操作 → 保存
  }
}
```


[README.md](../README.md)<br>
[06_simple_structure.md](./06_simple_structure.md)<br>
[08_tips_for_beginners.md](./08_tips_for_beginners.md)<br>
