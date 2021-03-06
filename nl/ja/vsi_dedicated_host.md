---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 専用ホストと専用インスタンス 

専用ホストは、ホストを配置するデータ・センターおよび POD を指定できる仮想サーバーです。 その後、ワークロード配置の最大限の制御、およびプロビジョン後の柔軟なオプションを可能にするために、インスタンス (つまり、仮想マシン) を特定のホストに割り当てます。
{:shortdesc}

## 保証された容量
ホストが配置されたデータ・センターおよび POD 内での容量が保証されます。 例えば、専用ホストと専用インスタンスを含む POD が容量に到達した場合、ホストに適切なスペースがあれば、専用インスタンスをホストに引き続き割り当てることができます。

## 可視のワークロード
専用ホストに割り当てられたすべての専用インスタンスのリソース使用量全体を 1 ページに表示できます。 コア、RAM、およびローカル・ストレージの使用量を表示します。これを利用して、専用インスタンスを別の専用ホストにマイグレーションする必要があるかを判断することができます。 こうした細分化されたレベルの情報により、ワークロードを最大限に制御して管理できます。 

## デプロイ後の管理
保証された容量とワークロードの可視性のほかに、専用ホスト間で専用インスタンスをマイグレーションして、ワークロード配置を最大限に制御することができます。

## 保守
インフラストラクチャー保守で専用ホストの再始動が必要とされる場合があります。 例えば、Xen ハイパーバイザーが更新を必要とすることがあります。 複数の専用ホストがある場合、保守によるダウン時間を最小化するために以下のオプションがあります。 
* 1 つのデータ・センター内の複数の POD によって保守が実行されます。 必要な保守を分散するため、専用ホストを別々の POD にデプロイできます。 
* 専用ホストについてのサポート・チケットを作成して、定期保守を遅らせるように要請できます。 その間に、同じ POD 内の専用ホスト間で専用インスタンス (オフライン) をマイグレーションできます。

## 高可用性
ある専用ホストで障害が起こった場合、その専用ホストの作業負荷は自動的に新しい専用ホストに移行されます。 専用インスタンスは、仮想サーバーのライフサイクルを通して専用のままです。

高可用性シナリオのため、追加の専用ホストを指定することを検討してください。 例えば、追加の専用ホストがあると、保守期間の作業負荷を移行するための柔軟性が得られます。
