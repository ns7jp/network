# ネットワーク教材の背景・実施状況

[教材一覧と概要](../README.md)に戻る。教材の背景、確認できる範囲、AI 支援の内訳をまとめています。

教材・実施状況は更新停止時点（2026-10-18）のものです。今回の整理で本人の実行実績は追加していません。

## 教材の背景

このリポジトリは、**未経験からインフラ・サーバー構築エンジニアへの転職を目指す人**が、
ネットワークとサーバー構築の基礎を、要件・設計・手順・確認方法の順に学ぶための
ポートフォリオ教材です。実行結果と本人の説明を追加することで、習得した範囲を伝えられます。

ただの用語集や暗記ノートではなく、**架空のIT企業に所属する新人エンジニアとして、
架空の取引先企業から届く「案件(お仕事)」を1つずつ解決していく**というストーリー形式を
採用しています。実際の現場で使われる「要件定義 → 設計 → 構築 → 動作確認 → トラブル対応」
という流れをそのまま体験できるように作られています。

> 💡 **初心者の方へ**：このパックは「知識ゼロから読んでも迷わない」ことを最優先に設計しています。
> 各案件は独立した教材としても読めますが、`案件01 → 案件09` の順に読み進めると、
> 1つの会社のネットワークが少しずつ成長していく様子を体験できます。

## AI 支援と主作品との関係

- **AI支援で作成した部分が大きいです。** 教材の多くは、AIツール（Claude Code・OpenAI Codex）の支援で作成しました。2026-09-28 時点で確認できる範囲では、main へのプルリクエストのマージ6件のうち5件は `claude/…`、1件は `codex/…` のブランチからのもので、マージを除くコミット7件のうち5件は作者が `Claude` です（作者が島田則幸の2件は、最初の LICENSE・README の作成と `codex/…` ブランチの1件）。
- **主作品との関係:** 案件03（DHCP/DNS）・案件08（監視）などは、主作品の [DHCP 構築案件パック](https://github.com/ns7jp/server/blob/main/docs/build-package-dhcp/README.md)・[Zabbix 構築案件パック](https://github.com/ns7jp/server/blob/main/docs/build-package-zabbix/README.md)と扱うテーマが重なります。この教材は Cisco 機器の設定を中心にした別の構成で、主作品の記録の代わりにはなりません。

## 実施状況と記録方法

**公開している成果物は、架空案件9件の設計・構築・確認手順をまとめた教材です。** 2026年9月11日時点の公開資料で確認できる範囲を示します。

| 区分 | 現在の状態 | 確認できる内容 |
| --- | --- | --- |
| 設計・演習教材 | 作成済み | 全9案件の構成図、設定例、確認方法、トラブルの例 |
| 本人による構築・動作確認 | 実行証跡未掲載（実施状況未確認） | 掲載コマンド・期待出力だけでは、本人が全9案件を実施したとは判定できません |
| 本人による判断・説明 | 説明記録未掲載 | 「得られるスキル」や面接文例は学習目標・記入例であり、本人の習得確認ではありません |
| 実顧客・本番環境での運用 | 実績として未確認 | 架空の会社・依頼・障害シナリオを用いた演習です |

短時間で見る場合は、[案件01の基礎手順](../projects/case01_lan_design/README.md) → [案件09の統合設計・試験項目](../projects/case09_capstone/README.md) → [本人実績の残し方](04_portfolio_presentation_guide.md) の順にご覧ください。本人が別構成で実施したサーバー演習は、[serverの検証証跡台帳](https://github.com/ns7jp/server/blob/main/docs/evidence/README.md)から確認できます。本教材9案件の実行証拠とは区別しています。

各案件のREADMEには、以下を必ず記載しています。

- お客様(架空)からの依頼内容と背景
- 構成図・IPアドレス設計
- 実際の作業手順(コマンド・設定を含む)
- 動作確認の方法
- よくあるトラブルと対処法
- この案件の学習目標と、実施後に使う面接説明の例

[案件09](../projects/case09_capstone/README.md) では教材全体の設計のつながりを確認できます。
本人の実施範囲・理解度は、実施日・環境・結果と本人の説明を記載した記録で確認します。

## 🎬 想定シナリオ

| 項目 | 設定 |
| --- | --- |
| あなたの立場 | IT保守運用会社「**フュージョンITソリューションズ**」に入社したばかりの新人インフラエンジニア |
| 取引先企業 | 従業員10名 → 50名へと成長していく商社「**株式会社サンプル商事**」 |
| あなたの仕事 | 成長する取引先から寄せられる、ネットワーク・サーバーに関する相談(案件)に、先輩の指導を受けながら1つずつ対応していく |

登場人物や社名はすべて架空のものです。IPアドレスは実在の組織を指さないよう、
プライベートIPアドレスと `RFC 5737` で予約された検証用アドレス(`203.0.113.0/24` など)のみを使用しています。

## 🧰 教材で扱う技術・環境

| 分類 | 使用ツール |
| --- | --- |
| ネットワーク機器シミュレータ | Cisco Packet Tracer |
| サーバー仮想化 | VirtualBox |
| サーバーOS | Ubuntu Server / CentOS Stream |
| 主なミドルウェア | Apache/Nginx, ISC DHCP, BIND9, Samba, OpenSSH, OpenVPN, Zabbix, keepalived |
| 主なコマンド | ping, traceroute, ip, nslookup/dig, tcpdump, systemctl, iptables/firewalld |

具体的な導入手順は [docs/02_environment_setup.md](02_environment_setup.md) にまとめています。

## 📁 ディレクトリ構成

```text
network/
├── README.md                          # 教材全体の入口
├── docs/                               # 全案件共通のドキュメント
│   ├── 00_roadmap.md
│   ├── 01_glossary.md
│   ├── 02_environment_setup.md
│   ├── 03_ip_address_design.md
│   ├── 04_portfolio_presentation_guide.md
│   └── repository-guide.md             # このファイル
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
