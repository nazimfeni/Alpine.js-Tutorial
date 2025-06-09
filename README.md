# 🚀 Alpine.js Starter
A lightweight and modern JavaScript framework for adding interactivity directly in your HTML.

## 📦 What is Alpine.js?
Alpine.js offers you the reactive and declarative nature of big frameworks like Vue or React, but in a much smaller (≈10kB gzipped) package, with no build step required.

- It’s perfect for:
- Laravel Blade components
- Static websites
- Projects that don’t need a full SPA
- Enhancing HTML with small bits of interactivity

## 🛠 Features
### 🧠 Declarative syntax (x-data, x-model, x-show, etc.)

⚡ Reactive data binding
🪶 Lightweight (10kB gzipped)
🧩 No build tools required
🛡️ Works perfectly with Tailwind CSS

### 🚀 Getting Started
✅ Include Alpine.js
```
<script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>
```
Add this just before your closing </body> tag or in the <head> with defer.

### ⚙️ Core Directives
| **Directive**  | **Purpose**                            | **Example**                  |
| -------------- | -------------------------------------- | ---------------------------- |
| `x-data`       | Component state                        | `x-data="{ open: true }"`    |
| `x-model`      | Two-way binding                        | `x-model="inputValue"`       |
| `x-show`       | Show/hide with CSS                     | `x-show="isVisible"`         |
| `x-bind` / `:` | Bind attribute to data                 | `:src="imageUrl"`            |
| `x-on` / `@`   | Handle events                          | `@click="doSomething()"`     |
| `x-transition` | Animations on show/hide                | `x-show="open" x-transition` |
| `x-if`         | Conditional rendering (DOM add/remove) | `x-if="condition"`           |





