# RecordNoteApp

## 概要と進捗状況

AdobeXDで少し作ってみたプロトタイプ
![demo](https://github.com/amaocha-first/RecordNoteApp/blob/media/RecordNoteAppDemo.gif)

現在制作中のオリジナルアプリ。  
当初は、メモアプリとボイスメモアプリとTODOアプリを一緒にして、多機能メモアプリとして考えていた。  
しかし、現在ではターゲットをもっと絞り込んで、作曲時の補助ツールアプリにしていこうと考えている。  

基本機能は、
* 歌詞制作(テキストメモ)
* メロディーメモ(録音)
* コード進行メモ
これら３つができて、作曲時に便利なメモツールにしたい。

今の段階で、コード進行関係以外の主要機能はだいたい実装できた。

## このアプリの特徴 

ただのメモアプリやボイスメモアプリとの決定的な違いは次の２つである。

### 特徴１：歌詞(テキスト)とメロディー(オーディオ)が同じ場所で管理できる。

歌詞とメロディーは基本セットなので、同じ場所で関連づけて保存や管理をしたい。  
そのため、今回はTabBarとRDBMSを使って、これを実現させる。  

また、これにより歌詞を見ながら録音することもできたり、録音したものを再生しながら歌詞を見ることもできる。　　

### 特徴２：コード進行のメモがしやすい
まず、コード進行を歌詞と一緒にメモするときに大変だと感じるのは理由が２つある。

* 英数字や記号の変換が多い
* 任意の位置に置くためにspaceを入れないといけない

手打ちで、こうしたコードを打ち込もうとするとすごくめんどくさい。(ex.「シャープの記号どこ？」、「記号と数字の切り替え多い！」など)

これらを解決して簡単にメモできるようにするために、今回のアプリではフリック入力のようなUIとドラッグアンドドロップを活用しようと考えている。  

参考
![sampleImage01](https://github.com/amaocha-first/RecordNoteApp/blob/media/RecordNoteAppImage01.png)

![sampleImage02](https://github.com/amaocha-first/RecordNoteApp/blob/media/RecordNoteAppImage02.png)


また、コードは何種類もあるが、基本的にはキーを選択すれば、ダイアトニックコードが下のUIに自動で表示される。  
その他の特別必要なコードもCustomで登録できる。




