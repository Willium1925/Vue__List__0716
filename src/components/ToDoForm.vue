<script>
    // 一個輸入表單用來新增待辦事項
    // label 提示要輸入什麼
    // input 是文字輸入框 會有 id name 屬性
    // 按鈕用來新增待辦事項
    // 輸入的內容要跟 data 的 label 做雙向綁定
    // 當按下新增按鈕時，會觸發 onSubmit 方法
    // data 會有 label 屬性 用來儲存輸入的待辦事項
import { ref } from 'vue';
const newToDo = ref('');
const addToDo = () => {
  if (newToDo.value.trim() !== '') {
    // 這裡可以添加邏輯來處理新增待辦事項
    console.log('新增待辦事項:', newToDo.value);
    newToDo.value = ''; // 清空輸入框
  } else {
    console.warn('待辦事項不能為空');
  }
};


</script>

<template>
  一個輸入表單用來新增待辦事項
  label 提示要輸入什麼input 是文字輸入框 會有 id name 屬性按鈕用來新增待辦事項
  <form @submit.prevent="addToDo">
    <label for="todo-input">新增待辦事項:</label>
    <input type="text" id="todo-input" v-model="newToDo" name="todo-input" required />
    <button type="submit">新增</button>
  </form>



</template>

<style scoped>

</style>