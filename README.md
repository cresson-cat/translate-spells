# translate-spells

Translate the text into Japanese. In addition, google cloud's text-to-speech allows you to read naturally

The following is being written..

----------

1. shellscript の初期設定 >> OK
1. 引数の存在チェック。存在しない場合は処理終了 >> OK
   - そもそも、標準入力に変更する
1. 単語 / 文章をキャッシュしておく。キャッシュミスした場合のみ API を呼ぶ >> OK
   - 400万文字/月以上読み上げなければ課金されないが、念の為
1. usage 関数を作成
1. README 書く
1. ファイルを開けるようにする（-i <file_path>）
1. trans コマンドへ引数を渡せるようにする（-- -b.. のように -- 以降を渡す）
