ほしの すうじカードバトル - GitHub Pages 安定版

【GitHubへの入れ方】
1. ZIPをそのままGitHubにアップロードしないでください。
2. ZIPを展開します。
3. 展開した中の index.html と cards フォルダを、GitHubリポジトリの一番上（ルート）にアップロードします。
4. 構成が次の形になっていることを確認してください。

   index.html
   cards/
     number_0.jpg
     number_1.jpg
     ...

【カードを追加する方法】
1. 新しいカード画像を cards フォルダへ追加します。
   例：cards/number_10.jpg
2. index.html の CARD_MASTER に1件追加します。

   {
     id: "number_10",
     name: "ほしのゆうしゃ",
     number: 5,
     image: "cards/number_10.jpg",
     rarity: "R"
   }

3. 保存してGitHubへ反映します。

【重要】
・画像はindex.htmlにBase64埋め込みしていません。
・ゲーム本体のindex.htmlはカード画像の追加分だけ大きくなることはありません。
・画像は index.html からの相対パスで読み込みます。
・GitHub Pagesの「リポジトリ名/」のようなサブフォルダ公開でも動くよう、document.baseURIを基準に画像URLを解決します。
・カード画像が読み込めない場合は、数字の代替表示を出してゲーム画面が壊れないようにしています。

【現在登録されているカード】
number_0 ～ number_9：10枚
SRカード：3枚

【保存】
カード所持数、デッキ、星のかけらは、この端末のブラウザのlocalStorageに保存します。
