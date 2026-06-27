# Architecture Decision Records

このディレクトリは、確定した設計判断の履歴を保存する場所です。

ADR には「なぜその判断をしたか」を書く。現在状態そのものは `../architecture/`、`../api/`、`../database/`、`../operations/`、`../performance/` に書く。

Accepted になった ADR は削除しない。変更時は Superseded として新しい ADR へリンクする。

## What To Write

- 採用した技術、方式、外部サービス
- 採用しなかった代替案
- 判断理由
- トレードオフ
- コスト、性能、運用への影響
- 後から「なぜ？」となりそうなこと

## Records

| ADR | Status | Decision |
| --- | --- | --- |

## Reading Flow

1. [Records](#records) で関連する ADR を探す。
2. Current State 文書とあわせて、現在状態と判断理由を分けて確認する。
3. 古い ADR が Superseded の場合は、後継 ADR を確認する。

## Adding an ADR

```bash
cp docs/adr/template.md docs/adr/0001-example.md
```

## AI Update Rule

AI がアーキテクチャ、DB 設計方針、外部サービス、運用方式、性能方針に関わる判断を行った場合は、ADR を追加または更新する。

ADR は履歴なので、原則削除しない。
