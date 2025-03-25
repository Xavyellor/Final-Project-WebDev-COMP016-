# Grocery To-Do List

A simple Vue 3-powered grocery to-do list that allows users to add, edit, mark, and delete grocery items.

## Features
- ✅ **Add Items**: Type a grocery item and click "Add" to add it to the list.
- ✏️ **Edit Items**: Click "Edit" to modify an existing item.
- ✔️ **Mark as Done**: Click an item to toggle between completed and pending.
- ❌ **Remove Items**: Click "X" to remove an item from the list.
- 📊 **Item Counter**: Displays the total items and the number of completed items.

## Tech Stack
- ⚡ Vue 3 with `<script setup>`
- 🎨 Tailwind CSS for styling
- 🎯 Computed properties for dynamic counting

## Usage
- Type a grocery item in the input field and click **"Add"**.
- Click on an item to **toggle completion** (strike-through effect).
- Click **"Edit"** to modify an item and press **Enter** or click **"Save"** to confirm.
- Click **"X"** to remove an item.
- The total items and completed items are displayed at the bottom.

## Code Breakdown
### Template
- **Input field & button** to add new items.
- **List rendering** with `v-for` to display items dynamically.
- **Inline editing** via `v-if` and `v-else`.
- **Event handlers** to manage user interactions.

### Script
- **Reactive data** using `ref([])`.
- **Methods** to add, edit, remove, and toggle items.
- **Computed properties** for completed item count.



## License
This project is licensed under the **MIT License**.
---
Made with ❤️ using Vue 3 & Tailwind CSS.

