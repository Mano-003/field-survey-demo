# CHANGELOG — ui-candidate (field-survey-demo)

正本は brain-garden（非公開）の `apps/field-survey-hub-ui-candidate/index.html`
（ブランチ：`claude/field-survey-ui-candidate`）です。このファイルは反映履歴のみを記録します。

## [Unreleased] - 2026-07-16

- 正本の実装（設計レビュー①〜⑧で承認された内容）を無改変でコピーして初回公開。
  - schemaVersion "2.0"、`case:{name}` 構造
  - 現地調査5項目（接道状況／インフラ引込状況／給排水設備の現況／建物外観・劣化状況／
    眺望・日照）を追加。土地建物用／区分所有用で共通表示
  - 確認情報トグル（確認状況／確認日／確認時刻／確認者）を既存の備考トグルと同じ
    仕組み（CSSのdisplay切替のみ）で実装し、開閉時のスクロールジャンプを構造的に回避
  - 新規CSSは`legal-note`／`link-btn`の2つのみ。それ以外は既存コンポーネントを再利用し、
    告知書・付帯設備表と同一デザインに統一
  - 付帯設備表・物件状況確認書のデザイン・操作フローは無変更
  - schemaVersion不一致・欠落のJSONは読込拒否（現行版JSONとの自動統合はしない）
- 正本とのSHA-256一致を確認済み：
  `71326995bdebcb5fb341b96f907b9f925fcd2232668f7ee7f0c89e360f68ebd4`
