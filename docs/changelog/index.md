# Changelog

このディレクトリは、実施済みの変更履歴を時系列で記録する場所です。

ここには「何を変更したか」を書く。判断理由は `../adr/`、未実装の構想は `../proposals/` に分ける。

## What To Write

- 実施日
- 変更内容
- 影響範囲
- 関連する ADR、Proposal、Issue
- 移行や注意点

## Documents

| Document | Purpose |
| --- | --- |
| [CHANGELOG](CHANGELOG.md) | 実施済み変更を時系列で把握する |

## Reading Flow

1. [CHANGELOG](CHANGELOG.md) で最近の変更を確認する。
2. 変更理由が必要な場合は `../adr/` を確認する。
3. 実装前の検討内容が必要な場合は `../proposals/` を確認する。

## AI Update Rule

AI がコード、設定、ドキュメントを変更した場合は、必要に応じて `CHANGELOG.md` を更新する。

小さな文言修正まで必ず記録する必要はないが、後から作業履歴として意味がある変更は記録する。
