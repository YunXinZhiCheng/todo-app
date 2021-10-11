<template>
  <!-- todo 列表 -->
  <div class="todo-list">
    <!-- todo 项目 -->
    <TodoListItem
      v-for="todo in todos"
      :key="todo.id"
      :todo-item="todo"
      @change-state="todo.completed = $event.target.checked"
    />
  </div>
</template>

<script>
// 导入子组件
import TodoListItem from '@/components/TodoListItem'
export default {
  name: 'TodoList',
  // 注册子组件
  components: {
    TodoListItem,
  },
  // props属性接收数据
  props: ['todos'],
}
</script>

<style>
/* 列表 */
.todo-list {
  display: grid;
  row-gap: 14px;
}
</style>
