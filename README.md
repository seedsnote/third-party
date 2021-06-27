
## Try it now

如果你想找寻好用的Seeds思记第三方工具，或提交你的作品，请移步到 [Discussion](https://github.com/seedsnote/third-party/discussions/categories/ideas-tools)

## Documentation

Seeds API采用典型的POST请求方法，支持将文本和图片发送到Seeds

1. 如果是文本，请使用content字段名，发送json格式

```
POST /api/msg/your-api-token HTTP/1.1
Host: seedsnote.com
Content-type: application/json
{
    "content": "Hello"
}
```

请求响应: 接口返回数据为json格式

|字段|返回值|备注|
|-----|-----|------|
|code|0或-1|用于判断请求是否成功，成功为0，失败为-1|
|message|保留字段|请勿用于判断成功或失败|
|data|保留字段|当前为空|


2. 如果是图片，请选择form-data格式，并将字段名

```
POST /api/msg/your-api-token HTTP/1.1
Host: seedsnote.com
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

----WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="file"; filename="sample.jpg"
Content-Type: image/jpeg

(data)
----WebKitFormBoundary7MA4YWxkTrZu0gW
```

请求响应: 接口返回数据为json格式

|字段|返回值|备注|
|-----|-----|------|
|code|0或-1|用于判断请求是否成功，成功为0，失败为-1|
|message|保留字段|请勿用于判断成功或失败|
|data|保留字段|当前为空|

## About Seeds

🌱 Seeds思记，一款优雅智能的笔记应用。我们为每一位用户提供专属的API地址，以便于你从不同的地方更好地采集想法到Seeds。

轻快的随时记，智能的知识网 ｜Write，Think，and Grow

![Frame 46](https://user-images.githubusercontent.com/67967374/123350924-96fa7200-d58e-11eb-9410-d8015228e57e.png) 
