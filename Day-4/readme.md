## Two-Way Data Binding in Alpine.js
Two-way data binding means that:
- When the input changes, the data updates.
- When the data changes, the input updates.
- In Alpine.js, this is done using the x-model directive.

### Two-Way Data Binding with `x-model`

| Element Type              | Example                                           |
| ------------------------- | ------------------------------------------------- |
| `<input type="text">`     | `<input x-model="name">`                          |
| `<textarea>`              | `<textarea x-model="message"></textarea>`         |
| `<input type="checkbox">` | `<input type="checkbox" x-model="accepted">`      |
| `<input type="radio">`    | `<input type="radio" x-model="choice" value="A">` |
| `<select>`                | `<select x-model="country">`                      |

### `x-model` Modifiers

| Modifier  | Purpose                                                  | Example                        |
| --------- | -------------------------------------------------------- | ------------------------------ |
| `.lazy`   | Updates data only on `change`/`blur`, not on every input | `<input x-model.lazy="name">`  |
| `.number` | Converts the input string to a number                    | `<input x-model.number="age">` |
| `.trim`   | Trims leading and trailing whitespace                    | `<input x-model.trim="name">`  |
