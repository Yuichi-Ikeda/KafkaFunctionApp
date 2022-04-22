# Azure Functions - Kafka Consumer アプリケーション

## 概要
　Azure Functions Kafka extension を利用した C# サンプルです。users Topic に配信されたメッセージをトリガーとして起動します。

[ベースサンプル](https://github.com/Azure/azure-functions-kafka-extension-sample-confluent)を元に最新版の Visual Studio 2022 にて新規作成しています。

### ローカル開発環境
- Visual Studio 2022

## 開発環境の準備

### [クイック スタート:Visual Studio を使用して Azure で初めての関数を作成する](https://docs.microsoft.com/ja-jp/azure/azure-functions/functions-create-your-first-function-visual-studio)

ローカル実行には local.settings.json ファイルをプロジェクトに追加して環境変数を設定する必要があります。

```json:local.settings.json
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "UseDevelopmentStorage=true",
    "FUNCTIONS_WORKER_RUNTIME": "dotnet",
    "Broker": "<Your domain>.confluent.cloud:9092",
    "Topic": "users",
    "APIKey": "<Your API Key>",
    "Secret": "<Your API Secret>"
  }
}
```

### クラウド実行環境
- Azure Functions : Windows 環境推奨
- .NET 6

　デプロイ後に Azure Functions の構成メニュー、アプリケーション設定で環境変数として local.settings.json の値を登録する必要があります。
