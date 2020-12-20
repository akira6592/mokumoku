# mokumoku-network

[Ansible ユーザー会](https://ansible-users.connpass.com/)主催で開催されている、[Ansible もくもく会 ネットワーク編](https://github.com/ansible/workshops/blob/devel/exercises/ansible_network/README.ja.md)の、Ansible Tower に対する操作を Ansible で自動化するための Playbook です。

本編では Ansible Tower に対する操作の Playbook を作成しませんので、こちらはおまけ的な位置付けです。

Ansible Tower 自体に不慣れな場合は、まずは手動で操作されることをおすすめします。

そのうえで「あの操作はこうやって Playbook 化できるのか」と参考程度にご覧いただければと思います。

# 実行方法
## 環境設定
`inventory.ini` の以下の変数の値を、当日のご自身の環境の値に変更する。

```ini
[tower:vars]
ansible_host=当日のご自身の環境のAnsibleTowerのホスト名
tower_password=当日のご自身の環境のパスワード
```

## Playbook 実行
```
ansible-playbook -i inventory.ini 実行したいPlaybook
```
