# try-expo
React Native勉強会用のレポジトリです！

# 構築手順
1.expoインストール
npmの場合
```
npm install -g expo-cli
```
yarnの場合
```
yarn global add expo-cli
```

2.プロジェクトの作成(※project-nameの部分は任意の名前になります。)
```
expo init project-name
```

3.選択画面でtabsを選択(テンプレートが作成されます。)
```
? Choose a template: › - Use arrow-keys. Return to submit.
    ----- Managed workflow -----
    blank                 a minimal app as clean as an empty canvas
    blank (TypeScript)    same as blank but with TypeScript configuration
 ❯  tabs (TypeScript)     several example screens and tabs using react-navigation and TypeScript
    ----- Bare workflow -----
    minimal               bare and minimal, just the essentials to get you started
    minimal (TypeScript)  same as minimal but with TypeScript configuration
```
Managed workflowとBare workflowの違いは簡単にいうと、

・Managed workflow→Expo のサポート下で開発できる

・Bare workflow→Expo なしでの開発に近く、カスタマイズ性は上がるが難易度が高い

という違いみたいです！

4.下記コマンドで実行する
```
expo start
or
npm start
or
yarn start
```

5.native-baseをインストールする
```
npm install native-base
```

6.アプリケーション全体でnative-baseを使うためにNativeBaseProviderをApp.tsxに追記する
```
import React from "react";
// 1. import `NativeBaseProvider` component
import { NativeBaseProvider, Text, Box } from "native-base";

export default function App() {
  // 2. Use at the root of your app
  return (
    <NativeBaseProvider>
      <Box flex={1} bg="#fff" alignItems="center" justifyContent="center">
        <Text>Open up App.js to start working on your app!</Text>
      </Box>
    </NativeBaseProvider>
  );
}
```
https://docs.nativebase.io/setup-provider
以上でセットアップの完了です！お疲れ様でした！

native-baseのコンポーネントがまとめられている「kitchen sink」も是非webから触って見てください！
https://docs.nativebase.io/kitchen-sink 
