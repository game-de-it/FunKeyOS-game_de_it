# FunKeyOS-game_de_it
  

## リリースファイル名の改訂とご紹介  
FunKeyOSベースのカスタムファームウェアを継続してリリースをするにあたり、  
今回からリリースファイル名を「FunKeyOS-<形式>-<公式Ver>-game_de_it_<ナンバリング>」として生まれ変わりました！  
新たなリリースをするたびにナンバリングの数値が増えていきます。  

## 特徴
---  
- [NEW] 「START+Aボタン」でシャットダウンできるようになりました  
(この機能を利用してゲーム中にシャットダウンしても、再度電源ONでゲームを再開できます)
- FunKeyOS-2.3.0ベースで作られたカスタムファームウェア
- RETROFEフロントエンドに「RetroRoomCovers」テーマを搭載  
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

##  今後の取り組み
- USB-DACを利用できるようにする
- SFCの動作改善とBGMを正常に鳴らすこと
- ファーストフォワード(早送り機能)
- ファンクションキー＋LRでステートセーブ、ロードの実装
- [解決？]スリープ機能の実装
  -  FunKeyOS-game_de_it_2にて「START+Aボタンでシャットダウン」機能が追加され、簡易的なハイバネーションが実現しました  
再び電源オンにすると終了したところからゲームが再開されます
- 日本語化


##  ダウンロード方法や使い方  
画面右にある「Releases」からダウンロードや使い方を確認できます
