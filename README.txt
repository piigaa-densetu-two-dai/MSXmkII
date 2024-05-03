MSX②代之家

MSXバージョンアップアダプター非対応ゲームをMSX②代に対応させパッチ(スクリプトです)です。

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

