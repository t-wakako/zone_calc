# zone_calc
##露出計の測定値から絞り、シャッターの組み合わせを表示します。
##Classic Meterはpentax等です。ModernはSekonic等です。
##Modernの時は実効感度を変えても、絞り、シャッターの組み合わせは変わりません。メモ用途です。


##11/3の機能追加

以下のように呼び出した時
https://t-wakako.github.io/zone_calc/index.html?ev=xx.xx
modernモードでev値を設定して表示する。
ただし、計算に使用するev値はこれまで同様1/3段単位
また、evパラメタを使用した場合、アプリに戻れるボタンが表示されるようにする。

<メモ>
iPhoneアプリ側の設定
Xcodeでアプリのターゲットを選択し、次の設定を行います。
Target → Info → URL Types
例えば次のように登録します。
項目	設定値
Identifier	com.example.spotmeter
URL Schemes	spotmeter
Role	Editor
これにより、次のURLでアプリを開けるようになります。
spotmeter://return

SwiftUIアプリでは、必要に応じて次のように受信できます。
.onOpenURL { url in
    if url.scheme == "spotmeter",
       url.host == "return" {
        // スポットメーター画面に戻す
    }
}

##11/4の機能追加
パメラタ追加、iso、note、fそれぞれ開く時に選択状態になるようにした。
アプリ戻る時にパラメタの内容を渡せるようにした。


