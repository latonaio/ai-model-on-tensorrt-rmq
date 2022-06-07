# ai-model-on-tensorrt-rmq
ai-model-on-tensorrt-rmq は、TensorRT 上で 動作させた AIモデル からのアウトプットとして、1/10/100ミリ秒のタイムサイクルで、マイクロサービス間の効率的・安定的処理が可能な RabbitMQ へメッセージを JSON 形式で出力するマイクロサービスです。
本マイクロサービスは、単体で動作せず、TensorRT 上で 動作させた AIモデル からのアウトプットとしてRabbitMQ へメッセージをJSON 形式で出力するマイクロサービス作成時の、参照元となるマスタレポジトリです。  

## 動作環境
- C
- C++
- Docker
- TensorRT Runtime


## 動作手順
### Dockerコンテナの起動
Makefile に記載された以下のコマンドにより、AIモデル の Dockerコンテナ を起動します。
```
docker-run: ## Docker ストリーミング用コンテナを建てる
	./docker/run.sh
```

### ストリーミングの開始
以下のコマンドにより、DeepStream 上の AIモデル でストリーミングを開始します。  

```
XXXXXXXXXXXXXXXXXXXXX /dev/video0
```

## engineファイルについて
本レポジトリのengineファイルは、XXXXXXXXXXXXXXXXXXXXXXXXX にあります。  
なお、AIモデル の NVIDIA Jetson用の engineファイルは、XXXXXXXXXXXXXXXX からダウンロードできます。  

## RabbitMQ への JSON Output
ai-model-on-tensorrt-rmq は、Outputとして、RabbitMQ へのメッセージをJSON形式で出力します。  
サンプルのJSONファイル は、Outputs フォルダ内の sample.json にあります。  
本レポジトリでは、例として、[multihumanparsing-on-tensorrt-rmq](https://github.com/latonaio/multihumanparsing-on-tensorrt-rmq) のサンプルJSONが格納されています。  

