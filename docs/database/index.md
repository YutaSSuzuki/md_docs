# Database

このディレクトリは、現在の DB 構造を理解するための資料を置く場所です。

DB を使用しないプロジェクトでは、このファイルに「このプロジェクトでは DB を使用しない」と書く。

## What To Write

- 使用する DB 製品
- テーブル、カラム、型、制約
- インデックス
- リレーション
- マイグレーション方針
- 初期データ、検証データ

## Documents

| Document | Purpose |
| --- | --- |
| [Schema](schema.md) | 現在のテーブル、カラム、制約を把握する |
| [ER Diagram](er-diagram.md) | テーブル間の関係を把握する |
| [Migration](migration.md) | DB 変更方法と履歴の扱いを把握する |

## Reading Flow

1. [Schema](schema.md) で現在の DB 構造を確認する。
2. [ER Diagram](er-diagram.md) で関係性を確認する。
3. [Migration](migration.md) で変更方法を確認する。

## AI Update Rule

AI がテーブル、カラム、インデックス、制約、マイグレーションを変更した場合は、このディレクトリを更新する。

DB 設計方針を変更した場合は、`../adr/` に ADR を追加する。
