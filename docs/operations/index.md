# Operations

このディレクトリは、プロジェクトを実行・運用するための手順を置く場所です。

ここには「どう動かすか」「どう確認するか」「問題が起きたらどう対応するか」を書く。

## What To Write

- ローカル実行手順
- ビルド手順
- デプロイ手順
- バックアップ、リストア手順
- 監視方法
- 障害対応手順
- よくある問題と対処

## Documents

| Document | Purpose |
| --- | --- |
| [Runbook](runbook.md) | 日常的な実行・確認手順を把握する |
| [Deployment](deployment.md) | デプロイ手順を把握する |
| [Backup](backup.md) | バックアップとリストア手順を把握する |
| [Monitoring](monitoring.md) | 監視項目と確認方法を把握する |
| [Troubleshooting](troubleshooting.md) | 障害時の調査・復旧手順を把握する |

## Reading Flow

1. [Runbook](runbook.md) で基本操作を確認する。
2. [Deployment](deployment.md) で反映方法を確認する。
3. [Monitoring](monitoring.md) で正常性の見方を確認する。
4. 問題発生時は [Troubleshooting](troubleshooting.md) を確認する。

## AI Update Rule

AI が起動方法、ビルド方法、デプロイ方法、監視方法、障害対応方法を変更した場合は、このディレクトリを更新する。

性能計測の実行手順は `../performance/` ではなく、このディレクトリに書く。計測結果や分析は `../performance/` に書く。
