# grass7ja

GRASS GIS 7.0.3 リリースにともなう、日本語poファイルのメンテナンス

## Usage
1.grass7ja を GitHub Desktop でローカルにクローン  
2.作業状況は、開始時にissueに記載：ファイル名と編集予定範囲  
3.各自ファイルを修正。  
grass7po/grasslibs_ja.po が分量が多いので、手分け。  
全部が日本語訳にする必要はないと思いますが、その場合は英語をコピーしてください。

###メンテナンス対象例および確認箇所：
__・日本語訳がない__  
    `＃: ../lib/display/r_raster.c:128`  
    `＃, c-format`  
    `msgid "%s variable defined, %s ignored"`  
    `msgstr ""`  

__・元が１行なのに２行になってる__  
    `＃: ../lib/driver/parse_ftcap.c:84`  
    `＃, c-format`  
    `msgid "%s: Unable to read font definition file; use the default"`  
    `msgstr ""`  
    `"%s:フォントの定義ファイルが読み取れません;  デフォルト値を使用してください"`

__・変換文字列が化けている__  
    `#: ../lib/display/icon.c:80`  
    `#, fuzzy, c-format`  
    `msgid "Unsupported icon %d"`  
    `msgstr "���"`

__・重要チェック項目  このケースはプログラムがクラッシュする__  
    `#: ../lib/manage/do_copy.c:43`  
    `#, fuzzy, c-format`  
    `msgid "Copy %s <%s> to current mapset as <%s>"`  
    `msgstr "���"`


__・その他一応チェック必要  ヘッダにfuzzyがついてる。__  
    `#, fuzzy, c-format`  

***
Dear translators,

in preparation of the new stable release GRASS GIS 7.0.3 we would like
to invite you to check and update your favourite translation.

Please be sure to work on the latest .po message files which you can
download from either

 https://svn.osgeo.org/grass/grass/branches/releasebranch_7_0/locale/po/

or

 https://svn.osgeo.org/grass/grass/trunk/locale/po/

Please send the (even partially) updated files to me at any time for
upload. Merging is easy for me :)

Best
Markus

