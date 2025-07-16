
<template>
  <div id="app">

    <h1>直接使用 ToDoItem 組件</h1>
    <ul>
      <li>
        <to-do-item label="安安你好，預設勾選" :done="true"></to-do-item>
      </li>
      <li>
        <to-do-item label="安安你好，預設不勾" :done="false"></to-do-item>
      </li>
    </ul>

    <!-- 換行 -->
    <br><br><br>

    <h1>使用渲染</h1>
    <ul>
      <li v-for="item in ToDoItems00" :key="item.id">
        <to-do-item
            :label="item.label"
            :done="item.done"
            :id="item.id"></to-do-item>
      </li>
    </ul>

    <h1>使用 ToDoForm 組件</h1>






  </div>

</template>
<script>
import ToDoItem from "./components/ToDoItem.vue";
import ToDoForm from "@/components/ToDoForm.vue"; // 這裡來的資料是最內層的，要讓他出現在此

export default {
  name: "app",
  components: {
    ToDoItem,
    ToDoForm,
  },

  data() {
    // 這裡可以初始化待辦事項列表
    return {
      ToDoItems00: [
        { label: "銀魂", done: true },
        { label: "鏈鋸人", done: false },
        { label: "進擊的巨人", done: true },
        { label: "鬼滅之刃", done: false },
        { label: "海賊王", done: true },
        { label: "火影忍者", done: false },
        { label: "名偵探柯南", done: true },
        { label: "我的英雄學院", done: false },
      ],
    };
  },
  methods: {
    // 這裡可以添加方法來處理待辦事項的新增、刪除等操作
  },
  mounted() {
    // 在組件掛載後可以進行一些初始化操作
    console.log("App 組件已掛載");
    //
  },
  watch: {
    // 可以監聽 ToDoItems00 的變化，進行相應的處理
    ToDoItems00(newVal) {
      console.log("待辦事項列表已更新:", newVal);
    },
  },
  computed: {
    // 可以添加計算屬性來處理待辦事項的統計等
  },


};
</script>

