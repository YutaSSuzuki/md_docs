# Docs as Code Framework

このリポジトリは、Docs as Codeで開発資料を管理するための考え方とMarkdownテンプレートを保存します。

個別システムの現行資料は含めず、各プロジェクトで再利用するドキュメント体系そのものを管理します。

## Usage

新しい開発を始めるときは、このリポジトリをcloneします。

```bash
cd ~/git
git clone https://github.com/YutaSSuzuki/md_docs.git
```

対象プロジェクトに `docs/` を作り、必要なテンプレートをコピーして内容を記入します。

```bash
cd ~/git/<project>
mkdir -p docs/{architecture,api,database,operations,performance,adr,proposals,roadmap,changelog}
cp ~/git/md_docs/templates/documentation-policy.md docs/documentation-policy.md
```

ADRやProposalなどは、作成時に対応するテンプレートをコピーします。

```bash
cp ~/git/md_docs/templates/adr.md docs/adr/0001-example.md
cp ~/git/md_docs/templates/proposal.md docs/proposals/example.md
```

テンプレート更新を取り込む場合:

```bash
git -C ~/git/md_docs pull --ff-only
```

## Intent

個人開発でも、未来の自分を別の開発者として扱います。

そのため、開発速度を落としすぎずに、後から再開しても次が分かる状態を目指します。

- 現在のシステム構成
- 判断理由
- 未完了作業
- 実施済み変更
- 運用手順
- 性能課題

## Adopted Ideas

本フレームワークでは、複数の考え方を用途別に採用します。

| Idea | Role |
| --- | --- |
| Docs as Code | MarkdownをGitで管理し、コードと同じ変更履歴に載せる |
| Living Documentation | Current State文書を常に最新状態に保つ |
| ADR | 後から「なぜ？」となる判断を削除せずに残す |
| Proposal | 実装前の検討案と承認対象を残す |
| Roadmap | 未着手、進行中、保留、完了を管理する |
| Changelog | 実施済み変更を時系列で記録する |

## Directory Pattern

```text
docs/
├── index.md
├── documentation-policy.md
│
├── architecture/
├── api/
├── database/
├── operations/
├── performance/
│
├── adr/
├── proposals/
├── roadmap/
└── changelog/
```

## Current State Documents

以下は現在状態だけを書く文書です。過去の構成は残しません。

- `architecture/`
- `api/`
- `database/`
- `operations/`
- `performance/`

過去の構成や判断理由は `adr/`、実施済み履歴は `changelog/`、未実装の構想は `proposals/` に分けます。

## Templates

- [documentation-policy.md](templates/documentation-policy.md)
- [adr.md](templates/adr.md)
- [proposal.md](templates/proposal.md)
- [roadmap.md](templates/roadmap.md)
- [changelog.md](templates/changelog.md)
- [current-state.md](templates/current-state.md)
- [api.md](templates/api.md)
- [database.md](templates/database.md)
- [operations.md](templates/operations.md)
- [performance.md](templates/performance.md)
