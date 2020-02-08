# 実践Rust入門学習メモ

## 目次

- 基礎編
  - 第1章 Rustの特徴
  - 第2章 はじめてのRustプログラム
  - 第3章
  - 第4章
  - 第5章
  - 第6章
  - 第7章
- 実践編
- 

## 第1章 Rustの特徴

- パフォーマンス早い
  - C++とほぼ変わらんレベル
    - マシンコードにコンパイル
    - GCなしの軽量なランタイム
    - ゼロコスト抽象化 (抽象化機能を実行時のコスト無しに実現)
- 安全
  - 型安全
  - メモリ安全性
    - バッファオーバフロー
    - 誤ったメモリ領域へのアクセス
    - 初期化前のメモリ領域へのアクセス
    - 解放後のメモリ領域へのアクセス (UseAfterFree)

- マルチスレッドでデータ競合(Data race)が起きない
  - channel
  - lock
  - slice
  - immutableな参照
  - 競合状態(race condition)は防げない(処理順序やデッドロックなど)

- 他の言語との連携が容易
  - FFI(多言語関数インターフェイス)を通して他の言語と連携できる
   - Python, C, Node.js, Ruby, Erlang


## 第2章 はじめてのRustプログラム

- rustup
  - 複数バージョンのRustのインストールと管理(nvm的な働きか？)
  - クロスコンパイル用のターゲットのインストール 
  - RLSなどの開発支援ツールのインストール(RLSはVSCodeでいい感じにするために必要だった)

- Helloworld
    - cargo new helloでcargo runでOK
    - rustでは1プロジェクトをcrateと呼ぶ
    - cargo : 貨車
    - crate : 木箱
 
- VSCodeのインストール
  - RLS : Rust Language Service
    - Language Servierプロトコルに準拠する開発支援用サーバ

- RPM計算機プログラムとデバッガによる実行
    - トレイト境界 ： javaでいう <T extends ...>のようなもの (らしいが説明が難しくてわからない。8章でやるようなのでその時にはわかりたい。)
    - デバッガのセットアップ
      - lldbというコマンドを使う(macではリンカのインストール時にLLDBも一緒に入る)
      - VSCode に CodeLLDBというExtensionを入れる

    

