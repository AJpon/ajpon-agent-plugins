---
name: skill-authoring-workflow
description: 'Use when 複雑なスキルの新規作成や大幅改修について、目的確認、曖昧さの解消、既存資産の再利用判断、段階的開示、設計承認、テスト承認が必要なとき。公開向けスキル作成、適用範囲が広いスキル設計、曖昧な依頼からの要件整理、既存スキルの大幅整理、回帰確認を伴うスキル改修で使う。'
---

# skill-authoring-workflow

複雑なスキルの新規作成または大幅改修だけを扱う。軽微な description 修正、単純な草案、通常の
eval、通常の配布だけならこのワークフローは開始せず、既存の `skill-creator` へ案内する。

## 進行順序

1. **適用判断**
   - 依頼が複雑な新規作成または大幅改修かを判断する。
   - 対象外なら理由を短く述べ、`skill-creator` の担当として止める。
2. **目的発見**
   - 目的や困りごとの確認を始める時点で
     [references/intent-discovery.md](references/intent-discovery.md) を読む。
3. **目的照合**
   - 事実・仮説・未確定事項を短く返し、ユーザー確認を得る。
   - 必要なら [templates/requirements.md](templates/requirements.md) に案件契約を記録する。
4. **既存資産・適用範囲調査**
   - 再利用、拡張、統合、新規の比較を始める時点で
     [references/scope-and-reuse.md](references/scope-and-reuse.md) を読む。
5. **設計承認**
   - 司令塔、参照資料、テンプレートの責務分担や読込条件を固める時点で
     [references/progressive-disclosure.md](references/progressive-disclosure.md) を読む。
6. **テスト承認**
   - eval、形式検査、リンク検査、人によるレビューの計画を作る時点で
     [references/test-first-workflow.md](references/test-first-workflow.md) を読む。
   - 必要なら [templates/test-plan.md](templates/test-plan.md) に案件契約を記録する。
7. **作成・検証**
   - 設計承認とテスト承認の両方の後にだけ、対象スキル成果物を作成・変更する。
   - 既存スキルの大幅改修や破壊的変更の判断を含む場合は、変更前または回帰計画時点で
     [references/maintenance-and-regression.md](references/maintenance-and-regression.md) を読む。
8. **引き渡し**
   - 変更ファイル、実施した検証、未検証事項、環境制約、ユーザーに残る作業を報告する。

## 停止条件

- 設計承認とテスト承認の前に、対象スキル成果物を作成・変更しない。
- 承認前に作成できるのは、レビュー用の要件整理、設計メモ、テスト計画、eval 案だけ。
- 目的確認の前に対象ドメインや利用環境を決め打ちしない。
- 検証できない項目は成功扱いにせず、未検証として残す。

## Red Flags / Common Mistakes

- 急ぎを理由に、質問や承認を飛ばして成果物へ進む。
- 曖昧な依頼を、特定ドメインや特定実装に勝手に決める。
- 一度に複数質問して、1回1問の発見プロセスを崩す。
- 軽微修正や通常 eval / 配布までこのワークフローで抱え込み、`skill-creator` との境界を曖昧にする。
