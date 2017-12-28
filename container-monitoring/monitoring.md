## コンテナのモニタリング

#### Github@KY0000

---

### コンテナのリソース監視

1. [Monitoring Kubernetes with Datadog](https://www.datadoghq.com/ja/blog/monitoring-kubernetes-datadog/)
1. cAdviser(k8s付属) ⇒ fluentd ⇒ zabbix 方式
1. [Grafana App for Kubernetes](https://github.com/grafana/kubernetes-app)

---

### cadviser x fluentd x zabbix

- Exactly Once は必要ですか？
- At Most Once で良ければデータ転送ツールの標準として Fluentd でいかがでしょうか？

### fluent-plugin-cadviser

- SEO 適正評価サービスの WooRank が開発したプラグイン。
- Fork して使用すればよいかと思います。

### fluent-plugin-zabbix

- sfujiwara なる謎の人物が作成しているプラグイン。

---

## その他スライド

[スライド集](../index.html)


