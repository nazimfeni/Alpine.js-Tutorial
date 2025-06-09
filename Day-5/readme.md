## Working with Alpine.js Lifecycle and Utilities
✅ 1. Understanding Lifecycle with x-init
x-init lets you run code when the component is initialized.
```
<div x-data="{ message: '' }" x-init="message = 'Component Loaded!'">
  <p x-text="message"></p>
</div>
```
✅ 2. Accessing DOM Elements with $refs and x-ref
- x-ref marks an element.
- $refs gives access to it.
```
<div x-data="{ focusInput() { $refs.name.focus() } }">
  <input x-ref="name" type="text" placeholder="Click button to focus">
  <button @click="focusInput()">Focus Input</button>
</div>
```
✅ 3. Using $el and $nextTick
- $el: refers to the current element.
- $nextTick: waits until the DOM has updated.

```
<div x-data="{ count: 0, updated: '' }">
  <button @click="count++; $nextTick(() => updated = 'DOM Updated')">Add</button>
  <p x-text="count"></p>
  <p x-text="updated"></p>
</div>
```
✅ 4. Watching Data with $watch
```
<div x-data="{ count: 0 }" x-init="$watch('count', value => console.log('Count is', value))">
  <button @click="count++">Increment</button>
</div>
```
✅ 5. Dispatching Custom Events with $dispatch
```
<div x-data @custom-event.window="alert('Received!')">
  <button @click="$dispatch('custom-event')">Send Event</button>
</div>
```
✅ 6. Creating Global Stores with Alpine.store()
```
<script>
  document.addEventListener('alpine:init', () => {
    Alpine.store('app', { theme: 'light' });
  });
</script>

<div x-data>
  <button @click="$store.app.theme = 'dark'">Dark Mode</button>
  <p x-text="$store.app.theme"></p>
</div>
```