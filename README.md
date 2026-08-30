# 🌐 ネットワーク基礎演習案件パック

**未経験からサーバー構築エンジニアを目指す人のための、実務を模した学習型ポートフォリオ**

![status](https://img.shields.io/badge/status-portfolio-blue)
![level](https://img.shields.io/badge/level-beginner--friendly-brightgreen)
![topic](https://img.shields.io/badge/topics-network%20%7C%20server%20%7C%20infra-orange)

---

## 📌 このリポジトリについて

このリポジトリは、**未経験からインフラ・サーバー構築エンジニアへの転職を目指す人**が、
「ネットワークとサーバー構築の基礎知識を、実務に近い形で身につけたこと」を
採用担当者に伝えるためのポートフォリオです。

ただの用語集や暗記ノートではなく、**架空のIT企業に所属する新人エンジニアとして、
架空の取引先企業から届く「案件(お仕事)」を1つずつ解決していく**というストーリー形式を
採用しています。実際の現場で使われる「要件定義 → 設計 → 構築 → 動作確認 → トラブル対応」
という流れをそのまま体験できるように作られています。

> 💡 **初心者の方へ**：このパックは「知識ゼロから読んでも迷わない」ことを最優先に設計しています。
> 各案件は独立した教材としても読めますが、`案件01 → 案件09` の順に読み進めると、
> 1つの会社のネットワークが少しずつ成長していく様子を体験できます。

---

## 🎬 想定シナリオ

| 項目 | 設定 |
|---|---|
| あなたの立場 | IT保守運用会社「**フュージョンITソリューションズ**」に入社したばかりの新人インフラエンジニア |
| 取引先企業 | 従業員10名 → 50名へと成長していく商社「**株式会社サンプル商事**」 |
| あなたの仕事 | 成長する取引先から寄せられる、ネットワーク・サーバーに関する相談(案件)に、
先輩の指導を受けながら1つずつ対応していく |

登場人物や社名はすべて架空のものです。IPアドレスは実在の組織を指さないよう、
プライベートIPアドレスと `RFC 5737` で予約された検証用アドレス(`203.0.113.0/24` など)のみを使用しています。

---

## 🗂️ 案件一覧(全9案件)

| No. | 案件名 | 学べること | 難易度 |
|---|---|---|---|
| [案件01](projects/case01_lan_design/README.md) | 本社オフィスLANの設計・構築 | IPアドレス設計、L2スイッチ、ケーブリング、疎通確認の基礎 | ★☆☆☆☆ |
| [案件02](projects/case02_wan_routing/README.md) | 本社-支社間ルーティング構築 | VLSM、静的ルーティング、ルーティングテーブル | ★★☆☆☆ |
| [案件03](projects/case03_dhcp_dns/README.md) | DHCP/DNSサーバー構築 | IPアドレス自動配布、名前解決、Linuxサーバー構築の基礎 | ★★☆☆☆ |
| [案件04](projects/case04_vlan_segmentation/README.md) | VLANによる部門分割 | VLAN、タグVLAN(802.1Q)、VLAN間ルーティング、ACL | ★★★☆☆ |
| [案件05](projects/case05_firewall_nat/README.md) | ファイアウォール・NAT構築 | NAT/PAT、DMZ、ポート開放、境界防御 | ★★★☆☆ |
| [案件06](projects/case06_web_server/README.md) | Webサーバー構築・公開 | Webサーバー構築、SSL/TLS、公開サーバー運用 | ★★★☆☆ |
| [案件07](projects/case07_file_remote_access/README.md) | ファイルサーバー・リモートアクセス | Samba、SSH公開鍵認証、VPN | ★★★★☆ |
| [案件08](projects/case08_monitoring_ha/README.md) | 監視・冗長化による可用性向上 | 死活監視、VRRP冗長化、バックアップ運用 | ★★★★☆ |
| [案件09](projects/case09_capstone/README.md) | 【集大成】第二支社インフラ統合構築 | 案件01〜08の総合実践、設計書一式の作成 | ★★★★★ |

進め方の詳細は [docs/00_roadmap.md](docs/00_roadmap.md) を参照してください。

---

## 📖 ドキュメント一覧

| ドキュメント | 内容 |
|---|---|
| [docs/00_roadmap.md](docs/00_roadmap.md) | 学習ロードマップ、案件の依存関係、想定学習時間 |
| [docs/01_glossary.md](docs/01_glossary.md) | 初心者向け用語集(ネットワーク・サーバー用語をやさしく解説) |
| [docs/02_environment_setup.md](docs/02_environment_setup.md) | 演習環境の作り方(Packet Tracer / VirtualBox など) |
| [docs/03_ip_address_design.md](docs/03_ip_address_design.md) | 全案件共通のIPアドレス設計書 |
| [docs/04_portfolio_presentation_guide.md](docs/04_portfolio_presentation_guide.md) | このポートフォリオを面接・書類選考でどう伝えるか |

---

## 🧰 使用技術・環境

| 分類 | 使用ツール |
|---|---|
| ネットワーク機器シミュレータ | Cisco Packet Tracer |
| サーバー仮想化 | VirtualBox |
| サーバーOS | Ubuntu Server / CentOS Stream |
| 主なミドルウェア | Apache/Nginx, ISC DHCP, BIND9, Samba, OpenSSH, OpenVPN, Zabbix, keepalived |
| 主なコマンド | ping, traceroute, ip, nslookup/dig, tcpdump, systemctl, iptables/firewalld |

具体的な導入手順は [docs/02_environment_setup.md](docs/02_environment_setup.md) にまとめています。

---

## 📁 ディレクトリ構成

```text
network/
├── README.md                          # このファイル(ポートフォリオ全体の入口)
├── docs/                               # 全案件共通のドキュメント
│   ├── 00_roadmap.md
│   ├── 01_glossary.md
│   ├── 02_environment_setup.md
│   ├── 03_ip_address_design.md
│   └── 04_portfolio_presentation_guide.md
└── projects/                           # 案件本体(全9案件)
    ├── case01_lan_design/README.md
    ├── case02_wan_routing/README.md
    ├── case03_dhcp_dns/README.md
    ├── case04_vlan_segmentation/README.md
    ├── case05_firewall_nat/README.md
    ├── case06_web_server/README.md
    ├── case07_file_remote_access/README.md
    ├── case08_monitoring_ha/README.md
    └── case09_capstone/README.md
```

---

## 🙋 採用ご担当者様へ

各案件のREADMEには、以下を必ず記載しています。

- お客様(架空)からの依頼内容と背景
- 構成図・IPアドレス設計
- 実際の作業手順(コマンド・設定を含む)
- 動作確認の方法
- よくあるトラブルと対処法
- この案件で得られたスキルと、面接でのアピールポイント

短時間でスキルレベルを確認されたい場合は、集大成である
[案件09](projects/case09_capstone/README.md) からご覧いただくのが最も効率的です。

---

## 📜 ライセンス

本リポジトリの学習コンテンツは [LICENSE](LICENSE) の条件のもとで公開しています。
