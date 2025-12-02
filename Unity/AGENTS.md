# AGENTS.md - Unity開発ガイドライン

## プロジェクト概要

ここに概要を書く

## 技術スタック

- Unity: 6.3
- UI: UI Toolkit（UXML + USS）

## ファイル構成

```
Assets/
  ├── ThirdParty/     # 外部アセット
  └── Project/        # 自作アセット
        ├── Scripts/       # C#スクリプト
        ├── Prefabs/       # プレハブ
        ├── Scenes/        # シーンファイル
        ├── Materials/     # マテリアル
        ├── Textures/      # テクスチャ
        ├── Fonts/         # フォント
        ├── Audio/         # 音声ファイル
        └── Animations/    # アニメーション
```

## C#コーディング規約

- クラス名: PascalCase（例: `PlayerController`）
- メソッド名: PascalCase（例: `MovePlayer()`）
- 変数名: camelCase（例: `playerSpeed`）
- プライベート変数: `_`プレフィックス（例: `_health`）
- 定数: UPPER_SNAKE_CASE（例: `MAX_HEALTH`）
- Inspector公開: `[SerializeField] private float _speed;`

## UIは UI Toolkit を採用する

- UXML: レイアウト定義（VisualTreeAssetとしてロード）
- USS: スタイル定義（StyleSheetとしてロード）
- C#: UIDocumentからrootVisualElementを取得してロジック実装

## Context7 MCP Server の使用の徹底

コード生成時は必ずContext7 MCP Serverを呼び出し、Unity公式ドキュメントの最新情報を参照すること。

All checks must pass before generated code can be merged.
