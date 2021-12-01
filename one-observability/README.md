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

## CloudWatch Synthetics
> Amazon CloudWatch Syntetics を使用して、スケジュールに従って実行される設定可能なスクリプトを作成し、エンドポイントと API を監視できます。
> Canaries はエンドポイントの可用性とレイテンシーをチェックし、読み込み時間データとUIのスクリーンショットを格納できます。REST API、URL、Web サイトのコンテンツを監視し、フィッシング、コードインジェクション、クロスサイトスクリプティングによる不正な変更がないかチェックできます。

> VPC 設定 Canary を配置する VPC を選択することもできます。これは、非公開エンドポイントをテストする場合に重要です。

APIのカナリアテストも可能。

## Container Insights
> CloudWatch Container Insights を使用して、コンテナ化されたアプリケーションとマイクロサービスから、メトリクスとログを収集、集計できます。

TBD

## Logs Insights
> CloudWatch Logs Insights には、サンプルクエリ、コマンドの説明、クエリの自動補完、およびログフィールド検出が用意されています。
> CloudWatch Logs Insights は、Amazon Route 53、AWS Lambda、AWS CloudTrail、Amazon VPC などの AWS サービス、および JSON としてログイベントを発行するアプリケーションログまたはカスタムログからログ内のフィールドを自動的に検出します。

## Lambda Insights
> Lambda Insights は ServiceLens と統合されています。以下の図のように、 View をクリックすると、特定の関数の実行に関する X-Ray のトレースを表示することができます。

## メトリクス
> Amazon EC2 インスタンスなどの一部のリソースの詳細モニタリングを有効にしたり、独自のアプリケーションメトリクスを公開することもできます。Amazon CloudWatch は、検索、グラフ化、アラームのために、アカウント内のすべてのメトリクス（AWS リソースメトリクスとユーザーが提供するアプリケーションメトリクスの両方）を利用できます。

## ダッシュボード
## 異常検出
## 埋め込みメトリックフォーマット
## アラーム

TBD

## Amazon Managed Service for Prometheus
> Amazon Managed Service for Prometheusは、Prometheusメトリクスの取り込み、保存、クエリー、アラートに対する水平スケーラビリティを追加するオープンソースのCNCFプロジェクトであるCortexを搭載しています。Amazon Managed Service for Prometheus は、Amazon Elastic Kubernetes Service と Amazon Elastic Container Service、および自己管理型 Kubernetes クラスター全体にわたるアプリケーションの監視を開始するために必要な負荷を軽減します。

## Amazon Managed Grafana
> AMG は、Amazon CloudWatch、Amazon Elasticsearch Service、Amazon Timestream、AWS IoT SiteWise、AWS X-Ray、Amazon Managed Service for Prometheus (AMP) などの運用データを収集する AWS データソースと統合され、一般的なオープンソースデータベース、サードパーティのモニタリングツールへのプラグインを提供します。AMG を使用すると、複数の AWS サービス、AWS アカウント、およびリージョンの情報を 1 つの Grafana ダッシュボードで簡単に視覚化できます。

## AWS Distro for OpenTelemetry 
> AWS ディストリビューションを OpenTelemetry で使用して、Amazon Elastic Compute Cloud (EC2)、Amazon Elastic Container Service (ECS)、Amazon Elastic Kubernetes Service (EKS) on EC2、AWS Fargate、AWS Lambda、オンプレミスで実行しているアプリケーションを計測できます。

