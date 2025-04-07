# react-ko-starter

en English | [ja 日本語](./README.ja.md)

This is the **official starter template** for [react-ko](https://github.com/menimani/react-ko),  
a minimalist bridge between **React** and **Knockout.js**.

## 🚀 Quick Start

```bash
npx degit menimani/react-ko-starter-ts my-app-ts
cd my-app-ts
npm install
npm run dev
```

Then open [`App.tsx`](./src/App.tsx) and edit freely.  
Knockout bindings will work instantly inside your React components!

For the JavaScript version, check out:  
[react-ko-starter-js](https://github.com/menimani/react-ko-starter-js)

---

## 📦 What's included

- ✅ React + TypeScript + Vite (official template)
- ✅ [Knockout.js](https://knockoutjs.com/) installed
- ✅ [react-ko](https://github.com/menimani/react-ko) installed
- ✅ No extra setup or configuration — just `npm install` and go

---

## 💡 What is `react-ko`?

> `react-ko` allows you to write Knockout bindings (`data-bind`) inside your React JSX,  
> using your existing KO ViewModels directly.

- Use `ko.observable`, `computed`, `observableArray`, etc. as usual
- Apply KO bindings in React DOM with `data-bind`
- Use `<KoScope viewModel={vm}>...</KoScope>` to bind a viewModel to any component subtree
- Or use `<RootKnockoutProvider viewModel={vm}>` for global bindings

---

## 🧪 Sample Code

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

## 🔍 Next Steps

- Add more `observable` fields
- Try `computed` or `observableArray`
- Move the ViewModel to a separate file
- Explore `react-ko` docs for [KoIf / KoForeach / KoScope](https://github.com/menimani/react-ko)

---

## 🧠 Why use this?

Because:
- Knockout is simple, reactive, and proven
- React is great for component composition
- You get **KO's reactivity** with **React's structure**, no boilerplate
- Sometimes `useState` and `useEffect` are just not worth it

---

## 🛠️ License

MIT

