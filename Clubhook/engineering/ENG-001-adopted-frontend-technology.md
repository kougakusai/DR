# ENG-001:Adopted front end technology.md

Date: 7/14

## Status

proposed

## Context

クライアントがいるわけでもなく給料が発生するわけでもないので、モチベーションの維持のため検討時点でモダンな技術を採用したい。
その中でリーダーが独断と偏見と好みで技術を採用した。

## Decision

- [React](https://ja.reactjs.org/) - Facebook 製 UI ライブラリ。
- [Next.js](https://nextjs.org/) - React のフレームワーク。
- [TypeScript](https://www.typescriptlang.org/) - 型があることでバグを防いだり、ドキュメント代わりになったり、チーム開発が楽になります。
- [Tailwind CSS](https://tailwindcss.com/) - ユーティリティファーストな CSS フレームワーク。
- [ESLint](https://eslint.org/) - コードを分析し問題点を指摘してくれるツール。
- [Prettier](https://prettier.io/) - コードフォーマッター。
- [Jest](https://jestjs.io/ja/) - Facebook 製の JavaScript のテスティングフレームワーク。
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/) - React Components　をテストするためのもの。
- [Mock Service Worker](https://mswjs.io/) - サービスワーカーを利用して API モックを作れるライブラリ。
- [GitMoji](https://gitmoji.dev/) - Commit メッセージに絵文字を使うもの。

## Other Options (任意)
- [Chakra　UI](https://chakra-ui.com/) - React用の UI コンポーネントフレームワーク
  - TailwindCSSを前のプロジェクトで使用していたので、新しくChakra　UIを学習するコストを掛けるよりTailwindCSSを使用する方が良いと判断した。

## Consequences

