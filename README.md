# ネットワーク基礎演習案件パック

<a id="-ネットワーク基礎演習案件パック"></a>

架空の企業ネットワークを題材に、要件 → 設計 → 構築 → 動作確認 → トラブル対応を学ぶ **全9案件の教材**です。Cisco 機器の設定例と、Linux サーバーの演習を収録しています。

> **更新停止（参考資料）**：2026-10-18 から更新を停止しています。教材・実施状況は当時のものです。採用の判断には、主作品 [server](https://github.com/ns7jp/server) の本人操作の記録をご覧ください。

<a id="このリポジトリの位置づけ"></a><a id="採用ご担当者様へ成果物と実施状況"></a><a id="-このリポジトリについて"></a><a id="-採用ご担当者様へ"></a>

## この教材で確認できること

- **AI 支援で作成した学習用の副作品**です。9案件の構成図、設定例、確認方法、トラブルの例を用意しています。[AI 支援・教材の背景](docs/repository-guide.md)
- **本人が Packet Tracer や VM で実施した記録は掲載していません。** 全9案件の実施状況と本人の理解度は未確認です。掲載コマンド・期待出力・面接用の文例は、本人の実績や習得の証明ではありません。
- 社名・依頼・障害シナリオは架空です。[server の実行記録](https://github.com/ns7jp/server/blob/main/docs/evidence/README.md)は別構成の演習で、この9案件の実行証拠とは区別しています。

教材の内容を確認する場合は、[案件01の基礎手順](projects/case01_lan_design/README.md)と[案件09の統合設計・試験項目](projects/case09_capstone/README.md)から読めます。実施後の記録方法は[本人実績の残し方](docs/04_portfolio_presentation_guide.md)にまとめています。

## 🗂️ 案件一覧(全9案件)

| No. | 案件名 | 学べること | 難易度 |
| --- | --- | --- | --- |
| [案件01](projects/case01_lan_design/README.md) | 本社オフィスLANの設計・構築 | IPアドレス設計、L2スイッチ、ケーブリング、疎通確認の基礎 | ★☆☆☆☆ |
| [案件02](projects/case02_wan_routing/README.md) | 本社-支社間ルーティング構築 | VLSM、静的ルーティング、ルーティングテーブル | ★★☆☆☆ |
| [案件03](projects/case03_dhcp_dns/README.md) | DHCP/DNSサーバー構築 | IPアドレス自動配布、名前解決、Linuxサーバー構築の基礎 | ★★☆☆☆ |
| [案件04](projects/case04_vlan_segmentation/README.md) | VLANによる部門分割 | VLAN、タグVLAN(802.1Q)、VLAN間ルーティング、ACL | ★★★☆☆ |
| [案件05](projects/case05_firewall_nat/README.md) | ファイアウォール・NAT構築 | NAT/PAT、DMZ、ポート開放、境界防御 | ★★★☆☆ |
| [案件06](projects/case06_web_server/README.md) | Webサーバー構築・公開 | Webサーバー構築、SSL/TLS、公開サーバー運用 | ★★★☆☆ |
| [案件07](projects/case07_file_remote_access/README.md) | ファイルサーバー・リモートアクセス | Samba、SSH公開鍵認証、VPN | ★★★★☆ |
| [案件08](projects/case08_monitoring_ha/README.md) | 監視・冗長化による可用性向上 | 死活監視、VRRP冗長化、バックアップ運用 | ★★★★☆ |
| [案件09](projects/case09_capstone/README.md) | 【集大成】第二支社インフラ統合構築 | 案件01〜08の総合実践、設計書一式の作成 | ★★★★★ |

進め方の詳細は [学習ロードマップ](docs/00_roadmap.md) を参照してください。

## 📖 ドキュメント一覧

| ドキュメント | 内容 |
| --- | --- |
| [学習ロードマップ](docs/00_roadmap.md) | 学習ロードマップ、案件の依存関係、想定学習時間 |
| [用語集](docs/01_glossary.md) | 初心者向け用語集(ネットワーク・サーバー用語をやさしく解説) |
| [演習環境の準備](docs/02_environment_setup.md) | 演習環境の作り方(Packet Tracer / VirtualBox など) |
| [IP アドレス設計](docs/03_ip_address_design.md) | 全案件共通のIPアドレス設計書 |
| [実績の記録・伝え方](docs/04_portfolio_presentation_guide.md) | このポートフォリオを面接・書類選考でどう伝えるか |
| [教材の背景・実施状況](docs/repository-guide.md) | AI 支援の内訳、架空シナリオ、教材で扱う技術・環境 |

<details>
<summary>以前の README の節から探す</summary>

<a id="-想定シナリオ"></a><a id="-教材で扱う技術環境"></a><a id="-ディレクトリ構成"></a>

[想定シナリオ](docs/repository-guide.md#-想定シナリオ)、[技術・環境](docs/repository-guide.md#-教材で扱う技術環境)、[ディレクトリ構成](docs/repository-guide.md#-ディレクトリ構成)は、教材の背景ページへ移しました。

</details>

## 📜 ライセンス

本リポジトリの学習コンテンツは [LICENSE](LICENSE) の条件のもとで公開しています。
