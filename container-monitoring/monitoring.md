## コンテナのモニタリング

#### Github@KY0000

---

### コンテナのリソース監視

1. [Monitoring Kubernetes with Datadog](https://www.datadoghq.com/ja/blog/monitoring-kubernetes-datadog/)
1. [Grafana App for Kubernetes](https://github.com/grafana/kubernetes-app)
1. [cAdvisor x zabbix](https://www.zabbix.com/img/zabconf2015_jp/presentations/04_zabconf2015_watanabe.pdf)
1. [Prometheus + Grafana + cAdvisor](http://bit.ly/2pIxRDP)
1. cAdvisor(k8s付属) ⇒ fluentd ⇒ zabbix 方式

---

### 監視 SaaS を使ったモニタリング

- メリット：楽。確実。
- デメリット：高い。
- ◎◎円/監視ホスト数・月
- 例えば？
  - Datadog
  - Mackerel
  - New Relic

---

### Heapster & cadvisor x fluentd x zabbix

- 採用の前に fluentd の特性を知るべし。
  - "Exactly Once" or "At Most Once "

--

### Heapster

- Kubernetesクラスタ内のコンテナのリソースモニタリングツール。
- Kubernetesクラスタ内の全てのminionを自動で発見
- pod ID、コンテナ名、pod IP、ホスト名、ラベルを統計情報と一緒に保存

--

### cAdvisor

- Google 主に開発した Docker コンテナのリソースモニタリングツール
![cadvisor-logo](images/cadvisor-logo.png)

--

### fluent-plugin-cadviser

- SEO 適正評価サービスの WooRank が開発したプラグイン。
- Fork して使用すればよいかと思います。

--

### fluent-plugin-zabbix

- sfujiwara なる謎の人物が作成しているプラグイン。
- fluentd で取り込んだデータを zabbix へ転送できる。
- 送るだけなので大したことやってない。
- Fork して使用すればよいかと思います。

---

## その他スライド

[スライド集](../index.html)


