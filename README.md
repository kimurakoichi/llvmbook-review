llvmbook-review
===============

p9 lilbgcc → libgcc の間違い?
p12 依存パッケージ名にTeXinfo というのがあるが、Texinfo ではないか?
 参考 http://www.gnu.org/software/texinfo/
p14 ■Debugビルドに失敗する場合 に
Debugでも問題なビルドできるということなので
とあるが
問題なく～
の誤り?

p15 ■過去のLLVMをインストールする場合の注意点 に
OcamlとあるがOCaml(Cも大文字)が正しい
 参考 http://caml.inria.fr/

p17 3.3.4 llc の最初の段落
アーキテクチャは-marchオプションで指定できますが, を指定しない場合は入力ファイルから自動的に選択されます。
読点の後の「を」が余計

p23 このページに限らず「浮動少数」となっているが「浮動小数」(浮動小数点数)が正しい
p28 このページに限らず「アライメント」とありますが 「アラインメント」(alignment) ではないでしょうか?
日本語としては「アライメント」で通じると思いますが

p34、35 list4.12やlist4.13ででてくる getelementptr 命令についてくる inbounds が気になるのですが
どこかに説明ないでしょうか?

p40 2重開放→二重解放
SAFE_DELETEマクロについてはその有効性を疑問視する向きもありますがどうでしょうか?
また、delete 対象がNULLかどうかのチェックは冗長のはずです
(delete/delete[]に食わせても問題ないことは規格にあった(はず))

p41 
このあたりからダブルクオートでくくられた用語等が頻出しますが
“” ではなく ”” のように開きのクオート記号が間違ってます。

p45
lexerプログラムですが、66行目で char 変数のアドレスを atoi関数に渡すのは良くありません。

p58 list5.16
@param のあとに「勘数名」というのがありますがこれはなんでしょうか?

p59
プログラムのコメント中に「戻り値」とありますが、ここまでの本文では「返り値」が使われていましたので
統一性に欠けます。本文でも後の方では「戻り値」が使われているようです。

p62 list5.20
13行目から始まる if-else は then 部が大きすぎ、else部が一行しかないので
条件をひっくり返して
 if (!lhs)
   return NULL;

 if (Tokens->getCurType() == ...
とした方が良くはないでしょうか

p69 list5.28
11行目、find関数を呼び出していますが、STLのものならstd::findとした方がよくはないでしょうか?
他のページで使っている vector などでは std::vector となっています。

p80 list 5.38
10行目で vに初期値を入れておらず、最後に return v していますが
vに値が入らないフローはあり得ないでしょうか?

p82
加算、減算、積算、除算とありますが、この積算は乗算の間違いではないでしょうか
http://ja.wikipedia.org/wiki/%E7%A9%8D%E7%AE%97

p97 list5.58
main 関数のインデントが10行目からおかしい

p102
一つ目のメソッドは のあとの doInitialization の配置が変

p116
呼び出し規約で、引数5つ以上は未定義としていますが、p124で
「それ以上に引数がある場合にはスタックに割り当てます」と書いているのと食い違っているような
















