# Piosolver レポート拡張ツール

## これは何？
Piosolverが出力する集合分析のレポートファイル(report.csv)にEQBなどの特徴量列を追加して、PostgreSQLにテーブルとして追加するツールです。

EQBはポーカーの分析において強力な特徴量ですが、Piosolverにレポートとして出力する機能がないため、このツールを開発しました。

## 使い方

1. Piosolverで以下の設定を行います：
   - 「include hands in report」にチェックを入れて集合分析レポートを出力

2. ファイル配置：
   - main.pyと同じディレクトリに`report`フォルダを作成
   - `report`フォルダ内にPiosolverのReportsフォルダから生成される集合分析レポートが入ったフォルダを配置

3. フォルダ名の設定：
   - 配置したフォルダ名がテーブル名として使用されます
   - 必要に応じてフォルダ名を変更してください
   - 例：`"AggregatedReport_2024-11-25_23-42-13"` → `"BBvsBTN3bet flop"`

## 追加される特徴量

- EQB
- EQB毎のアクション頻度
- 役バケット
- 役バケット毎のアクション頻度
- ハイカードなどのコミュニティカード特徴量

※特徴量の詳細については、コードから察してください