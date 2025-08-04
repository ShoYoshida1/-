# ROS 2 Bag Trimmer (Python Script)

このPythonスクリプトは、ROS 2のbagファイルを時間指定で簡単にカット（トリミング）するためのコマンドラインツールです。記録の開始時点からの**相対時間（秒）**で範囲を指定できるため、タイムスタンプを計算する必要がなく、直感的に操作できます。

## 概要 (Description)

長時間の記録で肥大化したbagファイルから、解析やデバッグに必要な部分だけを効率的に抽出することを目的としています。

## 要件 (Requirements)

* **ROS 2 (Humble)**
* **Python 3**

## 使い方 (Usage)

**スクリプトの実行**
以下の形式でコマンドを実行します。

    python3 bag_trimmer.py <入力bagディレクトリ> <出力bagディレクトリ> [オプション]
## 実行例 (Example)

### 例: 記録の10秒後から60秒後までを切り出す

`long_bag_source`というディレクトリにあるbagファイルを、記録開始10秒後から60秒後までの範囲でカットし、`short_clip_10_60`という名前で保存する場合：

```
python3 bag_trimmer.py long_bag_source short_clip_10_60 --start 10 --end 60
```
