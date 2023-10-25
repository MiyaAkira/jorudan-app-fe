# jorudan-app-fe
## 概要
* ふらっと調べられる観光地案内アプリのフロントエンド部分を開発
* アプリの概要については下記url先の資料を参照 
https://mailkyutechjp-my.sharepoint.com/:p:/g/personal/koki_yoshida958_mail_kyutech_jp/Ec1x4LxUc_5Nv_wAg4rXLo4BzGFXwWnX-gYmZO643EBMKw?e=qh8349
## 環境構築
1. リポジトリのダウンロード
`git clone https://github.com/ysdko/jorudan-app-fe.git`
1. pythonのバージョン確認
`python3 -V`
でバージョンが3.10.12であることを確認
3.10.12でない場合は以下を実行

1. pyenvのインストール(pyenvがインストールされていない場合)
    1. pyenvに必要なパッケージのインストール
`sudo apt install \
  build-essential libssl-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev curl llvm \
  libncursesw5-dev tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev \
  libopencv-dev git`
    1. pyenvをダウンロード
    `git clone https://github.com/pyenv/pyenv.git ~/.pyenv`
    1. パスを通す
    `echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init --path)"' >> ~/.bashrc`
    1. pyenvがインストールされたか確認
    `pyenv -v`


1. pyenvを使ったpythonのバージョンの切り替え
    1. pythonの新しいバーションのインストール
    `pyenv install -l 3.10.12`
    1. 現在のディレクトリにてpythonのバージョンの切り替えをする
    `pyenv local 3.10.12`
    1. バージョンが切り替わっているか確認
    `python -V`
1. 仮想環境の作成
`python3 -m venv venv`

1. 仮想環境内に入る
`. venv/bin/activate`
1. 必要なパッケージのインストール
`pip install -r requirements.txt`
1. サーバを立てる.ローカルホストが立ち上がりHello Worldが表示されればOK
`streamlit run test.py`

## 開発方法
1. イシューを作成(https://github.com/ysdko/jorudan-app-fe/issues)
1. main ブランチから開発用のブランチを切る。（ブランチ名については下のブランチ命名規則を参照）
 `git fetch`
 `git checkout origin/main -b issue #イシュー番号`
2. 開発用のブランチで開発を進める。（このブランチからさらにブランチを切ってマージをさせる分には自由にやってもらって大丈夫です。コミットのルールについては下記を参照）
4. main -> 開発用ブランチにマージをし、コンフリクトが発生していないか確認する。



## コミット命名規則
- コミット名は`プレフィックス: コミットの説明`の形式
    - 例: `git commit -m "add: 場所入力画面の作成"`


- プレフィックスは以下を参考
    - fix：バグ修正
    - add：新規（ファイル）機能追加
    - update：機能修正（バグではない）
    - remove：削除（ファイル）



