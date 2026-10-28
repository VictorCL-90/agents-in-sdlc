---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
description: "Copilot CLI のモード、カスタマイズ、MCP ツール、プルリクエストの自動化を学びながら、Tailspin Toys の変更を 2 つ実装、検証、提供します。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** は、ターミナルで GitHub Copilot をエージェント型のコーディング アシスタントとして利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業の流れを保てます。

このワークショップでは、Tailspin Toys の 1 つの連続したワークフローに取り組みます。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして、基本を確認します。
2. 星評価に対象を絞った変更を加えてブラウザーでレビューし、最初のプルリクエスト (PR) を手動でマージします。
3. フィルター機能の Issue から開始し、Plan モードでアプローチを定義して、Autopilot モードで構築した後、Interactive モードでレビューします。
4. リポジトリの指示を更新し、フィルター機能の作業に適用します。
5. 既存の `quality-checks` スキルをカスタマイズし、プロジェクトのチェックに使用します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーでフィルター機能を確認します。
7. 品質保証 (QA) カスタム エージェントを作成し、要件、カバレッジ、検証の証拠をレビューします。
8. フィルター機能の変更全体をレビューし、フィルター機能の PR に Agent Merge を使用します。
9. コンテキスト、モデル、共有、クラウドへの任意の委任に使える便利なスラッシュ コマンドを確認します。

ワークショップの焦点を絞るため、作成する PR は 2 つです。1 つ目は星評価、2 つ目はフィルター機能と、指示・スキル・QA プロファイル・テストの更新です。フィルター機能と品質に関するワークフローでは 1 つの会話とブランチを共有するため、各ツールを確認しながら、それまでの作業を活用できます。

## レッスン

| レッスン | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. Copilot CLI のインストール][ex1] | インストール | Copilot CLI をインストールして認証し、基本を確認します |
| [2. 星評価の追加で小さな成果を得る][ex2] | 最初の変更 | 既存の評価と null の場合の代替表示を追加し、最初の PR をマージします |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | Issue から機能を計画し、Autopilot で構築して、Interactive モードでレビューします |
| [4. カスタム指示による Copilot のガイド][ex4] | コンテキスト | 指示を確認して更新し、フィルター機能に適用します |
| [5. quality-checks スキルのカスタマイズと使用][ex5] | 繰り返し実行できるチェック | 既存のスキルを確認し、報告形式を変更して実行します |
| [6. Playwright MCP による機能の検証][ex6] | ブラウザーでの観察 | CLI で MCP を設定し、フィルターの動作を確認します |
| [7. QA エージェントの作成と使用][ex7] | 要件とカバレッジ | 専門家のプロファイルを作成して選択し、最終検証の証拠を収集します |
| [8. 機能の PR の作成とマージ][ex8] | レビューとマージ | 変更全体をレビューして PR を作成し、Agent Merge を使用します |
| [9. GitHub Copilot CLI のスラッシュ コマンド][ex9] | CLI 機能 | コンテキスト、モデル、共有、クラウド エージェントへの任意の委任を確認します |
| [10. 振り返りと次のステップ][ex10] | まとめ | ワークフロー、再利用可能なカスタマイズ、追加リソースを確認します |
| [オプション: Foundry を組み込む][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づいたエージェントをデプロイして Web サイトに接続します |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと Codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランを利用していない場合、認証済みの学生は [GitHub Education][student-plan] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用するエージェント、MCP、コードレビュー、Copilot CLI の各機能が含まれています。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## はじめる

**[前提条件から始める →][ex0]**

[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[student-plan]: https://github.com/education/students
[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
