
<template>
  <div id="app">
    <h1>待辦清單</h1>
    <ul>
      <li>
        <to-do-item label="安安你好，預設勾選" :done="true"></to-do-item>
      </li>
      <li>
        <to-do-item label="安安你好，預設不勾" :done="false"></to-do-item>
      </li>
    </ul>
  </div>

</template>
<script>
import ToDoItem from "./components/ToDoItem.vue";

export default {
  name: "app",
  components: {
    ToDoItem,
  },
};
</script>

