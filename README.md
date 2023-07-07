# FunKeyOS-game_de_it

## ●特徴
---  
- [NEW] Bluetoothでオーディオ出力が可能になりました  
  - ボリューム調整はスピーカーやヘッドセット側で行ってください 
- [NEW] picoarch(retroarchのSDL版)が利用可能になりました
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

## ●picoarchエミュレータ情報
```
●拡張子表
fmsx(MSX)
  [rom,mx1,mx2,dsk,cas]

fceumm(NES,Disksystem)
  [fds,nes,unf,unif]

gambatte(GB,GBC)
  [gb,gbc,dmg,zip]

genesis-plus-gx(GG,MD,SMS,MEGACD)
  [bin,gen,smd,md,cue,iso,chd,sms,gg,m3u,68k,sgd]

gpsp(GBA)
  [gba,bin,zip]

mgba(GBA)
  [gba,bin,zip]

pce-fast(PCE,CD-ROM2)
  [pce,cue,ccd,chd,toc,m3u]

pcsx_rearmed(PS1)
  [iso,bin,cue,img,mdf,pbp,toc,cbn,m3u,chd]

snes9x2005(SNES)
  [smc,fig,sfc,gd3,gd7,dx2,bsx,swc,zip]

```

##  ●ダウンロード方法や使い方  
画面右にある「Releases」からダウンロードや使い方を確認できます  

##  ●今後の取り組み
- USB-DACを利用できるようにする(なんかできそうな予感6/27)
  - ベータ版で実装しましたが引き続き作業中
  - RETROFE実行中はCPU使用率が高くなる現象を確認
- retroarchの導入
- 音楽＆動画再生プレイヤーの導入
- 画面60Hz対応
- SFCの動作改善とBGMを正常に鳴らすこと
- ファーストフォワード(早送り機能)の実装
- ファンクションキー＋LRでステートセーブ、ロードの実装
- スクショ用にポーズ機能の実装
- スリープ機能の実装
  -  FunKeyOS-game_de_it_2にて「START+Aボタンでシャットダウン」機能が追加され、擬似的なハイバネーションが実現しました  
再び電源オンにすると終了したところからゲームが再開されます
- 日本語化
    
## ●リリースファイル名の改訂とご紹介  
FunKeyOSベースのカスタムファームウェアを継続してリリースをするにあたり、  
今回からリリースファイル名を「FunKeyOS-<形式>-<公式Ver>-game_de_it_<ナンバリング>」として生まれ変わりました！  
新たなリリースをするたびにナンバリングの数値が増えていきます。  
