# mokumoku

[Ansible ユーザー会](https://ansible-users.connpass.com/)主催で開催されている、Ansible もくもく会の、Automation Controller に対する操作を Ansible で自動化するための Playbook です。

新コンテンツ（AAP2.1）の以下コンテンツに対応しています。

| 内容  | ディレクトリ |
|--|--|
|ネットワーク編 Exercise 6、7、9 | [network](./network/) |
| サーバー編 Exercise 2-3、2-4、2-6 | [server](./server/) |

もくもく会コンテンツ本編では Automation Controller に対する操作の Playbook を作成しませんので、こちらはおまけ的な位置付けです。

Automation Controller 自体に不慣れな場合は、まずは手動で操作されることをおすすめします。

そのうえで「あの操作はこうやって Playbook 化できるのか」と参考程度にご覧いただければと思います。

# 実行方法

## コレクションのインストール

`ansible.controller` コレクションをあらかじめインストールする。

Ansible Galaxy ではなく Automation Hub への接続が必要です（[接続設定](https://tekunabe.hatenablog.jp/entry/2020/12/27/ansible_galaxy_automation_hub)）。
## 環境設定
`inventory.ini` の以下の変数の値を、当日のご自身の環境の値に変更する。

```ini
[controller:vars]
ansible_host=当日のご自身の環境のAnsiblecontrollerのホスト名
controller_password=当日のご自身の環境のパスワード
```

## Playbook 実行
```
ansible-playbook -i inventory.ini 実行したいPlaybook
```
