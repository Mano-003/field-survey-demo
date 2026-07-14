# CHANGELOG — field-survey-demo

## [Unreleased] - 2026-07-14 (3)

- 正本（brain-garden）で追加強化したスクロール位置復元処理を反映。
  - `overflow-anchor: none`によりブラウザ標準のスクロールアンカリングとの競合を排除。
  - スクロール位置復元を二重`requestAnimationFrame`化し、遅延レイアウト調整にも対応。
  - ヘッドレス環境では再現できない実機依存の挙動のため、Galaxy実機での再確認が必要。
  - 業務ロジック・質問文・選択肢・JSON構造は変更なし。
  - 正本とのSHA-256一致を確認済み：
    `3cefad5b74b2c3ac98e089fffdb14975c36a8328e03b4c246b721f5ed987569f`

## [Unreleased] - 2026-07-14 (2)

- 正本（brain-garden）で追加修正したスクロールジャンプ対策を反映。
  - 「未確認」タブの「開く」ボタンで発生していた、トップへ戻ってから目的地へ跳ぶ
    二重スクロールアニメーションを解消。
  - サブタブ（現地調査／告知書／付帯設備表）切替時のスクロール位置クランプによる
    瞬間ジャンプを解消。
  - 業務ロジック・質問文・選択肢・JSON構造は変更なし。
  - 正本とのSHA-256一致を確認済み：
    `25227b4345bad6d450271776d8508a07b43afbe71959e4ddba66cfa649a5a4d5`

## [Unreleased] - 2026-07-14

- 正本（brain-garden）で修正したGalaxy実機テストのスクロール位置ジャンプ対策を反映。
  - `renderSurvey()`／`renderEquipment()`／`renderDisclosure()`の全体再描画前後で
    `window.scrollY`を保持・復元し、`requestAnimationFrame`で再調整も追加。
  - 下部ナビ5ボタンに`type="button"`を明示。
  - 業務ロジック・質問文・選択肢・JSON構造（`schemaVersion: "1.2"`）は変更なし。
  - 正本とのSHA-256一致を確認済み：
    `ac66dcf3e990074b9f3a6f5e39b23c76f1628f9dc81a8be17627a5b2d3cb03a8`

## [codex-mvp1-baseline] - 2026-07-14

- 正本 `Mano-003/brain-garden` の `apps/field-survey-hub/index.html`
  （基準版：codex-mvp1-baseline）を無改変でコピーして初回公開。
  SHA-256ハッシュで正本との同一性を確認済み：
  `8dcd81f231654406b13c2510cbe0212d93b0fffc6bc5812838c7ac76e9c392b6`
- 業務ロジック・質問文・選択肢・JSON構造（`schemaVersion: "1.2"`）は正本と同一。
- GitHub Pagesによるダミーデータ検証公開のための最小構成
  （`index.html` / `README.md` / `CHANGELOG.md` / `.gitignore` / `.nojekyll`）のみを配置。
