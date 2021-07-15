# ENG-001:Adopted front end technology.md

Date: 7/14（ここのDateはDRを導入しようというのが決まり文書を書いた日。採用技術を考え始めたのは実際は2021年5月頃。）

## Status

proposed

## Context

クライアントがいるわけでもなく給料が発生するわけでもないので、モチベーションの維持のため検討時点(2021年5月頃)でモダンな技術を採用したい。また、プログラミングやチーム開発が初めてのメンバーも多く、挫折は防ぎたい。
この条件の中で私（以下：採用者）が独断と偏見と好みで技術を採用した。

## Decision

- [React](https://ja.reactjs.org/) - Facebook 製 UI ライブラリ。
  - TypeScriptと相性が良いらしいので。また採用者がちょうどReactを使用してサイトを作っていたこともあり、採用者がメンバーの質問に答えられるということで採用した。
- [Next.js](https://nextjs.org/) - React のフレームワーク。
  - 初心者が多い中でWebpackなどの設定を極力省きたかった。
- [TypeScript](https://www.typescriptlang.org/) - JavaScriptを拡張して開発されたプログラミング言語。
  - 型は必要。
- [Tailwind CSS](https://tailwindcss.com/) - ユーティリティファーストな CSS フレームワーク。 
  - 別プロジェクトで使用してフロントエンドの開発メンバーからも使いやすいという意見が出たため。CSSと対応するクラス名を調べる過程でCSSのセレクタの種類も覚えられるのではないかということで採用。
- [ESLint](https://eslint.org/) - コードを分析し問題点を指摘してくれるツール。
  - Reactの書き方(functionかアロー関数かなど）をチームで統一したいため。
- [Prettier](https://prettier.io/) - コードフォーマッター。
  - 調べた中でESLintとセットで導入しているケースが多かったため。このプロジェクトで今後の使用を検討する。
- [Jest](https://jestjs.io/ja/) - JavaScript のテスティングフレームワーク。
  - 初心者が多いからこそ勉強も兼ねてテストは導入したい。
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/) - React Components　をテストするためのもの。
- [Mock Service Worker](https://mswjs.io/) - サービスワーカーを利用して API モックを作れるライブラリ。
  - バックエンドの構成の決定が遅れたこと、デザインカンプが先にある程度できたことからフロントエンドから作り始めることにした。そのためバックエンドのAPIが作成されていない状態でAPIのモックを作成するために採用する。
- [GitMoji](https://gitmoji.dev/) - Commit メッセージに絵文字を追加。
  - 見やすそうだったので導入。使いやすければバックエンドでも導入する可能性あり。

## Other Options
- [Chakra　UI](https://chakra-ui.com/) - React用の UI コンポーネントフレームワーク
  - TailwindCSSを前のプロジェクトで使用していたので、新しくChakra　UIを学習するコストを掛けるよりTailwindCSSを使用する方が良いと判断した。
- CSS Modules - Reactのスタイリング方法の一つ
  - cssファイルが多くなってしまうのを避けたいので採用しなかった。
- CSS in JS - Reactのスタイリング方法の一つ
  - styled-componentsなどはコンポーネントと区別がつきにくいという欠点があり、学習コストも高そうな印象を受けたので。

## Consequences

