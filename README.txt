MSX②代之家

MSX②代標準ファームウェア
ma20_a.bin
ma20_o.bin

MSX②代標準ファームウェア(RP5C01機能なし) こちらの方がMSX本体との互換性が高いそうです。上の奴で不具合が出る場合はこちらを使ってください。
ma20_nortc_a.bin
ma20_nortc_o.bin

MSX②代日本語USBキーボード対応ファームウェア
ma20_kbd_a.bin
ma20_kbd_o.bin
readme_keyboard.txt (説明)
keymap.png (キーマップ)

trueMSX②代ファームウェア
trueMSX2_a.bin
trueMSX2_o.bin

以下MSXバージョンアップアダプター非対応ゲームをMSX②代に対応させパッチ(スクリプトです)です。

ファンタジーゾーンII
perl -p -i -e 's/\xd3\x98/\xd3\x88/g' romfile
perl -p -i -e 's/\xd3\x99/\xd3\x89/g' romfile
perl -p -i -e 's/\xdb\x99/\xdb\x89/g' romfile
perl -p -i -e 's/\xd3\x9a/\xd3\x8a/g' romfile

R-TYPE
perl -p -i -e 's/\xd3\x98/\xd3\x88/g' romfile
perl -p -i -e 's/\xd3\x99/\xd3\x89/g' romfile
perl -p -i -e 's/\xd3\x9a/\xd3\x8a/g' romfile
perl -p -i -e 's/\xdb\x98/\xdb\x88/g' romfile
perl -p -i -e 's/\x0e\x98/\x0e\x88/g' romfile
perl -p -i -e 's/\x0e\x88\x00/\x0e\x98\x00/g' romfile
perl -p -i -e 's/\xc3\x0e\x88/\xc3\x0e\x98/g' romfile
perl -p -i -e 's/\x0e\x9a/\x0e\x8a/g' romfile
perl -p -i -e 's/\x0e\x8a\x00/\x0e\x9a\x00/g' romfile
perl -p -i -e 's/\x0e\x99/\x0e\x89/g' romfile

TETRIS
perl -p -i -e 's/\x3e\x98/\x3e\x88/g' romfile
