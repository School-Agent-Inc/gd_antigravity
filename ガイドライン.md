# 貢献ガイドライン (Contributing Guidelines)

GoogleAntigravityプロジェクトへようこそ！
ここでは、このレポジトリへの参加方法やファイルを更新する手順（プルリクエストの送り方）について解説します。
**GoogleAntigravity上で行うことを前提とした説明です。**
　
## 🔰 参加の基本ルール

1. **誰でも歓迎**: アイデアひとつ、誤字修正ひとつからでも大歓迎です。
2. **安全第一**: `main` ブランチへの直接書き込みはできません。必ず新しいブランチを作って作業し、プルリクエストを送ってください。
3. **日本語OK**: コミットメッセージやプルリクエストの説明は日本語で構いません。
　
　
## 📝 参加ステップ (Pull Requestの流れ)
　
Git/GitHubに慣れていない方は、以下の手順を参考にしてください。
<img width="2816" height="1536" alt="Gemini_Generated_Image_83539l83539l8353" src="https://github.com/user-attachments/assets/7e8d76f0-2900-4806-aea0-d2abc5d24446" />
<br>
　
### Step 1: 準備 (1:Fork & 2:Clone & 3:Branch)

まず、GitHub上でレポジトリを自分のアカウントにコピー（Fork）し、それを手元に持ってきます。

1. GitHubで [School-Agent-Inc/gd_antigravity](https://github.com/School-Agent-Inc/gd_antigravity) を開きます。
2. 画面右上の **「Fork」** ボタンを押して、自分のアカウントにコピーを作成します。

**以下をコピーして、GoogleAntigravityのAgentに入力。**
<br>※ `<あなたのGitHubユーザー名>` の部分は自分のユーザー名に書き換えてください。<br>
<img width="284" height="150" alt="スクリーンショット 2026-01-08 22 50 52" src="https://github.com/user-attachments/assets/de9d663d-fe33-43f6-b9e0-cc1f28627945" />

```bash
# フォークした自分のレポジトリをクローン（最初の1回だけ）

# SSHの設定が済んでいる方
git clone git@github.com:<あなたのGitHubユーザー名>/gd_antigravity.git

# うまくいかない場合（HTTPS）
git clone https://github.com:<あなたのGitHubユーザー名>/gd_antigravity.git

cd gd_antigravity
```

**作業用ブランチの名前だけを変更して実行。**

> 💡 **ポイント**: 久しぶりに作業するときは、GitHubの自分のページで **[Sync fork]** を押してから `git pull` しましょう。

```bash
# 最新の状態にする
git checkout main
git pull origin main

# 作業用ブランチを作成（名前はわかりやすく。例: feature/add-new-idea）
git checkout -b feature/your-branch-name
```

<br><br>
### Step 2: いろいろ作業
アプリ作ったり<br>
プロンプトをmdファイル書いたり<br>
、、、、いろいろ<br>
　<br>
### Step 3: アップ前のセキュリティチェック
以下をコピーして、GoogleAntigravityのAgentに貼り付けて、リクエスト前にチェックしよう。

```bash
作成したファイルに対して以下の内容を確認し、厳密にチェックを行なってください。
含まれている場合は、GitHubにリクエストを送ってはいけません。

### 🔐 絶対に含めてはいけないもの

| 種類 | 例 | なぜダメ？ |
| :--- | :--- | :--- |
| **APIキー・シークレット** | `sk-xxxx...`, `OPENAI_API_KEY=...` | 悪意ある人に悪用され、高額請求される恐れがあります |
| **パスワード** | ログイン情報、データベースのパスワード | アカウントを乗っ取られる危険があります |
| **個人情報** | 本名、住所、電話番号、メールアドレス | プライバシーの侵害、詐欺に使われる恐れがあります |
| **認証トークン** | アクセストークン、リフレッシュトークン | あなたになりすましてサービスを使われてしまいます |
| **秘密鍵・証明書** | `.pem`, `.key` ファイル、SSH鍵 | サーバーやアカウントへの不正アクセスを許してしまいます |

### ✅ 投稿前チェックリスト

- [ ] コードに API キーやパスワードがハードコーディングされていないか？
- [ ] 設定ファイル（`.env` など）が含まれていないか？
- [ ] スクリーンショットに個人情報が映り込んでいないか？
- [ ] サンプルデータに実在の人物情報が含まれていないか？

```


### Step 4: 作業の保存と提出  (4:Commit & 5:Push & 6:Pull request)


作成・編集・セキュリティチェックが終わったら、以下の手順で変更をGitHubに送り、最後にプルリクエスト（提出依頼）を出しましょう。

1. 変更を保存して送る
　
以下をコピーして、GoogleAntigravityのAgentに入力。
**作業用ブランチの名前だけを変更して実行。**

```bash

# 1. 変更したファイルを準備する（カバンに詰めるイメージ）
git add .

# 2. 変更内容にメッセージをつけて保存する（ラベルを貼るイメージ）
git commit -m "〇〇の機能を追加"

# 3. GitHub上の自分のブランチ（Fork先）へ送信する（発送するイメージ）
git push origin feature/your-branch-name
```

2. GitHubで「マージ依頼」を出す
ブラウザで **自分のフォークしたリポジトリ** (`https://github.com/<あなた>/gd_antigravity`) を開くと、**「Compare & pull request」** というボタンが表示されます。

ボタンを押して、変更内容を確認します。
送り先（base repository）が `School-Agent-Inc/gd_antigravity` になっていることを確認して、「Create pull request」 をクリックして完了です！

## 📂 どこに何を入れる？

- 具体的なプロジェクトのファイル → `projects/`
- ふと思いついたアイデア → `ideas/`
- 共有したい資料 → `resources/`

迷ったら `ideas/` に入れておけばOKです！

---
困ったことがあれば、Gemini DIVEのチャットで気軽に質問してください。
Let's build something great together!
