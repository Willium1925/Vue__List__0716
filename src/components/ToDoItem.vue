<template>
  <div>
    <input type="checkbox" :id="id" :checked="isDone" />
    <label :for="id">{{label}}</label> <!-- :for 指的是下方的 id -->
  </div>
</template>

<script>
export default {
  props: {
    label: { required: true, type: String },
    done: { default: false, type: Boolean }
  },
  data() {
    return {
      isDone: this.done,
      id: "todo-" + crypto.randomUUID(), // 自動生成唯一 ID
    };
  },
};
</script>