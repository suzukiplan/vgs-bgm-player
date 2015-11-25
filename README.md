# VGS BGM Player
- 本リポジトリでは, VGS BGM Player のサポート情報を記します。
- アプリの使い方などについては [AppStore掲載の情報](https://itunes.apple.com/us/app/vgs-bgm-player/id1056898557?mt=8) をご確認ください。

__[VGS BGM Playerを入手](https://itunes.apple.com/us/app/vgs-bgm-player/id1056898557?mt=8)__

## Dropboxからインポートできるデータ
`vgs2mml` でコンパイル後, `vgs2pack` コマンドでメタデータを付与したデータをインポートできます。
試しに何かしらの曲を入れてみたい場合、東方BGM on VGS の `.vgs` ファイルを以下のリポジトリで公開しているので使ってみてください。

https://github.com/suzukiplan/Touhou-VGS-MML-data

_将来的にはポータルサイトみたいなものを運営したいです_

## VGS BGM Playerで鳴らす音楽データを自作
- VGS BGM Playerで鳴らす音楽データを作成するツール類は、全て無料で公開しています。
- 音楽データの作成には、PC（Mac OS X, Linux または Windows）が必要です。
- 音楽データは、MMLで記述します。

### MMLとは？
- MML（Music Macro Language）とは、テキスト形式の音楽データのことです。
- midi等の祖先だと思っておけば概ね間違いありません。
- 標準的な規格は存在しないので、色々な方言が存在します。

### 一連の手順
1. テキストエディタでMMLファイルを作成
2. [vgs2mmlコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2mml) でコンパイル: MML → BGM
3. [vgs2playコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2play) でBGMファイルを演奏（確認）
4. テキストエディタで metaファイル を作成
5. [vgs2packコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2pack) でBGMファイルとmetaファイルを結合: BGM+meta → vgs
6. vgsファイルをDropboxに格納して VGS BGM Player で import

### VGSのMMLの書き方＆鳴らし方
- VGSのMMLの仕様は [こちらのドキュメント](https://github.com/suzukiplan/vgs2/blob/master/MML.md) を参照してください。
- [東方BGM on VGSリポジトリのdataディレクトリ](https://github.com/suzukiplan/Touhou-VGS-MML-data/tree/master/data) に VGSのMMLで記述された音楽データがあるので、サンプルが必要な方はそちらを参照してください。
- [SUZUKI PLAN - Video Game System MK-II SR](https://github.com/suzukiplan/vgs2) をインストールすればMMLをコンパイル＆演奏することができます。
- MMLのコンパイルには [vgs2mmlコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2mml) を用います。
- コンパイルしたMMLの演奏には [vgs2playコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2play) を用います。

### 作成した音楽データをVGS BGM Playerで演奏
- [vgs2mmlコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2mml) で作成した音楽データは、そのままの状態では VGS BGM Player で演奏することができません。
- 作成した音楽データを VGS BGM Player で演奏するには meta data を記述して、[vgs2packコマンド](https://github.com/suzukiplan/vgs2/blob/master/Command.md#vgs2pack)でBGMファイルとmetaファイルを結合する必要があります。
- meta dataの詳細については[こちらのドキュメント](https://github.com/suzukiplan/vgs2/blob/master/META.md)を参照してください。
