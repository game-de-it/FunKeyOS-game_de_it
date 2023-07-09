# FunKeyOS-game_de_it

## 特徴
---  
- [NEW!!] ffplayに以下の機能を追加しました
  - ランダムプレイリスト再生
    - Mediaフォルダ内の「PlayList」というファイルを再生すると、Mediaフォルダ内にあるファイルから自動的に50曲をランダム再生します 
    - 2バイト文字非対応のため[ファイルとフォルダをすべて連番にリネームする手順](https://github.com/game-de-it/RGnano/blob/main/rename.md)を参考にしてください 
  - ファイル単体再生時にシーク操作ができるようになりました
```
●ffplayキー操作一覧
十字キー　↑ [60秒　先にスキップ]
十字キー　↓ [60秒　後ろにスキップ]
十字キー　→ [10秒　先にスキップ]
十字キー　← [10秒　後ろにスキップ]
STARTボタン [一時停止]
電源ボタン [再生終了]

※ランダムプレイリスト再生中は[一時停止]と[再生終了]しか操作ができません
```
- picoarch pokeminiエミュレーターを追加しました
- ffplayで音楽と動画が再生が可能になりました
  -  情報提供者 [ Twitter : じゅんたろう @GameboyJuntaro ] ありがとうございます！
- Bluetoothでオーディオ出力が可能になりました  
  - ボリューム調整はスピーカーやヘッドセット側で行ってください 
- picoarch(retroarchのSDL版)が利用可能になりました
  -  対応エミュ：MSX,NES,SNES,MD,GG,PS1,GB,GBA,PCE  
     - 32Xは既存のpicodriveを利用してください 
  - FF(早送り)の設定手順
    - ゲーム中に電源ボタン→ADVANCED→Options→Emulator controls→Toggle FF　でお好きなボタンに割り当ててください
    - 設定を保存する場合はSave config→Save global config　で保存してください
  - GBパレット(配色)の設定手順
    -  ゲーム中に電源ボタン→ADVANCED→Options→Emulator options→GB Colorization　で変更できます
    - GBCのパレットはInternal Palette GB　で変更可能です
-  USB-DACが利用可能
- 「START+Aボタン」でシャットダウンできるようになりました  
(この機能を利用してゲーム中にシャットダウンしても、再度電源ONでゲームを再開できます)  
- FunKeyOS-2.3.0ベースで作られたカスタムファームウェア
- RETROFEフロントエンドで利用できるテーマ「RetroRoomCovers」を搭載  
- picodrive-funkeyベースの「GameGear pico」を搭載
[picodrive-funkey](https://github.com/DrUm78/picodrive-funkey)を利用して新たなエミュレータとして「Game Gear pico」を作成し、既存のGame Gear(mednafen)と共存させています。  
公式のFunkeyOSではGame Gearでスケーリングを変更できませんでしたが「Game Gear pico」を利用することでGame Gearでもスケーリングが変更可能になります。  
- [システムステータス表示にてバッテリー残量を表示する機能](https://github.com/game-de-it/RGnano/blob/main/battery.md)を搭載  
- [ゲーム中のスナップショットがゲームのサムネイルになる機能](https://github.com/game-de-it/RGnano/blob/main/snapshot.md)を搭載  
- **__注意__**  
   - GMenu2xでのみGame gear picoは動作します(RETROFEでの動作は調査中です)  
  - このアップデートイメージファイルは公式のFunKeyOS、および私のGithubで公開しているFunKeyOSベースのカスタムファームウエアにのみ適用できます  
(AnbernicOSにこのファイルを置いてもアップデートは動作しません)  
  - アップデートする場合はROMファイル、サムネイル画像、セーブデータはそのまま保持されます
  - これらのアップデートイメージを適用した上で公式のアップデートイメージを適用した場合、本機能は全て削除されてしまいます

##  ●ダウンロード方法や使い方  
画面右にある「Releases」からダウンロードや使い方を確認できます  

##  ●今後の取り組み
- 2バイト文字対応
- USB-DACを利用できるようにする(なんかできそうな予感6/27)
  - ベータ版で実装しましたが引き続き作業中
  - RETROFE実行中はCPU使用率が高くなる現象を確認
- picoarchの導入(2.1.0で実装)
  - ファーストフォワード(早送り機能)の実装(2.1.0で実装)
  - ステートセーブ、ロードの実装(2.1.0で実装)
- 音楽＆動画再生プレイヤーの導入
- 画面60Hz対応
- SFCの動作改善とBGMを正常に鳴らすこと(性能的に無理っぽい)
- スクショ用にポーズ機能の実装(難しそう)
- スリープ機能の実装
  -  FunKeyOS-game_de_it_2にて「START+Aボタンでシャットダウン」機能が追加され、擬似的なハイバネーションが実現しました  
再び電源オンにすると終了したところからゲームが再開されます
- 日本語化
    
## ●リリースファイル名の改訂とご紹介  
FunKeyOSベースのカスタムファームウェアを継続してリリースをするにあたり、  
今回からリリースファイル名を「FunKeyOS-<形式>-<公式Ver>-game_de_it_<ナンバリング>」として生まれ変わりました！  
新たなリリースをするたびにナンバリングの数値が増えていきます。  
