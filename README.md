# Vagrant Ansible PHP7.3開発環境

Vagrant上のAnsibleでプロビジョニングしPHP開発環境を構築する。

* PHP7.3
* Nginx
* MariaDB
* PostgreSQL
* Node.js


## 説明

### Vagrant

vagrant plugin install vagrant-vbguest
vagrant plugin install dotenv
vagrant plugin install vagrant-disksize
vagrant plugin install vagrant-hostsupdater
vagrant plugin install vagrant-hostmanager


### Ansible
/provision/playbook.yml

## 使用例
```
vagrant up
```

```
vagrant ssh
```

##### Laravelインストール
```
composer create-project --prefer-dist laravel/laravel=6.* project
cd project
```

##### 設定
`.env`
```ini
DB_CONNECTION=pgsql
DB_HOST=localhost
DB_PORT=5432
DB_DATABASE=vagrant
DB_USERNAME=vagrant
DB_PASSWORD=vagrant
```

##### 確認

http://phpdev.test
