
# 📝 Alpine.js To-Do List with LocalStorage

This is a simple, lightweight To-Do List web app built using [Alpine.js](https://alpinejs.dev/) and browser `localStorage`. It allows you to:

- Add new tasks
- Mark tasks as done
- Delete tasks
- Automatically save and load tasks from localStorage

## 🚀 Features

- ⚡ Instant interactivity with Alpine.js
- 💾 Task persistence using browser localStorage
- ✨ Minimal UI with clean HTML/CSS
- 🧠 No backend or build tools required

## 📂 How It Works

- **Alpine.js Component**: The app is built using a single Alpine.js component initialized via `x-data="todoApp()"`.
- **State Management**:
  - `newTask`: Holds the input text.
  - `tasks`: Array of task objects with `{ text: '', done: false }`.
- **Form Handling**: `@submit.prevent="addTask"` adds a new task when the user submits the form.
- **Task Rendering**: Uses `x-for` to render tasks dynamically.
- **Task Completion**: Each task has a checkbox bound with `x-model="task.done"`.
- **Delete Functionality**: Tasks can be deleted by clicking the ❌ button.
- **Persistence**: All tasks are saved in `localStorage` using `JSON.stringify()` and loaded on page initialization using `JSON.parse()`.

## 💻 Code Overview

```js
function todoApp() {
  return {
    newTask: '',
    tasks: [],

    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({ text: this.newTask.trim(), done: false });
        this.newTask = '';
        this.saveTasks();
      }
    },

    removeTask(index) {
      this.tasks.splice(index, 1);
      this.saveTasks();
    },

    saveTasks() {
      localStorage.setItem('tasks', JSON.stringify(this.tasks));
    },

    loadTasks() {
      const stored = localStorage.getItem('tasks');
      if (stored) {
        this.tasks = JSON.parse(stored);
      }
    }
  };
}
```
Best of Luck