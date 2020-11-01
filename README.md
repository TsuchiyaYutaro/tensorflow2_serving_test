# TensorFLow 2.0 のテスト
TensorFlow 2.0 から Serving を使いモデルデプロイを簡単にできるようになったためそのテスト

# setup
### モデル作成
```
$ python train.py
```
### エンドポイント作成
```
$ docker-compose up
```
### テスト
```
$ curl -X POST -H "Content-Type: application/json" http://localhost:8501/v1/models/fashion_model:predict -d @test_data.json
```