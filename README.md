# ROS2用CPU使用率モニタコマンドパッケージ

## 概要
- 本パッケージはCPU使用率を取得してROS2のトピックとして配信するノードと、その情報を読み込み表示するノードから構成されるROS2パッケージです。

## 機能概要
- システムのCPU使用率を一定周期で取得します。
- 取得したCPU使用率はROS2のトピック通信を用いて配信されます。
- PublisherノードがCPU使用率を取得し、数値データとしてPublishします。
- Subscriberノードがトピックを読み込み、受信したCPU使用率を標準出力に表示します。

## 使用方法

### 必要なライブラリをインストールしてください。
- 以下のコマンドを実行してください。
```
pip3 install psutil
```

### 実行方法

#### CPU使用率を取得するには、以下のノードを実行します。
```
ros2 run robosysros2_pkg cpu_usage_publisher
```
#### CPU使用率を取得するには、以下のノードを実行します。
```
ros2 run robosysros2_pkg cpu_usage_listener
```
- 実行例

#### Subscriber
```
[INFO] [cpu_usage_listener]: Listen: CPU Usage: 12.5%
```

## テスト環境
```
OS: Ubuntu 22.04
ROS 2: Humble Hawksbill
Python: 3.10
```

## 必要なソフトウェア
```
ROS 2 Humble Hawksbill
Python 3.10
psutil (CPU 使用率取得のため)
```

## ライセンス
- このソフトウェアパッケージは、3条項BSDライセンスの下、再頒布及び使用が許可されます。
- © 2025 Rintatrou Matunaga
