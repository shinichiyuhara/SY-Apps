# Privacy Policy — Pinakeion

Last updated: 2026-05-24

## English

Pinakeion ("the app") does not collect, transmit, or share any
personal information.

### What we don't collect

- We do not collect any personal data.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not establish network connections.
- We do not track your reading habits or files.

### What is stored locally

Stored only on your Mac (UserDefaults, the app's local SQLite catalogue, or
its Caches / Logs directories):

- **Library paths**: folder paths you registered as Libraries, plus the
  security-scoped bookmarks needed to re-open them across sessions.
- **File Access grants**: broad sandbox bookmarks for your home folder
  or external volumes that you authorised in Settings → File Access.
- **File metadata**: filenames, file sizes, modification dates, added
  dates, relative folder paths inside each Library, parsed titles /
  author names inferred from filenames, image count per archive,
  format kind (archive or loose image).
- **Per-archive state**: favourites, ratings, read / unread status
  with finish timestamp, last-read page index.
- **Optional usage statistics** (on by default; toggle from Settings →
  Diagnostics → Usage Statistics): open count, last-opened timestamp,
  total reading time per archive — drives the Recently Opened and
  Most Opened smart folders.
- **Optional diagnostic log** (off by default; toggle from Settings →
  Diagnostics → Log): written to `~/Library/Logs/Pinakeion/`,
  auto-rotated at 5 MB with one backup kept.
- **Cover thumbnails**: JPEG cache under
  `~/Library/Caches/Pinakeion/thumbnails/`.
- **Quick Preview cache**: 5×4 page grid renders under
  `~/Library/Caches/Pinakeion/previews/`, capped at 500 MB with
  oldest entries evicted first.
- **Search index**: FTS5 trigram index over filenames / parsed titles
  / parsed authors. Derived from the file metadata above; kept inside
  the local SQLite catalogue; never sent anywhere.
- **Preferences**: view mode, sort field / direction, tile width,
  sidebar / inspector / folder browser visibility. Stored in macOS
  UserDefaults + the local catalogue.

### What we used to do — but no longer

Earlier preview builds (pre-v0.9.2) experimented with a sister-app
integration that imported read progress from a separate reader via a
shared App Group container. That integration has been removed
entirely in v0.9.2 — Pinakeion no longer reads from any App Group,
no longer reads any other app's database, and ships with no entitlement
to do so.

### Clearing data

- Settings → Privacy → **Delete All Personal Data** wipes the
  catalogue, thumbnails, preview cache, preferences, and the
  diagnostic log directory in one step.
- Settings → Thumbnails → **Clear All Thumbnails** wipes only the
  thumbnail cache.
- Settings → Thumbnails → **Clear Preview Cache** wipes only the
  Quick Preview page cache.
- Settings → Diagnostics → **Clear Logs** wipes only the diagnostic
  log directory.

### Children

The app is suitable for ages 4+ and contains no advertising, no in-app
purchases, and no links to external services.

### Contact

Questions or concerns: shinichiyuhara1@gmail.com

## 日本語

Pinakeion (「本アプリ」) は個人情報を一切収集・送信・共有しません。

### 収集しないもの

- 個人情報は収集しません。
- 解析サービス、クラッシュレポートサービス、広告 SDK は使用しません。
- ネットワーク接続を確立しません。
- 閲覧履歴やファイルを追跡しません。

### ローカルに保存されるもの

下記はあなたの Mac (UserDefaults / ローカル SQLite カタログ /
Caches・Logs ディレクトリ) にのみ保存されます:

- **Library パス**: Library として登録したフォルダパスおよび
  セッションをまたいで再アクセスするための security-scoped bookmark。
- **File Access 許可**: 設定 → ファイルアクセス で承認した
  ホームフォルダや外部ボリュームへの広域 sandbox bookmark。
- **ファイルメタデータ**: ファイル名、サイズ、更新日時、追加日時、
  Library 内の相対フォルダパス、ファイル名から推測したタイトル /
  著者、各アーカイブの画像枚数、フォーマット種別 (アーカイブ / 画像)。
- **アーカイブ毎の状態**: お気に入り、評価、既読 / 未読フラグと
  読了タイムスタンプ、最後に開いたページ。
- **任意の利用統計** (既定 ON、設定 → 診断 → 利用統計 で切替):
  各アーカイブの開閉回数、最終アクセス時刻、合計閲覧時間。
  「最近開いた」「よく開く」スマートフォルダの裏付けデータ。
- **任意の診断ログ** (既定 OFF、設定 → 診断 → ログ で切替):
  `~/Library/Logs/Pinakeion/` に書出、5 MB で自動ローテーション
  (1 世代保持)。
- **カバーサムネ**: JPEG キャッシュ
  (`~/Library/Caches/Pinakeion/thumbnails/`)。
- **クイックプレビューキャッシュ**: 5×4 ページのプレビュー
  (`~/Library/Caches/Pinakeion/previews/`)。上限 500 MB、古いものから
  破棄。
- **検索インデックス**: ファイル名 / 解析タイトル / 著者の FTS5
  trigram インデックス。上記ファイルメタデータから派生し、ローカル
  SQLite カタログ内に保持。外部送信は一切ありません。
- **環境設定**: 表示モード、ソート項目 / 方向、タイル幅、
  サイドバー / インスペクタ / フォルダブラウザの表示状態。
  macOS UserDefaults とローカルカタログに保存。

### 過去にあったが現在は廃止

プレビュー版 (v0.9.2 以前) では姉妹リーダーアプリの既読位置を
共有 App Group コンテナから取込む実験的機能がありましたが、v0.9.2
で完全に廃止しました。Pinakeion は App Group コンテナを一切
読まず、他アプリのデータベースも読まず、それを許す entitlement
も持ちません。

### データの消去

- 設定 → プライバシー → **全データを削除**: カタログ、サムネ、
  プレビューキャッシュ、設定、診断ログを一括削除。
- 設定 → サムネイル → **サムネイルを全削除**: サムネキャッシュのみ。
- 設定 → サムネイル → **プレビューキャッシュを削除**: クイック
  プレビューキャッシュのみ。
- 設定 → 診断 → **ログを消去**: 診断ログディレクトリのみ。

### 子供向け

本アプリは 4+ 区分で、広告・アプリ内課金・外部サービスへのリンクは
ありません。

### 問合せ

ご質問は shinichiyuhara1@gmail.com まで。
