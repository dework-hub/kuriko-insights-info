---
layout: default
title: kuriko Instagram Insights プライバシーポリシー
---

# kuriko Instagram Insights プライバシーポリシー

制定日: 2026年10月12日

kuriko Instagram Insightsは、本人のInstagramインサイトを本人のGoogle Driveへ記録するために、以下の方法でデータを扱います。

## アクセスするデータと用途

Instagram公式APIから、本人のアカウント情報、投稿ID・種類・公開日時、リーチ・表示回数・いいね・コメント・保存・シェアの指標を取得します。取得した値は、日付別のMarkdown記録を作成するために使います。

Google Drive APIから、認証した本人のアカウント情報、指定した保存先フォルダと記録ファイルのメタデータを取得します。これらはアカウントと保存先の確認、同名ファイルの確認、保存結果の照合に使います。記録ファイルの作成または更新も行います。

この構成では、Googleの同意画面にDrive全体のファイル管理権限が表示されます。実装は、指定したフォルダへの記録と、そのための確認処理に用途を限定します。無関係なDriveファイルを広告や分析のために収集しません。

## 保存先と運用サービス

インサイト記録は本人が指定したGoogle Driveフォルダに保存します。自動実行にはGitHub Actionsを使い、APIへの認証情報は非公開GitHubリポジトリの暗号化されたSecretsへ登録します。初期設定用のクライアント認証ファイルは、本人のMacでファイルアクセス権限を制限して保管します。

運用のためにMeta、Google、GitHubのサービスを利用します。インサイトやGoogleユーザーデータを販売したり、広告配信に利用したりしません。この自動化では、GoogleユーザーデータをAIモデルの学習に使いません。

実行ログと失敗通知には、実行状態やAPIの理由コードなど、問題の確認に必要な情報を記録します。アクセストークン、リフレッシュトークン、クライアントシークレットを記録に含めない運用を行います。

## 保管期間と利用停止

Driveに保存した記録は、本人が削除するまで保管します。利用を止める場合はGitHub Actionsの定期実行を無効にし、Googleアカウントでこのアプリのアクセス権を取り消せます。不要になった認証情報はGitHub SecretsとMacの設定用ファイルから削除できます。

Googleから受け取った情報の使用および他のアプリへの移転は、Limited Useの要件を含む[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy)に従います。

## 問い合わせ先

kurita@dework.net
