# 概要
REST APIハンズオンの実施結果を記載しています。どうせならリクエストのコードも記載すべきかもしれませんが、ハンズオンに記載している情報のため省略しています。
# GETリクエスト
![GetResponse1](https://github.com/tattsun-R/rest-api-handson/assets/138351540/f589878e-dc2d-4ef9-9d90-6d1eddf4c817)
![GetResponse2](https://github.com/tattsun-R/rest-api-handson/assets/138351540/07ad0989-d5fa-4fd5-a944-cb8f9cadc5ca)
# POSTリクエスト
Postmanでなぜかレスポンスステータスが201にならなかった。成功してるからいいものなのか。
```
$ curl -i -H "Authorization: token 個人アクセストークン" \
    -d '{
        "name": "blog02",
        "auto_init": true,
        "private": true,
        "gitignore_template": "Nanoc"
      }' \
    https://api.github.com/user/repos

・・・
HTTP/2 201
server: GitHub.com
date: Sat, 29 Jul 2023 13:21:31 GMT
content-type: application/json; charset=utf-8
・・・

{
　・・・
  "name": "blog02",
  ・・・
  "private": true,
 ・・・
    "html_url": "https://github.com/tattsun-R",
・・・
  "created_at": "2023-07-29T13:21:31Z",
  "updated_at": "2023-07-29T13:21:31Z",
・・・
  "visibility": "private",
・・・
```
![PostRespose](https://github.com/tattsun-R/rest-api-handson/assets/138351540/ff17bc13-c977-4f5d-bf21-c2d6755130a9)
# PATCHリクエスト
![PatchResponse](https://github.com/tattsun-R/rest-api-handson/assets/138351540/076f21a0-55fc-4715-a9a7-a9beba556249)

-----
参考：https://github.com/raisetech-for-student/rest-api-handson

