## Alpine.js Event Directives
| Directive (Shorthand) | Description                             | Examples                             |
|----------------------|---------------------------------------|------------------------------------|
| `@click`             | Fires on mouse click                   | `<button @click="doSomething()">`  |
| `@dblclick`          | Fires on double click                  |                                    |
| `@mouseenter`        | Fires when mouse enters element        |                                    |
| `@mouseleave`        | Fires when mouse leaves element        |                                    |
| `@mouseover`         | Fires when mouse moves over element    |                                    |
| `@mouseout`          | Fires when mouse moves out              |                                    |
| `@mousedown`         | Fires when mouse button is pressed     |                                    |
| `@mouseup`           | Fires when mouse button is released    |                                    |
| `@keydown`           | Fires when any key is pressed           |                                    |
| `@keydown.enter`     | Fires on Enter key                      |                                    |
| `@keydown.escape`    | Fires on Escape key                     |                                    |
| `@keyup`             | Fires when key is released              |                                    |
| `@keyup.enter`       | Fires on Enter key release              |                                    |
| `@input`             | Fires on input value change             | `<input @input="handleInput()">`   |
| `@change`            | Fires when input loses focus and value changed |                             |
| `@submit`            | Fires on form submission                | `<form @submit.prevent="submit()">`|
| `@focus`             | Fires when element receives focus       |                                    |
| `@blur`              | Fires when element loses focus          |                                    |
| `@resize.window`     | Fires when window is resized            |                                    |
| `@scroll.window`     | Fires when window scrolls                |                                    |
| `@click.away`        | Fires when click happens outside element | Useful for closing modals/dropdowns |
| `@dragstart`         | Fires when drag starts                   |                                    |
| `@drop`              | Fires when element receives dropped item|                                    |
| `@dragover`          | Fires when dragged item is over element |                                    |

### Event Modifiers
| Modifier          | Purpose                                         | Example                      |
|-------------------|------------------------------------------------|------------------------------|
| `.prevent`        | Calls `event.preventDefault()`                   | `@submit.prevent="save()"`    |
| `.stop`           | Calls `event.stopPropagation()`                  | `@click.stop="handleClick()"` |
| `.once`           | Event handler runs only once                      | `@click.once="alert('clicked!')"` |
| `.passive`        | Marks event listener as passive for better performance | `@scroll.passive="onScroll"`  |
| `.debounce.500ms` | Debounce event, waits 500ms after last event     | `@input.debounce.500ms="search"` |
| `.self`           | Fires only if event target is the element itself | `@click.self="close()"`        |
| `.away`           | Fires when click happens outside element          | `@click.away="close()"`        |

### x-model
x-model is used in Alpine.js to bind a form input element’s value to a data property, enabling two-way data binding — meaning the input updates the data, and the data updates the input.