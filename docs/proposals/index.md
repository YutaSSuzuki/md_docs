# Proposals

このディレクトリは、実装前の変更案を保存する場所です。

Proposal には「これから何をするか」を書く。実装後に確定した判断は `../adr/`、現在状態は各 Current State 文書、実施済み変更は `../changelog/` に分ける。

承認後に実装し、完了後は `done/` へ移動するか、不要なら削除する。

## What To Write

- 背景
- 解決したい問題
- ゴール
- 対象範囲
- 変更案
- 影響するドキュメント
- リスク
- ロールバック方法

## Active Proposals

| Proposal | Status | Goal |
| --- | --- | --- |

## Reading Flow

1. [Active Proposals](#active-proposals) で未完了の変更案を確認する。
2. 作業対象の Proposal を読む。
3. 実装前にユーザー承認を確認する。
4. 実装後は Current State、ADR、Roadmap、Changelog を更新する。
5. 完了した Proposal は `done/` へ移動するか、不要なら削除する。

## Adding a Proposal

```bash
cp docs/proposals/template.md docs/proposals/example.md
```

## AI Update Rule

AI は、大きな機能追加、設計変更、DB 変更、インフラ変更を始める前に Proposal を作成または更新する。

ユーザー承認が必要な作業では、Proposal を作成したあとに実装へ進む。
