# Vibe Coder Bootcamp - プロジェクト要件定義支援ツール

このプロジェクトは、Vibe Coder Bootcampの受講生がプロジェクトの要件定義を効率的に行うための支援ツールです。AIエージェント（Cursor）を活用して、基本的なプロジェクト情報から実装可能なレベルの詳細な設計書まで、段階的に作成することを目指します。

## 📁 プロジェクト構成

```
sampleproject/
├── README.md                                    # このファイル
├── docs/
│   ├── input/                                   # プロジェクト基本情報の入力フォルダ
│   ├── output/                                  # 生成されたドキュメントの出力フォルダ
│   ├── prompt/                                  # AIエージェント用プロンプトファイル
│   │   ├── system-requirements-prompt.md       # ステップ2: システム要件定義書作成用プロンプト
│   │   └── detailed_requirements_prompt.md     # ステップ3: 詳細要件定義書作成用プロンプト
│   └── template/                                # ドキュメントテンプレート
│       └── Requirements_Specification_Template.md
```

## 🚀 使用方法

### ステップ1: プロジェクト基本情報の入力

`/docs/input` フォルダに、実現したいプロジェクトに関する基本情報をテキストファイル（例: `idea.md`）として作成・入力してください。

**入力すべき情報の例：**
- **プロジェクト名**: アプリの名称
- **目的**: 誰の、どんな課題を解決したいか
- **主要機能**: 実現したいことのリスト
- **ターゲットユーザー**: どんな人に使ってほしいか

### ステップ2: システム要件定義書の作成 (骨子固め)

1.  Cursorで `docs/prompt/system-requirements-prompt.md` をメンションします。
2.  AIエージェントにドキュメント作成を依頼します。
3.  `docs/output/system_requirements.md` に、プロジェクトの骨子となるシステム要件定義書が生成されます。

**このステップの目的:**
あなたのアイデアを基に、プロジェクトの全体像、主要な機能、技術的な方向性、そしてUI/UXのコンセプトを固めます。

### ステップ3: 詳細要件定義書の作成 (実装レベルの詳細化)

1.  ステップ2で生成された `system_requirements.md` を確認します。
2.  Cursorで `docs/prompt/detailed_requirements_prompt.md` をメンションします。
3.  AIエージェントに詳細要件定義書の作成を依頼します。
4.  `docs/output/detailed_requirements_specification.md` に、実装可能なレベルの詳細な要件定義書が生成されます。

**このステップで生成される主な内容:**
- **UI/UX設計**: 画面遷移図、ワイヤーフレーム、デザインシステム
- **データベース設計**: ER図、テーブル定義
- **API仕様**: REST APIのエンドポイント定義
- **アーキテクチャ**: システム構成図、コンポーネント設計

### ステップ4: 個別詳細設計ドキュメントの生成 (分割・専門化)

1.  ステップ3で生成された `detailed_requirements_specification.md` を確認します。
2.  Cursorで `docs/prompt/generate_detailed_design_files_prompt.md` をメンションします。
3.  AIエージェントに実行を依頼します。
4.  `docs/design/` ディレクトリ内に、以下の5つの詳細設計ファイルが生成されます。
    - `system-architecture.md`
    - `database-design.md`
    - `api-specification.md`
    - `ui-ux-design.md`
    - `development-plan.md`

**このステップの目的:**
統合された詳細要件定義書を、各専門領域（DB, UI, APIなど）ごとのドキュメントに分割し、より専門的で管理しやすい形に整理します。

## 💡 使用のコツ

- **ステップ・バイ・ステップで進める**: 各ステップで生成された内容を確認し、納得してから次のステップに進むことで、手戻りが少なくなります。
- **AIの提案を活用する**: AIはあなたが見落としている視点や、より良い実現方法を提案してくれることがあります。提案内容を吟味し、プロジェクトに活かしましょう。
- **反復的な改善**: 生成されたドキュメントを確認し、必要に応じて `/docs/input` の情報を更新したり、プロンプトに追記したりして再生成することで、より完成度の高い設計書を作成できます。

## 🎯 期待される成果

このツールを使用することで、以下の成果が期待できます：

1.  **構造化された設計**: ビジネス要件からUI/UX、データベース、コンポーネント設計まで、体系的で漏れのない設計書を作成できます。
2.  **専門的なドキュメント管理**: 各専門領域に特化した設計書を持つことで、見通しが良く、管理しやすいプロジェクト構造を実現します。
3.  **開発効率の向上**: 明確な設計書に基づき、AIによるコード生成を含めた開発プロセスをスムーズに進めることができます。
4.  **リスクの早期発見**: 設計段階で潜在的な課題やリスクを特定し、事前に対策を検討できます。
5.  **思考の壁打ち**: AIを壁打ち相手として活用し、自身のアイデアを深掘りし、具体化することができます。

---

**Vibe Coder Bootcamp** - 「Text is KING」の原則に基づき、AIとの対話を通じてアイデアを形にしましょう！