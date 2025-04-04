# react-ko-starter

これは [react-ko](https://github.com/menimani/react-ko) の**公式スターターテンプレート**です。  
**React** と **Knockout.js** をシンプルに組み合わせたミニマルな環境を提供します。

---

## 🚀 クイックスタート

```bash
npx degit menimani/react-ko-starter my-app
cd my-app
npm install
npm run dev
```

[`App.tsx`](./src/App.tsx) を開いて編集すれば、すぐに Knockout のバインディングが React の中で動作します。

---

## 📦 含まれているもの

- ✅ React + TypeScript + Vite（公式テンプレート）
- ✅ [Knockout.js](https://knockoutjs.com/) インストール済み
- ✅ [react-ko](https://github.com/menimani/react-ko) インストール済み
- ✅ 余計な構成・コードなし、インストールしてすぐ開発可能

---

## 💡 `react-ko` とは？

> `react-ko` は React の JSX 内で Knockout の `data-bind` を使えるようにする軽量ライブラリです。  
> 既存の Knockout ViewModel をそのまま React コンポーネント内で利用できます。

- `ko.observable`, `computed`, `observableArray` などをそのまま使える
- `data-bind` 属性でDOMにバインディングを適用
- `<KoScope viewModel={vm}>...</KoScope>` で部分的にバインド可能
- `<RootKnockoutProvider viewModel={vm}>` を使えばアプリ全体でバインド可能

---

## 🧪 サンプルコード

```tsx
import { KoScope } from 'react-ko'
import ko from 'knockout'

class ViewModel {
  count = ko.observable(0)
  increment = () => this.count(this.count() + 1)
}

const vm = new ViewModel()

export default function App() {
  return (
    <KoScope viewModel={vm}>
      <button data-bind="click: increment">
        count is <span data-bind="text: count"></span>
      </button>
    </KoScope>
  )
}
```

---

## 🔍 次のステップ

- `observable` を追加してみる
- `computed` や `observableArray` を試す
- ViewModel を別ファイルに分離してみる
- [`react-ko` のドキュメント](https://github.com/menimani/react-ko) を読む（KoIf / KoForeach / KoScope）

---

## 🧠 なぜこれを使うのか？

- Knockout はシンプルでリアクティブ、実績あり
- React は構造化されたコンポーネントに最適
- KO のリアクティブ性 + React の構造性 → 最小構成で最高の体験
- `useState` や `useEffect` に疲れた人にも刺さる

---

## 🛠️ ライセンス

MIT
