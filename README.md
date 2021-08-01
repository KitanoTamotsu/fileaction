## 　　Lesson29.　Alfredのファイルアクションを使ってみる  
#### 開発メモ

[サンプル動画](https://user-images.githubusercontent.com/40127279/126054996-3003dc96-eb11-4521-a336-76e790c7b97c.mp4)
ワークフロー
<br><img width="600" src="https://user-images.githubusercontent.com/40127279/127757814-605572a6-cac6-4383-9583-11c8171a071f.png">


### 1.alfredのファイル操作を理解する
　alfredバーから目的のファイルに辿り着く方法は2つあります
<br>　
<br>　ひとつ目はファイル名を検索する方法
<br>　alfredバーに『'』を入力してから、検索ワードを記入するだけです
<br>　リターンエリアに検索結果が表示されるので『↑』『↓』でアイテムを選択します
<br>　選択したら『→』でファイルアクションが表示されます　
<br>
<br>　ふたつ目はパスを入力してナビゲートする方法
<br>　alfredバーに『/』を入力するとルートディレクトリがリターンエリアに表示されます
<br>　こちらの場合はフォルダも表示されるので、配下のフォルダをたどることができます
<br>　文字を入力することも可能です
<br>　例えば『/』のあとに『u』を入力して、表示されるusersのフォルダーを選択するみたいな
<br>　操作ができます
<br>　上記同様、ファイルアイテムを選択中に『→』でファイルアクションが表示されます
<br>　ちなみに、alfredバーに『~』を入力するとホームディレクトリにショートカットできます
### 2.alfredのファイル操作をカスタマイズする
　フォルダーの移動がデフォルトでは『⌘↑』『⌘↓』ですが、『←』『→』に変更できます
<br>　上位/下位フォルダへの移動なのですが、左右の矢印の方が直感的にわかりやすいですし、
<br>　アイテムの移動が『↑』『↓』であることを考慮すると誤操作もなくなると思われます
<br>　
<br>　設定方法です
<br>　alfredの設定パネルでFileSearchのNavigationタブを開いて
<br>　Shortcuts: □ Use ← and → for folder navigationのチェックボックスをオンにします
<br>　<img width="600" src="https://user-images.githubusercontent.com/40127279/127757869-cca24a50-8ae2-4806-909e-292c8fa2e50a.png">
<br>　これに伴ってファイルアクション表示（デフォルトで『→』）の変更が必要です
<br>　alfredの設定パネルでActionsのGeneralタブを開いて
<br>　Show Actions: □→ □fn □cntl □⇥ to action selected itemのチェックボックスをオンにすると
<br>　そのキーでファイルアクションを表示できるようになります
<br>　右矢印キー、ファンクションキー、コントロールキー、タブキーの4つが選べます
<br>　複数を選択した場合、それぞれの単独キーで機能します
<br>　<img width="600" src="https://user-images.githubusercontent.com/40127279/127757878-d4a9212e-3230-4aba-8be6-7d1cb7876add.png">
<br>　因みに私はファイルアクションの表示はcntlのチェックボックスをオンにしています
<br>　なぜなら、alfredバーから『⌃』『/』で前回フォルダの表示ができるので、
<br>　同じフォルダ内のファイルを操作する際に親和性があるからです
<br>　即ち
<br>　　『⌃』『/』でフォルダ表示
<br>　　『↑』『↓』でファイル選択
<br>　　『⌃』でファイルアクション表示という流れです
<br>　　単なる好みですね
### 3.FileActionのワークフローを作成する
　ワークフローはいたってシンプルです
<br>　trrigersとしてFileActionを配置します
<br>　ファイル数やファイルタイプの設定が可能です
<br>　ファイルタイプは開きたいファイルをドラッグ＆ドロップするだけの簡単設定です
<br>　<img width="600" src="https://user-images.githubusercontent.com/40127279/127757891-d9925875-ef5d-45bb-93b8-4c6839c6ecf1.png">
<br>　次にフローの後続としてActionsからOpenFileを選択して繋げます
<br>　設定は簡単で、右のボックスにファイルを開くためのアプリをドラッグ＆ドロップするだけ
<br>　<img width="600" src="https://user-images.githubusercontent.com/40127279/127757910-35d0bd8a-1b75-448e-82ad-2190e1468646.png">
### 4.さらなるカスタマイズ
  試してみるとファイルアクションの最下部に今回作成したアクションが表示されるのですが
<br>　それそ選択するのが煩雑でした
<br>　そこで、ファイルアクションの表示順を直近で利用したものから表示させるようにします
<br>　alfredの設定パネルでActionsのGeneralタブを開いて
<br>　Action Ordering:□Sort actions by last used par typeのチェックボックスをオンにします
<br>　これで、よく利用するものが上位に来るようになり、ファイルアクションをエンター一発で
<br>　起動できるようになります　
### 最後に
　今回のLessonは全てをキータイピングで操作するalfredの本領発揮というような気もします
<br>　今まではmacOSの『このアプリケーションで開く』からLuminarAIを開いていました
<br>　どちらも似たようは効率でしたので、使うかどうかは好みという気がします
<br>　jpgファイルで言えば、ぱっと見はクイックルックでみれるので、jpgのデフォルトアプリを
<br>　編集ソフトにするのが一番かも
<br>　もちろんalfredでもデフォルトアプリでのopenをサポートしています
<br>
#### 背景
　Alfredのファイル操作系の機能を使ってみたくなり試しました
<br>　たまに写真編集ソフトLuminarAIを使うことがあるので、LuminarAIで開くというシンプルな
<br>　ファイルアクションを題材としました。
<br>　LuminarAIは有料なので導入している方は少ないと思います
<br>　プレビュー.appなどに置き換えても試せると思います
#### 取扱説明
### 機能:
　LuminarAI.appで開く（ファイルアクション）
### インストール:
　1.[Alfredworkflow](https://github.com/KitanoTamotsu/fileaction/releases/download/1.0/Open.in.Luminar.AI.alfredworkflow.zip)をダウンロード 
<br>　2.ファイルをダブルクリックしてワークフローに登録
### 使い方:
  Alfredでファイル選択中にShowAction（デフォルトでは『→』キー）を実施
<br>
<br>
[トップページに戻る](https://kitanotamotsu.github.io/)

