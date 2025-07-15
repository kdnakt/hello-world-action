---
inclusion: always
---

# Conventional Commits強制ルール

## コミットメッセージの形式
すべてのコミットメッセージは以下のConventional Commits形式に従う必要があります：

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## 必須のtype一覧
- **feat**: 新機能の追加
- **fix**: バグ修正
- **docs**: ドキュメントのみの変更
- **style**: コードの意味に影響しない変更（空白、フォーマット、セミコロンの欠落など）
- **refactor**: バグ修正でも機能追加でもないコード変更
- **perf**: パフォーマンスを向上させるコード変更
- **test**: テストの追加や既存テストの修正
- **chore**: ビルドプロセスやツール、ライブラリの変更

## コミットメッセージのルール
1. **type**は必須で、上記リストから選択する
2. **description**は現在形で書く（例：「add」「fix」「update」）
3. **description**は小文字で始める
4. **description**の末尾にピリオドは付けない
5. **scope**は任意だが、使用する場合は括弧内に記述
6. 破壊的変更がある場合は、typeの後に「!」を付けるか、footerに「BREAKING CHANGE:」を記述

## 良い例
```
feat: add user authentication
fix(auth): resolve login redirect issue
docs: update API documentation
feat!: remove deprecated user endpoint
```

## 悪い例（使用禁止）
```
Added new feature
Fix bug
Update docs
WIP: working on feature
```

## Kiroへの指示
- コミットメッセージを提案する際は、必ずConventional Commits形式を使用する
- ユーザーが不適切な形式のコミットメッセージを書こうとした場合は、正しい形式を提案する
- 変更内容に基づいて適切なtypeを選択する
- 複数の変更がある場合は、論理的に分割して複数のコミットを提案する