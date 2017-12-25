## インフラ技術の歴史

#### Github@KY0000

---

### パブリッククラウドの歴史

--

### AWS

- 2006年設立
- Amazon が提供
- パブリッククラウドのトップ３の一つ。

--

### GCP

- 2008年スタート
- Google が提供
- パブリッククラウドのトップ３の一つ。

--

### Azure（アジュール）

- 2008年発表
- 2010年サービス開始
- Microsoft
- パブリッククラウドのトップ３の一つ。

---

### OpenStack

- https://ja.wikipedia.org/wiki/OpenStack
- はじまりは2010年10月
- Rackspace Hosting と NASA が始めた
- 2012年9月 OpenStack Foundation 発足・OpenStack の運用を移管
- AWS を参考に高度に仮想化したIaaSを誰でも構築するための技術

--

## 最初にして最後の目的

#### インフラ構築/管理に関する自動化基盤の提供#

--

### OpenStack を構成する要素

- Nova (コンピュート)
- Neutron (ネットワーキング)
- Cinder (ブロックストレージ)
- Keystone (アイデンティティサービス)
- Glance (イメージサービス)
- Swift (オブジェクトストレージ)
- Horizon (ダッシュボード)

~~いい感じに厨二っぽい~~

--

## 使いどころ

どうしてもパブリッククラウドを使いたくない、という場合はオンプレ環境にOpenStackを構築することで、
リソースの調達等が自動化でき、コストダウン可能になる。  
しかし、やはり自社で用意できるデータセンターの規模には限界があり、コストもかかるので大人数で巨大なリソースを共有するパブリッククラウドを使った方がメリットが大きいと言える。

### 参考サイト

[おぷすたディストリビューションビジネスは何処へ向かうのか](https://qiita.com/jyoshise/items/76444753ce169393239a)

---

### Docker

- 2013/3/13にリリース
- ソフトウェアコンテナ内のアプリケーションのデプロイメントを自動化するオープンソースソフトウェアである。
- dotCloud社 ⇒ Docker社。dotCloud社のPaaSクラウドサービスのシステムが元になって作成された。

--

### 使いどころ

- テスト環境等、環境を使い捨てにしたい
- 1コンテナー1プロセスで動かせる場合

--

## ここがやばい

- 1コンテナー1プロセスで動かす前提
- コンテナ管理
- イメージ管理

--

### 技術要素

Linuxコンテナ技術:　libcontainer
ファイルシステム： aufs
etc..

--

### 従来の仮想化技術と比べると？

- ハイパーバイザー型製品と比べて、ディスク使用量が少ない
- インスタンス作成・起動が速い
- 性能劣化がほとんどない

--

### 付随サービス

- Docker Hub
  - コンテナイメージの公式オープンリポジトリ的な奴
- Docker Swarm
  - 正式にはサービスではなく、動作モードの一つ
- Docker Composer
  - これもサービスではない

--

### 参考サイト

- [Dockerのメリット・デメリット](http://bit.ly/2zrR6Rx)
- [Dockerの誤解と神話。識者が語るDockerの使いどころとは？ Docker座談会（前編）](https://thinkit.co.jp/article/2127)

---

### Kubernetes

- 2014年6月7日 発表
- 2015年7月21日 v1.0 リリース & Cloud Native Computing Foundation（CNCF）を設立し、Kubernetes をシードテクノロジーとして提供。
- コンテナ化アプリケーションの配備、スケーリング、管理を自動化するためのオープンソースシステムです。
- ホストのクラスタ間でアプリケーション・コンテナの配置、スケーリング、および操作を自動化するための「プラットフォーム」を提供することを目的としています。
- 元々Googleによって設計され、Cloud Native Computing Foundationに寄贈。


--

#### Case Studies

- box
- ebay
- ポケモンGO
- SAP
- Yahoo!Japan

-- 

#### 参考サイト

- [K8s Bootcamp](https://kubernetesbootcamp.github.io/kubernetes-bootcamp/index.html)
- [k8s 公式サイト](https://kubernetes.io/)
- [k8s 公式ブログ](http://blog.kubernetes.io/)
- [k8s on openstack](http://openstackdays.com/wp-content/uploads/2017/08/4-B3-8.pdf)

---

### OpenShift

- Redhat 社が提供する Kubernetes の拡張。
- Kubernetes はコミュニティベースで運用されており、サポート等欲しい場合は OpenShift Enterprise を使用した方が良いと思われます。
- [TestDrive on Cloud](https://www.openshift.com/container-platform/trial.html)
--

### OpenShift Enterprise

- PaaS環境の構築から自社で行うタイプ

--

### OpenShift Online3

- フルマネージドの OpenShift 。
- 基本的な考え方は Kubernetes と同様
- まだちょっと不安定な感じがするので使わない方が無難。

--

### OpenShift Dedicated 

- OpenShift Online の占有ホスト版。
- 2016年1月25日

--

### OpenShift Origin 

- The Open Source Container Application Platform
- オープンソースで開発中のプロジェクト

---

## 目次

[スライド集](./index.html)


