# これは何？
Go公式ドキュメントの[Writing Web Applications](https://golang.org/doc/articles/wiki/)に従って作ったWikiアプリ

## Build & Run
```bash
go build wiki.go && ./wiki
```

## ページ一覧
| URL                             | Method | 内容                          |
| ------------------------------- | ------ | ----------------------------- |
| localhost:8080/view/{{ title }} | GET    | {{ title }}の閲覧ページを開く |
| localhost:8080/edit/{{ title }} | GET    | {{ title }}の編集ページを開く |
| localhost:8080/save/{{ title }} | POST   | {{ title }}の内容を保存する   |

## やりたいことリスト
- [x] templateを`/tmpl`, 記事を`/data`に保存する
- [x] `/`を`view/FrontPage`にリダイレクトする
- [x] HTML, CSSを良い感じにする
- [ ] `POST`以外で`/save`にリクエストを投げたら失敗するようにする
- [ ] `[PageName]`と`[]`でくくられているところはそのページへのリンクにする
- [ ] CSSが当たらない問題を解決する
