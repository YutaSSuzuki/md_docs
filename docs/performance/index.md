# Performance

このディレクトリは、性能に関する現在状態、試験計画、結果、分析を置く場所です。

ここには「どれくらいの性能で動くか」「何を測ったか」「どこがボトルネックか」を書く。

## What To Write

- 現在の性能状態
- 性能目標
- 性能試験計画
- 性能試験結果
- メトリクス
- ボトルネック分析
- 改善内容
- 再測定結果

## Documents

| Document | Purpose |
| --- | --- |
| [Current Performance](current-performance.md) | 現在の性能状態と既知の課題を把握する |
| [Test Plan](test-plan.md) | 何を、どの条件で、どう測るか把握する |
| [Test Result](test-result.md) | 測定結果を把握する |
| [Bottleneck Analysis](bottleneck-analysis.md) | 遅い箇所、制約、改善方針を把握する |

## Reading Flow

1. [Current Performance](current-performance.md) で現在の性能状態を確認する。
2. [Test Plan](test-plan.md) で測定条件を確認する。
3. [Test Result](test-result.md) で結果を確認する。
4. [Bottleneck Analysis](bottleneck-analysis.md) で原因と改善方針を確認する。

## AI Update Rule

AI が性能検証、性能改善、メトリクス取得、ボトルネック調査を行った場合は、このディレクトリを更新する。

計測コマンドや実行手順は `../operations/` に書く。測定条件、結果、分析はこのディレクトリに書く。
