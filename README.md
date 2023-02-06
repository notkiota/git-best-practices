<p align="center" href="#"><img width="150" height="200" src="https://cdnjs.cloudflare.com/ajax/libs/twemoji/14.0.0/svg/1f423.svg" alt="ひよこ"></p>

## Gitにまつわるベストプラクティスをまとめてみたリポジトリ

リポジトリ名の通り、GitやGithubについてのベストプラクティスをまとめていきます。  
一週間に一度は草を生やすことを目標に更新します。まずはとっつきやすいように日本語で！

## どうやって更新するの？

### 1. まずはリモートリポジトリをクローン（ローカルリポジトリを作成）

```bash
git clone https://github.com/notkiota/git-best-practices.git
```

### 2. ブランチを切る

```bash
git checkout -b {BRANCH}
```

### 3. 更新したファイルをステージング

```bash
git add {MODIFIED_FILE}
```

### 4. ステージングしたファイルをコミット

```bash
git commit -m "{MESSAGGE}"
```

### 5. コミットしたファイルをリモートリポジトリにプル

```bash
git push origin {BRANCH}
```

## 更新する時のルール

1. ファイルを更新する時は **必ず** ブランチを切る 
2. ブランチ名には **必ず** プレフィックスをつける
3. あるひとつの対応にあたりコミットをまとめる
4. コミットメッセージには **必ず** プレフィックスをつける
5. プルする時はプルリクエストを作成する

## 分かりやすいブランチ名とコミットメッセージをつけよう！

### プレフィックス

| プレフィックス | 内容 |
| :- | :- |
| `feat` | 新機能 |
| `fix` | バグの修正 |
| `docs` | ドキュメントのみの変更 |
| `style` | コードの動作に影響しない、見た目だけの変更<br>（スペース、フォーマット、欠落の修正、セミコロンなど） |
| `refactor` | バグの修正や機能の追加ではないコードの変更 |
| `perf` | パフォーマンスを向上させるコードの変更 |
| `test` | 不足しているテストの追加や既存のテストの修正 |
| `chore` | ビルドプロセスやドキュメント生成などの補助ツールやライブラリの変更 |

### 例：ブランチ名

| ブランチ名 | 内容 |
| :- | :- |
| `feat/show-current-date` | 今日の日付を表示する機能を追加 |
| `fix/show-current-date` | 今日の日付を表示する機能を修正 |
| `docs/add-read-me` | `README.md`を追加 |
| `style/main-py` | `main.py`のフォーマットを修正 |
| `refactor/is-holiday` | 休日か判定する機能をリファクタリング |
| `perf/is-holiday` | 休日か判定する機能を修正 |
| `test/get-prime-numbers` | 素数を取得する機能にテストコードを追加 |
| `chore/github-workflow` | GitHub Actionsのフローを修正 |

### 例：コミットメッセージ

| コミットメッセージ | 内容 |
| :- | :- |
| `feat:今日の日付を表示する機能を追加` | 今日の日付を表示する機能を追加 |
| `fix:関数内で使用している外部モジュールにセキュリティ上の問題が発生したため代替モジュールに入れ替え` | 今日の日付を表示する機能を修正 |
| `docs:README.mdを追加` | `README.md`を追加 |
| `style:main.py内の不要なブランクを削除` | `main.py`のフォーマットを修正 |
| `refactor:外部モジュールAをBに変更` | 休日か判定する機能をリファクタリング |
| `perf:関数内で新規にリストを作成せず引数で受け取った辞書を更新するよう修正` | 休日か判定する機能を修正 |
| `test:素数を取得する関数の返り値がタプル型であるかテストする` | 素数を取得する機能にテストコードを追加 |
| `chore:checkoutのバージョンをv2に修正` | GitHub Actionsのフローを修正 |
