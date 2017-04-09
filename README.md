# 事前準備
## ansible コマンドが使えるようにする
$ `sudo yum -y install epel-release`  
$ `sudo yum -y install ansible`

## ansible コマンドで接続確認する
$ `ansible all -i inventory/hosts -m ping`
```
192.168.33.20 | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}
```
