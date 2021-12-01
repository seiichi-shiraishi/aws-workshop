## URL
https://catalog.us-east-1.prod.workshops.aws/v2/workshops/31676d37-bbe9-4992-9cd1-ceae13c5116c/ja-JP/intro

## OverView
- CloudWatch
  - ネイティブモニタリング
  - ロギング
  - アラーム
  - ダッシュボード
  - AWS X-Ray (トレース)
- Amazon Managed Service for Prometheus
- Amazon Managed Grafana
- AWS Distro for OpenTelemetry (ADOT)
  - アプリケーション監視用の分散トレースとメトリックスを収集するためのオープンソースの API、ライブラリ、およびエージェントを提供
  - アプリケーションを計測し、相関メトリクスとトレースを複数の AWS およびパートナーのモニタリングソリューションに送信

## 環境設定
「自分のAWSアカウントを利用する」の通りに実行。
Service Stack がかなり時間かかる。4０mくらい。

## CloudWatch ServiceLens
> CloudWatch ServiceLens は、トレース、メトリクス、ログ、アラームを 1 か所に統合できるようにすることで、サービスとアプリケーションの可観測性を高めます。ServiceLens は CloudWatch と AWS X-Ray を統合し、アプリケーションのエンドツーエンドのビューを提供し、パフォーマンスのボトルネックをより効率的に特定し、影響を受けたユーザーを特定するのに役立ちます。

> ServiceLensを使用すると、X-Ray トレースを介してサービスインタラクションデータを取得したり、ダッシュボードを介してサービスメトリック情報への洞察を自動的に得ることができるだけでなく、トレースがキャプチャされたタイミングのアプリケーションログを通じて、さまざまなマイクロサービスのコンテキストに関する洞察を得ることができます。

## AWS X-Ray
> AWS X-Ray は、開発者がマイクロサービスアーキテクチャなどを使用して構築された分散アプリケーションを、本番環境において分析およびデバッグするのに役立ちます。X-Rayを使用すると、アプリケーションとその基盤となるサービスのパフォーマンスを把握して、パフォーマンスの問題やエラーの根本原因を特定し、トラブルシューティングできます。

> XRay は、トレースで使用されている AWSサービスの詳細を表示することもできます。たとえば、Invocation サブセグメントの下の DynamoDB を選択します。Resources タブに移動して、テーブル名、テーブルで実行された操作などの詳細を確認します。他のサービスについても確認し、サービス固有の情報を確認してください。

## Contributor Insights
> Contributor Insights は、外れ値を特定し、最も重いトラフィックパターンを特定し、上位のシステムプロセスをランク付けすることで、システムやアプリケーションのパフォーマンスに影響しているユーザーや要因を把握するのに役立ちます。

> これには、AWS CloudTrail、Amazon Virtual Private Cloud、Amazon API Gateway などの AWS サービスからのログ、サービスまたはオンプレミスサーバー（Apache のアクセスログなど）から送信されたカスタムログが含まれます。

> Amazon DynamoDB 用の Amazon CloudWatch Contributor Insights は、テーブルまたはインデックス内で最も頻繁にアクセスされたキーおよびスロットルされたキーを一目で識別するための診断ツールです。このツールでは、CloudWatch Contributor Insights を使用します。 テーブルまたはグローバルセカンダリインデックスで DynamoDB の CloudWatch Contributor Insights を有効にすることで、それらのリソースで最もアクセスされた項目とスロットルされた項目を表示できます。

### カスタムルールの作成
API Gateway -> Log full requests/responses data にチェックすると、ログデータをCloudWatchに送信できる
