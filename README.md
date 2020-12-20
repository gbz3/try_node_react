# try_node_react

## nodenv環境構築 @Ubuntu

1. Clone nodenv into `~/.nodenv`

```bash
$ git clone https://github.com/nodenv/nodenv.git ~/.nodenv
```

2. PATH設定

```bash
$ echo 'export PATH="$HOME/.nodenv/bin:$PATH"' >> ~/.bashrc
```

3. 環境設定

```bash
$ ~/.nodenv/bin/nodenv init
$ echo 'eval "$(nodenv init -)"' >>~/.bashrc
```

4. nodenv 再ロード(シェルセッション再起動)

5. node-build プラグインインストール

```bash
$ git clone https://github.com/nodenv/node-build.git ~/.nodenv/plugins/node-build
```

6. シェル環境確認

```bash
$ curl -fsSL https://github.com/nodenv/nodenv-installer/raw/master/bin/nodenv-doctor | bash
```

## Node.js環境構築 @Ubuntu

1. インストール可能バージョンの確認/インストール

```bash
$ nodenv install --list |grep ^14 |tail -3
14.15.1
14.15.2
14.15.3
$ nodenv install 14.15.3
$ ls ~/.nodenv/versions
14.15.3
```

2. shimsリハッシュ

```bash
$ nodenv rehash
```

3. グローバル環境設定(Optional)

```bash
$ nodenv global 14.15.3
```

4. ローカル環境設定

```bash
$ cd ~/_git_repos/try_node_react
$ nodenv local 14.15.3
$ cat .node-version
14.15.3
```
