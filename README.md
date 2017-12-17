# ClashOfCouple(仮名)
## Developers
* GameDesigner
    * agoago2nd
* Programmer
    * JichouP

## Genre
* Action-Puzzle

## Language
* Javascript

## Librally
* PIXI.js

## DevelopmentTools
* Browserify
* ESLint

## ESLint
```json
{
  "extends": ["eslint:recommended"],
  "env": {
      "browser": true
  },
  "parserOptions": {
    "ecmaVersion": 2017
  },
  "rules": {
    "no-magic-numbers": "error",
    "dot-location": ["error", "object"],
    "no-new": "error",
    "no-self-compare": "error",
    "vars-on-top": "error",
    "yoda": "error",
    "array-bracket-spacing": "error",
    "brace-style": "error",
    "camelcase": "error",
    "comma-spacing": ["error", {"before": false, "after": true}],
    "comma-style": ["error", "last"],
    "computed-property-spacing": ["error", "never"],
    "eol-last": "error",
    "indent": ["error", 2],
    "key-spacing": "error",
    "quotes": ["error", "single"],
    "require-jsdoc": "error",
    "semi": ["error", "always"],
    "semi-spacing": "error",
    "array-bracket-spacing": "error",
    "space-infix-ops": "error",
    "keyword-spacing": "error",
    "space-unary-ops": "error",
    "no-var": "warn",
    "prefer-const": "error"
  }
}
```
## 解説

### rulesより上の行について
* extends: eslintの推奨設定を使用する
* env: ブラウザ側のグローバル変数とかを使えるようにする
* parserOptions: EcmaScript2017に対応させる
* 
## rulesについて
* error: 警告が出たら必ず消すこと
* warn: 特別な理由がなければ警告を必ず消すこと

## ESLintの設定
* マジックナンバーは禁止。必ず名前をつけること
* ドット付近で改行する場合には、ドット前では改行せずにドット後にすること
* newしたやつは必ず変数代入をすること
* 自分自身との比較しないこと
* 変数定義は該当スコープの最上部でまとめて行うこと
* ヨーダ記法を使わないこと
* 配列の角括弧のすぐ内側に空白を入れないこと
* '{'の前には改行ではなく空白1つを入れること
* 変数はCONSTANT_CASEのものを除き全てcamelCaseで命名すること
* カンマの前には空白を入れない、後には空白をひとつだけ入れるようにすること
* 算出プロパティの角括弧内に空白を入れないようにすること
* ファイルの最後には空行を1つ入れること
* インデントはタブではなく空白2つにすること
* 文字定数はダブルクオートではなくシングルクォートで囲うこと
* jsdoc用のコメントは、関数定義時には必ず書くこと。(エディタの自動補完で関数の内容などを把握しやすくするためだけに使用)
    * 書くべき内容
        * 動作の概要
        * 引数の説明
        * 返り値
        * その他、補足等
* セミコロンは入れること
* セミコロンの後には改行か空白を1つ入れること
* 中置演算子の前後には空白を入れること
* varはできるだけ使わないようにすること
* 破壊的変更を行わない変数についてはconstを使うこと
