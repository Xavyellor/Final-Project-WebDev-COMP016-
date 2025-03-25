<template>
  <div class="px-5 mx-auto max-w-lg bg-white rounded-xl shadow-sm space-y-4 flex items-center justify-center min-h-screen">
    <div class="w-full">
      <h1 class="text-3xl font-bold text-center">Grocery To-Do List</h1>
      
      <!-- Input & Add Item -->
      <div class="flex space-x-5 mt-4">
        <input v-model="newItem" placeholder="Enter grocery item" class="border p-2 w-full rounded-xl" />
        <button @click="addItem" class="bg-green-500 text-white px-4 py-2 rounded">Add</button>
      </div>
      
      <!-- Grocery List -->
      <ul class="space-y-5 mt-4">
        <li v-for="(item, index) in items" :key="index" class="flex justify-between items-center bg-gray-100 p-2 rounded">
          <input v-if="item.editing" v-model="item.text" @keyup.enter="saveEdit(index)" class="border p-1 rounded w-full" />
          <span v-else :class="{'line-through': item.done}" @click="toggleItem(index)">{{ item.text }}</span>
          <div class="flex space-x-2">
            <button v-if="!item.editing" @click="editItem(index)" class=" text-blue-500">Edit</button>
            <button v-else @click="saveEdit(index)" class="p-2 text-green-500">Save</button>
            <button @click="removeItem(index)" class="text-red-500">X</button>
          </div>
        </li>
      </ul>

      <!-- Item Counter -->
      <p class="text-gray-600 mt-4">Total Items: {{ items.length }}</p>
      <p class="text-gray-600 mt-4">Items completed: {{ FinishedItems}}/{{items.length}}</p>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const newItem = ref('');
const items = ref([]);

const addItem = () => {
  if (newItem.value.trim()) {
    items.value.push({ text: newItem.value, done: false, editing: false });
    newItem.value = '';
  }
};

const removeItem = (index) => {
  items.value.splice(index, 1);
};

const toggleItem = (index) => {
  items.value[index].done = !items.value[index].done;
};

const editItem = (index) => {
  items.value[index].editing = true;
};

const saveEdit = (index) => {
  if (items.value[index].text.trim()) {
    items.value[index].editing = false;
  } else {
    removeItem(index);
  }
};

const FinishedItems = computed(() => items.value.filter((item) => item.done).length);
</script>

<style>
.line-through {
  text-decoration: line-through;
}
</style>
