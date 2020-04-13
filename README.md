### GMS2 User Manual on Japanese

超意訳。翻訳者の英語力が高くないため。また、言語や文化の違いによる齟齬は可能な限り吸収する必要があると考えるため。  
GMS2 そのものが独特で遠まわしな表現を使う傾向にあり、明らかに不自然だと思った部分は勝手ながらそれとなく直したりしている。

ただし、実際の IDE 内のコンテンツに関する翻訳はなるべく原型を留めるよう努力している。

- Drug and Drop
  - 翻訳しない

- ライセンス名 (Creator、Desktop とかそういうの)
  - 翻訳しない

- auto response
  - 自動制御
    - 直訳すると「自動応答」だが、応答 という言葉はなじみが薄いと考えた
      - なんなら原文で "auto choice" と書かれている部分もあり、response という文意にはたいして執着していないっぽいし
    - OK or Show Message の場合は「～時 (とき) の自動制御」
    - Yes or No or Show Message の場合は「～するかどうかの自動制御」

- single click, double click
  - シングルクリック、ダブルクリック
  - 間をハイフンでつなげている表現があったためそちらへ統一

- machine
  - コンピューター

- low-end
  - (性能の) 低い

- back, next
  - ドキュメント ナビゲーションでのそれは「戻る」「進む」にする

- 際
  - ～する際 は ～するとき と表記する

- () について
  - あまり多すぎる () は不自然なため、極力 排除する
    - 本筋に関連のある内容ならなんとかして () の外へ出す
    - あくまで補足的な内容ならそのままでよい

---

### 気になった点・補足

#### 環境設定 - 一般

- 画像の伸縮
  - なかなかわかりにくい説明。イメージ画像で補足したい
- ドライブ パスに `Subst` を使用
  - `subst` は Windows の仮想ディスクを作成するコマンド
- キーボード ショートカットでワークスペースを閉じるかどうかの自動制御
  - 実は今のところ理解しきれていない。普通にタブでこれをやってみても警告メッセージは表示されなかった。空のタブってなんだ...？ 何も表示されていないワークスペースやドックのタブでは再現できなかった
- ビルド再実行時の自動制御
  - 現在のビルド タスクを中断しますか？ 程度の意味
- ヘルプ マニュアルのポート番号
  - 原文には「デフォルトでは 51291」と書かれているが、翻訳者の環境では 51290 になっていた
- ヘルプに外部ブラウザーを使用
  - 原文には「デフォルトでオン」と書かれているが、翻訳者の環境ではオフになっていた
- 遅いダブルクリックの時間 (ミリ秒)
  - 遅いダブルクリックというか、要は「クリックしてもう一度クリック」である
  - これは Windows でも使えるテクニックなので、そう馴染みの薄いものではないだろう
- テキスト選択にバイアスをかけ誤選択を防ぐ
  - これがまたわかりにくいが、よ～く見てみると数ピクセルほど上下の選択がしにくくなっている
  - これはよく考えられているオプションだと思った
- すべてのデバイスでノートパソコン モードを有効化
  - ノート PC かどうかはバッテリーの有無で確認しているらしく、なんらかの理由でノート PC のバッテリーを取り外して使っているとノートパソコン モードは使えない。このオプションはそういった問題を解決する。それにデスクトップ ユーザーでもトラックパッド愛好家は一定数存在するので有用だ
- 現在開いているウィンドウのみを表示
  - つまり「最近開いたウィンドウ」を毎回リセットするということ
- ワークスペースのキーボード ナビゲーション時の角度範囲
  - なかなか翻訳にてこずった。40°の範囲内に複数のウィンドウがあったらどれが優先されるのだろう。純粋な8方向に最も近いウィンドウだろうか
- ワークスペース チェインのレンダリング セグメント数
  - 要はチェインの解像度である。1 にすれば直線になるし、5 ならカクカクの線に、20 ならなめらかな線になる
- ワークスペース チェインの交差を許可
  - 画像だとオンになっている (実際はオフなのでただのミス？)

#### 環境設定 - Drug and Drop

- ノード全体のドラッグが始まるまでのマウス押下時間 (ミリ秒)
  - これはなかなか絶妙 (褒めているわけではない) な操作で、すぐにドラッグし始めればノードの順番を入れかえ、そうでなければ全体のカメラ移動になる
- サブ カテゴリーである Comments の説明がごっそり抜けている

#### 環境設定 - 画像エディター

- ツール変更時、スプライトの変更を確定するかどうかの自動制御
  - わかりやすいのが円弧ツールなど。まだ確定していないのにペイント ツールに切り替えようとしたりすると確定するかどうかを訊いてくる。これは正直 "メッセージを表示する" から変えられないようにしても良かった気はするが、まぁ個人の判断に委ねられているので
- グリッドの水平スペース
  - 機能していないような気がする、しかも原文のデフォルト値が間違っている (1px となっているが、実際には 16px)
- グリッドの垂直スペース
  - 上に同じ
- デフォルトのスプライト アニメーション速度
  - 例がわかりにくすぎる。要はアニメーション モードの単位がそのまま使われるよということ

#### 環境設定 - スプライト エディター

- デフォルトのスプライト アニメーション モード
  - 画像だと フレーム/ゲーム フレーム になっている (実際は フレーム/秒 なのでただのミス？)
    - そもそもこれはデフォルトの状態を示す画像じゃないのか？ だとしても、あとで差し替えるときにはデフォルトの画像を示します
- デフォルトのスプライト アニメーション速度
  - 原文では「デフォルトでは 30」と書かれているが、翻訳者の環境では 15 だった

#### 環境設定 - オブジェクト エディター

- デフォルトのイベント コンテンツの追加
  - ~~GML ベースのプロジェクトでのみ適用される？~~
  - イベント ペインで各イベントを右クリックして GML に変換すると適用される
- DnD™ を GameMaker Language へ変換するときの自動制御
  - Drug and Drop の環境設定にも同じ項目がある
