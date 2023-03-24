<template>
  <ul class="todo-main">
    <MyItem
      v-for="todoObj in todos"
      :key="todoObj.id"
      :todo="todoObj"
      :checkTodo="checkTodo"
      :a="true"
      :deleteTodo="deleteTodo"
    />
  </ul>
</template>
/*不仅要根据数据的数量去遍历用多少次Myitem，还要把数据的具体信息传递给Myitem*/
<script>
import MyItem from "./MyItem.vue";

export default {
  name: "MyList",
  components: { MyItem },
  props: ["todos", "checkTodo", "deleteTodo"],
};
</script>


<style scoped>
/*main*/
.todo-main {
  margin-left: 0px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0px;
}

.todo-empty {
  height: 40px;
  line-height: 40px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding-left: 5px;
  margin-top: 10px;
}
</style>