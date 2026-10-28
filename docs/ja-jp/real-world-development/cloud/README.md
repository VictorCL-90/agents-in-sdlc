---
slug: ja-jp/real-world-development/cloud
title: "GitHub Copilot クラウド エージェント"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

**[GitHub Copilot クラウド エージェント](https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent)** を使うと、GitHub Copilot がクラウドで非同期に作業できます。GitHub で作業を割り当てると、クラウド エージェントがバックグラウンドでリポジトリを調べ、変更を行い、プルリクエストを作成します。その間、別の作業を進められます。

これらの演習では、まずクラウド エージェントが従うカスタム指示を追加し、GitHub Issue を割り当てて実装させます。カスタム エージェントを確認して使用し、作業方法を調整します。エージェント ダッシュボードからセッションを監視して方向付けた後、エージェントが作成したプルリクエストをレビューし、結果を改善します。

## 演習

| 演習 | トピック | 説明 |
|----------|-------|-------------|
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. カスタム指示][ex1] | コンテキスト | クラウド エージェントが従うカスタム指示を追加します |
| [2. クラウド エージェント][ex2] | 非同期エージェント | GitHub Copilot クラウド エージェントに Issue を割り当てます |
| [3. カスタム エージェント][ex3] | 専門エージェント | カスタム エージェントを確認して使用します |
| [4. エージェントの管理][ex4] | 監視 | エージェント セッションを監視して方向付けます |
| [5. 反復][ex5] | レビュー | PR をレビューし、Copilot の作業を改善して、次のステップを選びます |

## 前提条件

このワークショップに参加する前に、次のものを用意してください。

- [ ] 有効な **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかのプランが設定された GitHub アカウント
- [ ] アカウントまたは組織で有効になっている GitHub Copilot クラウド エージェント

> [!TIP]
> 有料プランを利用していない場合、認証済みの学生は [GitHub Education][callout-student-plan-education] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用するエージェント、MCP、コードレビュー、Copilot CLI の機能が含まれているため、すべてのハーネスを完了できます。

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> クラウド エージェントは **Copilot Student、Pro、Pro+、Business、Enterprise** で利用できます。Copilot Free は対象外です。Copilot Business または Enterprise では、管理者が組織で有効にする必要があります。

> [!NOTE]
> このハーネスでは MCP を扱いません。Copilot で MCP サーバーを使う方法については、[CLI ハーネス][cli]または [VS Code ハーネス][vscode]を参照してください。

## はじめる

**[演習 0「前提条件」から始める →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-custom-instructions/
[ex2]: 2-cloud-agent/
[ex3]: 3-custom-agents/
[ex4]: 4-managing-agents/
[ex5]: 5-iterating/
[cli]: ../cli/
[vscode]: ../vscode/
