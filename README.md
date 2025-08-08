# Happy-toast-kit

A simple and customizable toast notification system for React projects. 🎉

[![npm version](https://img.shields.io/npm/v/happy-toast-kit.svg)](https://www.npmjs.com/package/happy-toast-kit)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

---

## ✨ Features

- 🔔 Easy-to-use toast notifications
- 🎨 Customizable styles
- 🧠 Clean and minimal API
- ⏳ Auto-dismiss support
- 💡 Lightweight (zero dependency)
- 🌟 From version **1.1.1**, full support for **Tailwind CSS** out of the box

---

## 🚀 Installation

```bash
npm install happy-toast-kit
# or
yarn add happy-toast-kit
```

---

## 🧠 Usage

### 1. Wrap your app with `ToastProvider`

```tsx
import { ToastProvider } from "happy-toast-kit";

function App() {
  return (
    <ToastProvider>
      <YourApp />
    </ToastProvider>
  );
}
```

### 2. Use the `useToast` hook

```tsx
import { useToast } from "happy-toast-kit";

export default function MyComponent() {
  const showToast = useToast();

  return (
    <button onClick={() => showToast("Hello world!", "success")}>
      Show Toast
    </button>
  );
}
```

---

## 🔧 Props

| Prop        | Type       | Default | Description                     |
|-------------|------------|---------|---------------------------------|
| `children`  | `ReactNode`| —       | Your app content inside provider|

---

## 🖌️ Styling

This package uses a simple `.toast-container` and `.toast` class. You can override the styles using your own CSS.

Example CSS:

```css
.toast-container {
  position: fixed;
  top: 1rem;
  right: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  z-index: 9999;
}

.toast {
  padding: 1rem 1.5rem;
  border-radius: 0.375rem;
  color: white;
  font-weight: bold;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.toast.info {
  background-color: #3b82f6;
}

.toast.success {
  background-color: #10b981;
}

.toast.error {
  background-color: #ef4444;
}
```

Or, if you’re using Tailwind CSS (version 1.1.1 and up):

```tsx
<div className="fixed top-4 right-4 space-y-2 z-[9999]">
  <div className="bg-green-500 text-white font-bold px-6 py-4 rounded shadow">
    Your toast message
  </div>
</div>
```

---

## 🧪 Local Development

Want to contribute? Clone the repo and run the example:

```bash
git clone https://github.com/aliafshani/happy-toast-kit
cd happy-toast-kit
npm install
npm run dev
```

---

## 🤝 Contributing

Feel free to open issues or PRs. If you're interested in working on this together or expanding it with new features like (dismiss buttons, queueing, or animation support), let's connect!

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## ❤️ Author

Made with love by [Ali Afshani ( Aliwsh )](https://aliafshani.github.io/AandN-group/) – if you liked it, don’t forget to star the repo ✨