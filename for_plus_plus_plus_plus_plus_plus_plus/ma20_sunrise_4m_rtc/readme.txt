MSXπ✨✨✨✨✨✨✨用のma20とsunriseと4MマッパーメモリーとRTCの複合ファームウェアです。
起動方法、注意事項等はma20/sunriseファームウェアと同じです。
RTC機能入りなのでMSX+Nextorで時刻を扱うことが出来ます。別途、DS3231モジュールが必要です。(モジュールが無いと起動しません)

ご注意
時刻の取得・設定のみに対応です。アラーム機能や不揮発RAM機能は機能しません。

RTC結線方法

MSXπ側  DS3231モジュール側
VCC     VCC
GND     GND
IO32    SDA
IO33    SCL

aliexpress等で安価に販売されているDS3231モジュール(DS3231.png参考)には充電回路が組み込まれています。
一次電池のCR2032を使用する場合はDS3231.pngの通りにチップを取り外すことをお勧めします。

ファームウェア書き込み方法

1. MA-20ロムファイル(NEOSC.ROMとNEOSV.ROM)とSunriseIDE用のNextorカーネルを用意します。

Nextorカーネルは以下からダウンロードして下さい。

https://github.com/Konamiman/Nextor/releases/download/v2.1.2/Nextor-2.1.2.SunriseIDE.MasterOnly.ROM
又は
https://github.com/Konamiman/Nextor/releases/download/v2.1.2/Nextor-2.1.2.SunriseIDE.ROM

(下のファイルを使用すると起動が僅かに遅くなります)

2. ma20_sunrise_4m_rtc.binファイルの後ろにNEOSC.ROMとNEOSV.ROMと1でダウンロードしたNextorカーネルを連結します。

unixのcatコマンドを使用する例
$ cat ma20_sunrise_4m_rtc.bin NEOSC.ROM NEOSV.ROM Nextor-2.1.2.SunriseIDE.MasterOnly.ROM > firmware.bin

windowsのcopyコマンドを使用する例
>copy /b ma20_sunrise_4m_rtc.bin + NEOSC.ROM + NEOSV.ROM + Nextor-2.1.2.SunriseIDE.MasterOnly.ROM firmware.bin

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
