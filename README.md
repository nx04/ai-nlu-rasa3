# ai-rasa

## 软件要求：
```
# python 3.8

# python3.8 依赖包 rasa==3.0.8

pip3.8 install rasa==3.0.8 -i https://pypi.tuna.tsinghua.edu.cn/simple
```

## Training NLU-only models

```
rasa train nlu
```

## Testing your NLU model on the command line

```
rasa shell nlu
```

或者 

```
rasa shell -m models/nlu-20190515-144445.tar.gz
```

## Running an NLU server

```
rasa run --enable-api -m models/nlu-20190515-144445.tar.gz
```

You can then request predictions from your model using the /model/parse endpoint. To do this, run:

```
curl localhost:5005/model/parse -d '{"text":"hello"}'
```



