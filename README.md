# Website template minimum

静的ウェブサイトを開発するための最小構成テンプレートです。LPや数ページくらいのWebサイトを開発するため想定になってます。node.js は利用せずに Visual Studio Code の拡張機能や MAMP or XAMPP の開発環境を利用する構成になっています。

## 目次

- [推奨環境](#推奨環境)
- [ディレクトリ構成](#ディレクトリ構成)
- [拡張機能設定](#拡張機能設定)
- [便利サイト](#便利サイト)

---

## 推奨環境

- macOS または Windows
- Visual Studio Code ソースコードエディタ
- MAMP または XAMPP によるWebサーバー環境

---

## ディレクトリ構成

```
.
├── .vscode/
│   ├── extensions.json
│   └── settings.json
├── htdocs/
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.min.css
│   │   ├── img/
│   │   │   └── dummy.gif
│   │   ├── js/
│   │   │   └── jquery-3.6.0.min.js
│   │   └── sass/
│   │      ├── foundation/
│   │      │   ├── _base.scss
│   │      │   ├── _mixin.scss
│   │      │   ├── _reset.scss
│   │      │   └── _variables.scss
│   │      ├── layout/
│   │      │   └── _dummy.scss
│   │      ├── object/
│   │      │   ├── component/
│   │      │   ├── └── _dummy.scss
│   │      │   ├── project/
│   │      │   ├── └── _dummy.scss
│   │      │   └── utility/
│   │      │       └── _dummy.scss
│   │      └── style.scss
│   └── index.html
├── .editorconfig
├── .gitignore
└── README.md
```
### `.vscode/`

Visual Studio Codeのワークスペース設定ファイルを格納しています。推奨拡張機能やエディタの設定をプロジェクトで統一するために使用しています。

### `htdocs/`

プロジェクトのルートディレクトリに対応しています。

### `htdocs/assets/`

プロジェクトのアセットディレクトリに対応しています。CSSや画像、JavaScriptファイルなどを格納します。

### `htdocs/assets/css/`

CSSファイルを格納します。

### `htdocs/assets/img/`

画像ファイルを格納します。

### `htdocs/assets/js/`

JavaScriptファイルを格納します。

### `htdocs/assets/sass/`

CSSにコンパイルされる前のSassファイルをこのディレクトリに配置します。`htdocs/assets/sass/style.scss`をエントリーポイントとして、`htdocs/assets/css/`に`style.min.css`として出力されます。フォルダの構成は[FLOCSS](https://github.com/hiloki/flocss)に対応しています。

### `htdocs/assets/sass/foundation/`

サイト全体のデフォルトスタイルを格納します。

### `htdocs/assets/sass/layout/`

各ページを構成するサイト全体で共通したエリアを格納します。

### `htdocs/assets/sass/object/`

サイト全体で再利用できるパターンを持つモジュールを配下のそれぞれのフォルダに格納します。

### `htdocs/assets/sass/object/component/`

小さな単位のモジュールを格納します。（ボタンなど）

### `htdocs/assets/sass/object/project/`

いくつかのComponentと、他の要素によって構成される大きな単位のモジュールをを格納します。

### `htdocs/assets/sass/object/utility/`

ComponentとProjectのモディファイア（パターン）で解決することができないスタイル、また、調整のための便利クラスなどを格納します。

### `.gitignore`

Git の管理に含めないファイルを指定するためのファイルです。

### `README.md`

このファイルです。プロジェクトの説明、ツールの使い方、インストール方法などを理解してもらうために記述しています。

---

## 拡張機能設定

### Japanese Language Pack for Visual Studio Code

Visual Studio Codeはデフォルトで英語での表示になっています。日本語化する場合に必要なパッケージです。

### indent-rainbow

インデントに色がつきコードの可読性を上げます。

### EvilInspector

インストールするだけで、エディタ上の全角スペースが着色されるようになります。

### vscode-icons

フォルダやファイル拡張子からアイコンが変更されます。何のファイルなのか一目でわかりやすくなります。

### Auto Complete Tag

Auto Close TagとAuto Rename Tagを併せ持つ拡張機能です。閉じタグを自動で入れてくれて、開始タグを変更すると閉じタグも同様に変更します。

### Path Intellisense

ファイルパス、ファイル名を自動補完してくれます。

### HTMLHint

HTMLの構文チェックをしてくれます。ルールのカスタマイズをしたい場合は`.htmlhintrc`を作成する必要があります。

### Live Sass Compiler

Sassファイルを監視して自動でコンパイルしてくれます。`.vscode/settings.json`の設定内容を元にベンダープレフィックスを付与します。IE11対応は外しているので必要な場合は`"ie >= 11",`の記述を追加します。  
※Sassの@importを使った書き方が2022年10月1日までにサポート終了します。今後は@useと@fowardを使った書き方になりますが、「Live Sass Compiler」は対応していません。

---

## 便利サイト

### [Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/)

CSSプロパティの各ブラウザ対応状況を表示してくれます。

### [gitignore.io - プロジェクトに役立つ.gitignoreファイルを作成しよう](https://www.toptal.com/developers/gitignore)

`.gitignore`生成サービスです。

### [placehold.jp | ダミー画像生成 モック用画像作成](https://placehold.jp/)

サイズ表示付きの画像を生成できるWEBサービスです。

### [SVGOMG - SVGO's Missing GUI](https://jakearchibald.github.io/svgomg/)

SVG画像を圧縮してくれるWEBサービスです。

### [Table Tag Generator | HTMLの表を簡単に作成・結合ツール。テーブルタグジェネレーター](https://tabletag.net/ja/)

列と行を指定すると、リアルタイムにプレビューとソースが変更されます。

### [TinyPNG – Compress WebP, PNG and JPEG images intelligently](https://tinypng.com/)

画像サイズを圧縮してくれるWEBサービスです。

### [Qiita](https://qiita.com/)

Qiitaは、エンジニアに関する知識を記録・共有するためのサービスです。
