# React Location


### React Locationとは
- React Routerと同様の、Reactアプリケーション用のルーターのライブラリ
- 2021年の11月12日にリリース
- 作者は、React Query等も作成してる、Tanner Linsley氏

---

### 特徴
React Routerと比べると、CSRに特化してるのが特徴
- 画面遷移時での非同期のハンドリングが豊富

---

### 主な機能

#### Route Loaders
- Route Loadersとは、path変更などが行われた場合に実行される関数

画面遷移時に、データfetchや非同期処理を行う場合に、
データfetchや非同期処理が完了するまで、画面遷移を待機させるようハンドリングを行ってくれる。

画面遷移を待機させる意図としては、
画面遷移時にfetchしてるデータが利用可能になる前に、遷移が完了してしまうのは良しとしないという考えのもと、
データfetchや非同期処理が完了するまで、画面遷移を待機させる機能を用意してる

また、遷移後の画面でデータfetchや非同期処理が完了するまでのスピナー表示など必要になり、
スピナーを表示するために、表示/非表示の切り替えなどのロジック実装をするのは、
ユーザーエクスペリエンスとして最適ではないという考え

https://react-location.tanstack.com/guides/route-loaders

---

#### Route Elements
- 画面遷移周りをハンドリングしてくれる機能

  - pathが一致したがエラーが発生したときに、エラー用のコンポーネントを定義しておけば表示してくれる
  - pathが一致してpending状態に入ったときに、pending用のコンポーネントを定義しておけば表示してくれる


https://react-location.tanstack.com/guides/route-elements
https://react-location.tanstack.com/guides/pending-states

---

#### React Location Simple Cache
- Route Loaders内で利用できるcache機能
  - 画面遷移時にRoute Loadersでfetchしたデータのcacheが使えるようになります。

別途ライブラリをインストールすることで、cacheが使える。
公式のdevToolも用意されてるので、開発もしやすそう

https://react-location.tanstack.com/tools/simple-cache
https://react-location.tanstack.com/tools/devtools
