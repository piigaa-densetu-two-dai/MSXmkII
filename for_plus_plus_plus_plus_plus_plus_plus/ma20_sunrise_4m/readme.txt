MSXπ✨✨✨✨✨✨✨用のma20とsunriseと4Mマッパーメモリーの複合ファームウェアです。
起動方法、注意事項等はma20/sunriseファームウェアと同じです。

ファームウェア書き込み方法

1. MA-20ロムファイル(NEOSC.ROMとNEOSV.ROM)とSunriseIDE用のNextorカーネルを用意します。

Nextorカーネルは以下からダウンロードして下さい。

https://github.com/Konamiman/Nextor/releases/download/v2.1.2/Nextor-2.1.2.SunriseIDE.MasterOnly.ROM
又は
https://github.com/Konamiman/Nextor/releases/download/v2.1.2/Nextor-2.1.2.SunriseIDE.ROM

(下のファイルを使用すると起動が僅かに遅くなります)

2. ma20_sunrise_4m.binファイルの後ろにNEOSC.ROMとNEOSV.ROMと1でダウンロードしたNextorカーネルを連結します。

unixのcatコマンドを使用する例
$ cat ma20_sunrise_4m.bin NEOSC.ROM NEOSV.ROM Nextor-2.1.2.SunriseIDE.MasterOnly.ROM > firmware.bin

windowsのcopyコマンドを使用する例
>copy /b ma20_sunrise_4m.bin + NEOSC.ROM + NEOSV.ROM + Nextor-2.1.2.SunriseIDE.MasterOnly.ROM firmware.bin

3. uf2conv.exeを用いて2で作成したfirmware.binをuf2ファイルに変換します。

例: windowsコマンドプロンプト上で
uf2conv.exe firmware.bin firmware.uf2

uf2conv.exeはhttps://github.com/piigaa-densetu-two-dai/MSXpi_plus_plus_plus_plus_plus_plus_plus/tree/main/uf2convにあります。

4. MSXに刺さっていない状態のMSXπをブートモードでPCに接続します。

MSXπのBOOTSELボタンを押しながらPCとUSB接続して下さい。
接続が成功するとドライブが認識されます。

5. MSXπに3で作成したfirmware.uf2ファイルを書き込みします。

4で認識されたドライブにfirmware.uf2をドラッグアンドドロップ(コピー)します。
コピーが完了するとドライブが見えなくなります。

6. 書込みが終わったらPCから外して完了
