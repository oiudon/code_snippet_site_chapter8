# 環境構築

## pyenvでPython3.9.0のインストール
1. /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"　…　Homebrewのインストール
2. brew install pyenv　…　pyenvのインストール
3. echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
4. pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
5. echo 'eval "$(pyenv init -)"' >> ~/.zshrc
6. exec "$SHELL"
7. brew install openssl readline sqlite3 xz zlib tcl-tk　…　必要なプラグインをインストール
8. pyenv install 3.9.0　…　Python 3.9.0をインストール
9. pyenv versions　…　pyenvでインストールしたPythonバージョンの確認
10. pyenv global 3.9.0　…　Python 3.9.0を適用
11. python --version　…　Pythonバージョンの確認

## Gitクローン
1. cd /Users/mac/Documents/Django　… 作業ディレクトリを移動
2. git clone git@github.com:oiudon/code_snippet_site.git　… クローン

## 仮想環境の作成
1. cd code_snippet_site　… 作業ディレクトリに移動
2. python -m venv venv　… 仮想環境を作成する
3. source venv/bin/activate　… 仮想環境をアクティベートする
4. pip install --upgrade pip　… pipのアップグレード
5. pip install django==3.2　… Django 3.2をインストール

## Djangoコマンド
* source /Users/mac/Documents/Django/code_snippet_site/venv/bin/activate　…　仮想環境をアクティベートする
* deactivate　…　開発環境をディアクティベートする
* python manage.py runserver　…　開発サーバー立ち上げ
* manage.py makemigrations　…　マイグレーションファイルを作成
* python manage.py migrate　…　マイグレーションファイルからSQL発行しテーブル作成
* python manage.py test　…　テスト実行
* python manage.py createsuperuser　… admin権限ユーザーを作成
* python manage.py shell …　対話シェルの立ち上げ
* python manage.py shell_plus　…　django-extensionの対話シェル

## 管理画面
* ユーザー： admin
* アドレス： admin@example.com
* パスワード： M＠2shima

## マップ
* 管理画面： http://127.0.0.1:8000/admin

## ライブラリ
* pip install ipython …　シェルで自動補完が利用可能
* pip install django-extensions …　manage.py shell_plusコマンドが使用可能
* pip install django-bootstrap5　…　Bootstrap5のライブラリ
* pip install django-pygments-renderer　…　構文ハイライトを実装するライブラリ
