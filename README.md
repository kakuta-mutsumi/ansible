# ansible

## 概要

- ansibleでmacの環境構築をするためのもの

## 構造

```
.
├── README.md
└── mac
    ├── ansible.cfg
    ├── inventory
    │   ├── default
    │   └── group_vars
    │       └── local
    │           └── ansible.yml
    ├── playbooks
    │   ├── my-mac.retry
    │   └── my-mac.yml
    └── roles
        ├── base # macの基本設定
        │   ├── handlers
        │   │   └── main.yml
        │   └── tasks
        │       ├── main.yml
        │       └── osx_defaults.yml
        ├── dev-tools # homebrewを利用せず取得するもの
        │   └── tasks
        │       └── main.yml
        └── homebrew
            ├── tasks
            │   └── main.yml
            └── vars
                └── main.yml
```

## コマンド

```
cd mac
ansible-playbook ./playbooks/my-mac.yml
``` 