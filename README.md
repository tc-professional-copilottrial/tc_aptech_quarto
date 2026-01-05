
## 手順 1: プロジェクトの初期化とPython導入
```bash
# 1. 任意の作業フォルダを作成して移動
mkdir quarto-env-test
cd quarto-env-test

# 2. uvプロジェクトの初期化
uv init

# 3. Pythonのインストールとバージョン固定
# uv python install <version> で指定します
uv python install 3.14
uv python pin 3.14
```

## 手順 2: 仮想環境の作成と有効化
```bash
# 4. 仮想環境 (.venv) の作成
uv venv

# 5. 仮想環境の有効化
# Windows (PowerShell) の場合:
.venv\Scripts\activate

# Mac/Linux の場合:
source .venv/bin/activate
```

## 手順 3: 必要なライブラリのインストール
```bash
uv add jupyter matplotlib pandas
```

## 手順 4: VS Code の設定とプレビュー
### 拡張機能の確認

- VS Codeの拡張機能マーケットプレイスで以下が入っているか確認（なければインストール）。
- Quarto
- Python

### インタプリタの切り替え

- VS Code上で Ctrl + Shift + P (Macは Cmd + Shift + P) を押す。
- Python: Select Interpreter を入力して選択。
- 一覧から ('.venv': venv) または .venv フォルダ内のPythonを選択。
- ※一覧に出ない場合は、一度VS Codeを再起動してください。

### プレビュー実行

- 作成した check_env.qmd を開く（/// を ``` に戻しておくのを忘れずに）。
- 右上の「虫眼鏡アイコン（Preview）」をクリック。
- 右側にグラフや表が表示されれば成功です。
