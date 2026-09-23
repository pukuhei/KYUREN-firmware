# KYUREN

音声で文字を入力し、片手で編集・スクロールするためのデバイスです。
このリポジトリでは、本体のファームウェアとKYUREN Companionを配布します。

## ダウンロード

**現在はテスト版です。** 対応環境と注意事項を確認してからご利用ください。

| 必要なもの | ダウンロード |
| --- | --- |
| Mac用Companion（Apple Silicon、macOS 14以降） | [macOS版 DMG](https://github.com/pukuhei/KYUREN-firmware/releases/download/v2026.09.23-88c23f7c92/KYUREN-Companion-88c23f7c92-macOS-arm64.dmg) |
| Windows用Companion（Windows 11、x64） | [Windows版 EXE](https://github.com/pukuhei/KYUREN-firmware/releases/download/v2026.09.23-88c23f7c92/KYUREN-Companion-88c23f7c92-Windows-x64.exe) |
| KYUREN本体の通常版ファーム | [UF2](https://github.com/pukuhei/KYUREN-firmware/releases/download/v2026.09.23-88c23f7c92/KYUREN-xiao_ble-usb-studio.uf2) |

[すべての配布ファイル・更新内容](https://github.com/pukuhei/KYUREN-firmware/releases) · [検証状況](VERIFICATION.md)

## はじめに

1. Companionをインストールします。MacはDMGを開いてアプリをApplicationsへドラッグ、WindowsはEXEを実行します。
2. アプリを起動し、左メニューの「チュートリアル」を開きます。初回は自動で表示されます。
3. KYURENの電源を入れ、接続します。Windowsでは先にOSのBluetooth設定でペアリングします。
4. 音声入力に必要な許可と自動入力を確認します。Windows版にはWhisper smallが同梱され、Windowsの日本語音声認識機能の追加インストールは不要です。
5. メモ帳などの入力欄を選び、SW6を押したまま話します。離して、文字が入力されるまで待ちます。

音声入力はCompanion経由の文字入力です。会議アプリで選択するBluetoothマイクではありません。

## 本体の操作

図を横向きに見て、左上の切欠きがSW6です。右側の4キーは上段が左SW3・右SW5、下段が左SW2・右SW4、右端の縦長キーがSW1です。

| 操作 | 内容 |
| --- | --- |
| SW6を押して話す → 離す | 音声入力 |
| SW1 / SW2 / SW3 | Backspace / Space / Enter |
| SW4 / SW5 | カーソルを左 / 右へ |
| ノブを回す | 初期設定はスクロール。Companionで音量・明るさ・再生位置にも変更可能 |
| SW1＋SW5 | ジェスチャーの有効・無効 |
| SW2＋SW3＋SW4＋SW5 | トラックパッドの向きを90度変更。OLEDの矢印で上方向を約2秒表示 |
| SW2＋SW4を約0.25秒保持し、ノブを回す | Bluetooth接続先1〜5の切り替え |
| SW1を保持し、ノブを回して離す | Agentの表示セッションを選択・確定 |

Enterはアプリによって送信になります。Agentの選択は表示対象だけで、音声の入力先は変わりません。
トラックパッドの向きは再起動で標準へ戻ります。キー割り当てを独自に変更した場合、上記の操作と異なる場合があります。

## ファームウェアの更新

対象は **Seeed XIAO nRF52840 Senseを使用したKYUREN** です。別の基板には書き込まないでください。

1. USBデータ通信対応ケーブルで接続します。
2. 本体をブートローダモードにします（通常はリセットを素早く2回押します）。
3. `XIAO-SENSE`ドライブが表示されたら、ダウンロードしたUF2をコピーします。
4. ドライブが消えて本体が再起動するまで、ケーブルを抜かずに待ちます。

更新できない場合は、ケーブルとブートローダモードを確認してください。復旧用に過去の配布ファイルもReleasesに残します。

## テスト版の注意事項

- macOS版は開発用署名で、公証されていません。Windows版もコード署名されていません。OSが警告・起動拒否する場合があります。セキュリティ機能を一括で無効化しないでください。
- macOSでは更新後にアクセシビリティなどの許可を確認し直す必要がある場合があります。
- Windowsの音声入力はBluetooth接続を使用します。管理者権限のアプリへは自動入力できない場合があります。
- 明るさ・早送り・巻き戻しはディスプレイやアプリに依存します。
- 乾電池の残量表示は正確ではありません。残量の判断には使用しないでください。
- 実機・初回導入の未確認事項は[検証状況](VERIFICATION.md)に記載しています。

困った場合はCompanionの「チュートリアル」「診断」を確認してください。[Issues](https://github.com/pukuhei/KYUREN-firmware/issues)にはOS・配布日・再現手順を記載し、音声・会話内容・個人情報を含むログは公開しないでください。

第三者ソフトウェアのライセンスは[notices](notices/)およびアプリ同梱の通知を参照してください。
