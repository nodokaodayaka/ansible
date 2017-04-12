# 事前準備
## ansible コマンドが使えるようにする
$ `sudo yum -y install epel-release`  
$ `sudo yum -y install ansible`

## ssh できるようなにする
$ `ssh-keygen -t rsa`  
$ `パスワードなしでエンター`  
$ `ssh-copy-id vagrant@192.168.33.20`

## ansible コマンドで接続確認する
$ `ansible all -i inventory/hosts -m ping`
```
192.168.33.20 | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}
```
## httpd
### インストール
$ `ansible-playbook -i inventory/hosts httpd.yml`
### 接続確認
[ブラウザ接続確認](http://192.168.33.20)
