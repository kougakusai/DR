# ARC-002-backend-deployment

Date: 2021/07/17

## Status

proposed

## Context

clubhook-backendの開発初期はHerokuにデプロイしていた。
しかし、無料枠では24時間稼働が不可能であることから、別のデプロイ先を検討する運びとなった。

ただし、選定にあたって以下の要件を考慮した。
* 低コストであること
* 常時稼働可能であること
* サービスのスケールに対応できること

## Decision

Amazon Web Services(AWS)にデプロイし、サーバーレス環境で運用する。

AWSの中でも、次のものを仕様する。

|名称|機能|
|---|---|
|Cognito|認証|
|IAM|認可|
|AppSync|GraphQL API|
|Lambda|APIで使用する関数・処理|
|DynamoDB|データベース|

## Other Options (任意)

Google Cloud Platform(GCP)は、永久無料枠が存在するものの、RDBなど無料枠が無いサービスもあるため、不採用とした。
また、Google App Engine(GAE)にデプロイする場合はサーバーの設定が必要になるため、
サーバーレス運用が可能なAWSの方がメンテナンスコストが少ないだろうと判断した。

## Consequences

今まで開発していたコードはサーバを起動するものだったが、変更後はサーバーレスになるため、既存資産を活用することはできない。

また、AWS特有の開発方法があるため、学習コストを要する。
