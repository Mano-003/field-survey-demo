# field-survey-demo

現地調査アプリ（不動産売却案件ハブ｜初期調査・売主確認）の
GitHub Pages検証公開用リポジトリです。

## 正本との関係

- 正本（アプリコードの管理場所）は非公開リポジトリ [Mano-003/brain-garden](https://github.com/Mano-003/brain-garden) の
  `apps/field-survey-hub/index.html` です。
- このリポジトリ（field-survey-demo）は、GitHub Pagesでのスマホ実機検証のために
  正本から `index.html` を無改変でコピーした**検証用配布先**です。
- 更新は必ず正本（brain-garden）側で行い、検証が必要になった時点でこのリポジトリへ
  同じ内容を再コピーしてください。**このリポジトリ単体での直接編集は行わないでください。**

## 現在のステータス：ダミーデータ専用の検証環境

- **実名・住所・電話番号・メールアドレス等、実在の個人・案件を特定できる情報は
  一切入力しないでください。**
- 入力・保存・エクスポートするデータは、すべて架空の案件ID・架空の内容としてください。
- 本アプリはダミーデータによる動作確認専用であり、実案件の記録には使用しません。
- 本リポジトリはPublicです。公開URLには誰でもアクセスできる前提で運用してください。

## 付帯設備表の「有／無」について

「有／無」は現在の設置状況ではなく、売買対象として買主様へ引き渡す設備の有無を表します。

## 法的判断について

本アプリは現地確認・売主回答の記録用であり、告知要否・重要事項説明書への記載要否・
契約不適合責任・法令権利関係の確定を自動判断するものではありません。

## データの扱いについて

本アプリはサーバー通信を行わず、入力内容はブラウザの`localStorage`と、
アプリの「JSON出力」機能で手動生成するJSONファイルにのみ保持されます。
このリポジトリには案件データ（案件JSON等）を一切含めません。

## 更新方法（今後の運用）

1. 正本（brain-garden）の `apps/field-survey-hub/index.html` を更新
2. 変更内容をレビュー
3. 承認後、同ファイルをこのリポジトリの `index.html` へ無改変で反映（SHA-256で同一性確認）
4. `CHANGELOG.md` に反映内容を追記してコミット

## ui-candidate/ — UI候補版（比較検証用・未採用）

`ui-candidate/index.html` は、現行版（`index.html`）とは別のUI方針の候補版です。
正本は非公開リポジトリ brain-garden の `apps/field-survey-hub-ui-candidate/index.html`
（ブランチ：`claude/field-survey-ui-candidate`）で、現行版の正本
（`apps/field-survey-hub/index.html`）とは完全に別管理です。

- 公開URL：`https://mano-003.github.io/field-survey-demo/ui-candidate/`
- 現行版のURL（`https://mano-003.github.io/field-survey-demo/`）と並べて実機比較するための配置です。
- JSON構造は現行版（schemaVersion "1.2"）と異なる新系統（schemaVersion "2.0"）です。
  **現行版のJSONとは互換性がなく、自動統合もしません。**
- 採用が決まるまで、このディレクトリの追加・更新が現行版（`index.html`）に影響することはありません。
- 更新方法は現行版と同様（正本側で変更→レビュー→SHA-256確認のうえ無改変で反映）。
  詳細は `ui-candidate/CHANGELOG.md` を参照してください。