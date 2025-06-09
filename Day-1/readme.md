# Alpine JS Tutorial

### What is Alpine.js?

Alpine.js is a lightweight JavaScript framework for adding interactivity to your HTML using declarative attributes.

### Key Features of Alpine.js

#### Feature / Description

- Small & Fast Only ~10KB, perfect for fast-loading websites
- No Build Required
- Reactive Automatically updates the DOM when data changes
- Works with HTML You write everything directly in your HTML (no separate JS files needed)
- Great for UI Parts Perfect for modals, dropdowns, tabs, toggles, counters, and more

### Why use Alpine.js?

- Lightweight and Minimal
- Easy to Learn and Use
- Declarative and Reactive
- Good for Small to Medium Interactivity
- Works Well with Existing Backend Frameworks
  - Since Alpine.js is just JavaScript that runs in the browser, it works easily alongside server-rendered apps (Laravel, Rails, Django, etc.).
- No build step needed.

Here’s a complete list of Alpine.js core directives (as of Alpine v3), along with a short explanation for each. These directives are used to control reactivity, events, conditionals, loops, and more — all directly inside your HTML.

### Data & Initialization

| Directive | Purpose                                             |
| --------- | --------------------------------------------------- |
| `x-data`  | Declares a local component with reactive data.      |
| `x-init`  | Runs JavaScript when the component is initialized.  |
| `x-id`    | Generates unique IDs for use in ARIA/accessibility. |

### Binding Attributes and Text

| Directive       | Purpose                                                         |
| --------------- | --------------------------------------------------------------- |
| `x-text`        | Updates the element's `textContent`.                            |
| `x-html`        | Updates the element's `innerHTML`. _(Be careful of XSS)_        |
| `x-bind` or `:` | Dynamically bind attributes (e.g. `x-bind:class`, `:disabled`). |

### Events

| Directive                    | Purpose                                                |
| ---------------------------- | ------------------------------------------------------ |
| `@event`                     | Listen to a DOM event (e.g., `@click`, `@input`).      |
| `@click.away`                | Runs when you click outside the element.               |
| `@keydown.escape`            | Runs when the Escape key is pressed.                   |
| `@mouseenter`, `@mouseleave` | Handle specific browser events like mouse enter/leave. |

### You can use event modifiers:
.prevent → prevent default
.stop → stop propagation
.once → run only once
.debounce.300ms → delay event by 300ms

### Conditional Rendering

| Directive | Purpose                                                                                  |
| --------- | ---------------------------------------------------------------------------------------- |
| `x-show`  | Shows or hides an element using `display: none` based on a condition.                    |
| `x-if`    | Completely adds/removes the element from the DOM based on a condition. _(Alpine v3.10+)_ |

### Looping

| Directive | Purpose                        |
| --------- | ------------------------------ |
| `x-for`   | Loops over an array or object. |

### Two-Way Binding

| Directive | Purpose                                                     |
| --------- | ----------------------------------------------------------- |
| `x-model` | Two-way bind form inputs, checkboxes, radios, selects, etc. |

### Modifiers:

| Modifier  | Purpose                                    |
| --------- | ------------------------------------------ |
| `.lazy`   | Updates after `change` instead of `input`. |
| `.number` | Converts the input value to a number.      |
| `.trim`   | Trims whitespace from the input value.     |

### Refs & Lifecycle

| Directive / Property | Purpose                                                     |
| -------------------- | ----------------------------------------------------------- |
| `x-ref`              | Gets a reference to a DOM element from within Alpine logic. |
| `$refs`              | Used in expressions to access a referenced element.         |
| `$el`                | Refers to the current DOM element.                          |
| `$nextTick`          | Runs code after DOM updates.                                |
| `$watch`             | Watches a property and reacts when it changes.              |
| `$store`             | Access global Alpine store data.                            |
| `$dispatch`          | Dispatch a custom event to parent components.               |
| `$data`              | Access the entire component’s reactive data object.         |

### Transitions & Animations

| Directive      | Purpose                                                     |
| -------------- | ----------------------------------------------------------- |
| `x-transition` | Adds enter/leave transitions to elements when shown/hidden. |

**Modifiers examples:**

- `x-transition.duration.500ms` — sets transition duration to 500ms
- `x-transition.opacity` — applies opacity transition
- `x-transition.scale.90` — applies scale transform transition at 90%

### Component Scoping & Global State

| Feature          | Purpose                                        |
| ---------------- | ---------------------------------------------- |
| `x-teleport`     | Moves the element to another place in the DOM. |
| `Alpine.store()` | Defines global reactive state.                 |

### Additional built-in Alpine.js utilities

| Method                              | Description                                             |
| ----------------------------------- | ------------------------------------------------------- |
| `$refs.foo.focus()`                 | Call native DOM methods on referenced elements.         |
| `$el.querySelector()`               | Use normal DOM querying on the current element.         |
| `$watch('count', value => { ... })` | Watch and react to changes in a property named `count`. |
