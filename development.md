---
title: ローカルでの開発
---

## 環境のセットアップ

__注意: コピペする際も一行ずつ実行すること！__

### Gitのセットアップ

1. Git for Windowsをインストール
2. Git bashを起動
3. `ssh-keygen -t rsa -C "your.email@example.com" -b 4096`
4. `C:/Users/ユーザー名/.sshにあるid_rsa.pub`を  https://github.com/settings/keys にコピー (SSH Keys)

```
sudo gem install bundler
git clone git@github.com:tsugumi-guild/tsugumi-guild.github.io
cd tsugumi-guild.github.io
bundle install
```

## プレビュー

```
bundle exec jekyll serve
```

http://localhost:4000/　にアクセスすると、アップロードすることなく手元で変更内容を確認できる。

## 変更をアップロード

```
git add .
git commit
git push
```

## 編集するファイル

* `_layouts/default.html`: HTMLのテンプレート。大胆にレイアウトを変えたりJavaScriptを埋め込んだりできる。
* `assets/css/style.css`: スタイルシート。CSSを拡張したSassで記述されている。余白や色など細かいデザインはこちらで。
