<!-- このステップでは　my-resume を個人の端末にクローン(複製)する処理を書く -->

## Step 2: クローンの作成と修正

インターネット上に存在するGitHubのリポジトリデータをローカルの端末にダウンロードして修正することも可能です。
そうしておけば、新幹線や飛行機で出張している状況でもオフライン且つ高速な作業環境が実現できます。実験的な変更を加える場合やバックアップを取得したい場合にも役立ちます。
<!-- オーバービューを書く -->

### :keyboard: VSCodeのインストールとブランチの作成

今回はVSCodeを使ってローカルにリモートリポジトリのクローンを作成するため、事前に[VSCodeをインストール](https://azure.microsoft.com/ja-jp/products/visual-studio-code)します。

1. VSCodeのインストールが完了したら、[Git](https://git-scm.com/)をインストールします。VSCodeの拡張機能である[GitHub Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions)、[GitGraph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)、[GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)もインストールします。
1. 次にGitHubの画面で「<>Code」のボタンを押下し、表示されるHTTPSのURLをコピーします(コピーアイコンを押す)。
1. VSCode画面左のアクティビティバー「リモートエクスプローラー」を押下し、リモートリポジトリの追加「+」を押します。
1. 上部の検索バーに「GitHubからリポジトリを開く」を押し、先ほどコピーしたURLを入力し実行します。VSCode上にリモートリポジトリが表示されます。
1. デフォルトで main ブランチが選択されています。[最初の手順](https://github.com/kuboctopus/dodge-merge-conflict/blob/main/README.md)で作成した自分専用のmy-resume ブランチに切り替える必要があります。VSCodeの画面の左下に表示される「main」を押下し、「my-resume」を選択します。

<!-- 5. VSCodeの左ペインの「ソースの管理」を押下し、そのリポジトリを選択した状態で、「...」を押し、「ブランチ-ブランチの作成」を選びます。
6. 上部の検索バーにフォーカスが移動しますので、任意のブランチ名(name_yyyymmdd 等)を入力し、実行します。 -->

### :keyboard: ローカル端末へのクローンの作成

作成したブランチをローカルの端末に保存します。以下手順を記載。

1. VSCodeの画面左下にある「>< GitHub」を押下し、「新しいローカルクローンで作業を続ける」を押します。
1. 「はい、作業中の変更を使って続行します」を選択します。必要に応じてGitHubの認証を行い、ローカル端末のリポジトリの保存先を選択します。
1. 「複製したリポジトリを開きますか? または現在のワークスペースに追加しますか?」というメッセージダイアログが表示されるので、「開く」ボタンを押下します。
1. エクスプローラーで指定した保存先にリポジトリに含まれるフォルダとファイル群(dodge-merge-conflict 以下)が保存されていることを確認します。

以上でローカル端末へのクローン作成は完了です。

<!-- このステップでは　my-resume を修正しプルリクエストを行いマージコンフリクトが発生しないことを書く -->

## Step 3: ブランチの修正とプルリクエスト

先ほどローカルに複製したリポジトリのブランチ my-resume を修正し、リモートリポジトリの main ブランチとマージするためにプリリクエストを発行します。

### :keyboard: ブランチの修正

1. 先ずは、VSCodeの画面左下を確認し、選択中のブランチが「my-resume」になっていることを改めて確認します。
1. アクティビティバーのエクスプローラーが選択され、ブランチのツリーが表示されている箇所のアイコン![新しいファイル...](https://github.com/kuboctopus/dodge-merge-conflict/blob/main/.github/steps/img/add_file01.png)「新しいファイル...」を押下し、ファイル名「references.md」を作成します。 references.md に任意の文字列を入力し、保存します。
1. VSCodeの画面左側のツールバーの「ソースの管理」を押下し、変更メッセージに任意の文字列を入力、「コミット」ボタンを押下します。
1. ステージの確認メッセージが表示された場合は、「はい」を押します。更に、ボタンのテキストが「変更の同期」に変更されたら、押下します。

### :keyboard: プルリクエスト

1. GitHubの画面を表示し、「Pull requests」のリンクを押します。
1. 「Compare & pull request」のアイコンが表示されていますので、押下します。
1. 画面をスクロールし、修正内容を確認、任意のコメントや説明を入力、「Create pull request」を押下します。
1. 最後に、「No conflicts with base branch」(コンフリクト無し)のメッセージを確認し、「Merge pull request」を押します。

約20秒待ってから、このページ(あなたが指示を受けているページ)を更新してください。GitHub Actionsが自動的に次のステップに更新されます。

<!-- ymlでマージコンフリクトが発生しない処理を書く -->


