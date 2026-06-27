# Architecture

このディレクトリは、現在のシステム構成を理解するための資料を置く場所です。

ここには「今どう動いているか」を書く。過去の構成や採用理由は残さず、理由は `../adr/` に記録する。

## What To Write

- システム全体の構成
- 利用者、外部サービス、外部システムとの関係
- アプリケーション内部の主要コンポーネント
- 処理フロー
- デプロイ構成
- インフラ構成

## Documents

| Document | Purpose |
| --- | --- |
| [Current State](current-state.md) | 現在の構成を短く把握する |
| [System Context](system-context.md) | 利用者、外部システム、境界を把握する |
| [Runtime Flow](runtime-flow.md) | 主要な処理の流れを把握する |
| [Deployment](deployment.md) | 実行環境、配置、ネットワーク構成を把握する |

## Reading Flow

1. [Current State](current-state.md) で全体像を確認する。
2. [System Context](system-context.md) で外部との関係を確認する。
3. [Runtime Flow](runtime-flow.md) で処理の流れを確認する。
4. [Deployment](deployment.md) でどこでどう動くか確認する。

## AI Update Rule

AI がアプリ構成、依存サービス、処理フロー、インフラ、デプロイ方式を変更した場合は、このディレクトリを更新する。

構成変更の理由が後から必要になりそうな場合は、`../adr/` に ADR を追加する。
