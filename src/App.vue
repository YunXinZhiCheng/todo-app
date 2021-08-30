<template>
  <main>
    <!-- 容器 -->
    <div class="container">
      <!-- 标题 -->
      <h1>欢迎使用 Todo 待办事项</h1>

      <!-- 输入框和按钮 -->
      <TodoAdd />

      <!-- 过滤选项 -->
      <TodoFilter />

      <!-- todo 列表 -->
      <TodoList />
    </div>
  </main>
</template>

<script>
// 导入子组件
import TodoAdd from '@/components/TodoAdd'
import TodoFilter from '@/components/TodoFilter'
import TodoList from '@/components/TodoList'
export default {
  name: 'App',
  // 注册子组件
  components: {
    TodoAdd,
    TodoFilter,
    TodoList,
  },
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Helvetica, 'PingFang SC', 'Microsoft Yahei', sans-serif;
}

/* 整个页面 */
main {
  width: 100vw;
  min-height: 100vh;
  display: grid;
  align-items: center;
  justify-items: center;
  background-color: #b8c6db;
  background-image: linear-gradient(315deg, #b8c6db 0%, #f5f7fa 74%);
}
/* 容器 */
.container {
  width: 60%;
  max-width: 400px;
  box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.15);
  border-radius: 24px;
  padding: 48px 28px;
  background-color: rgb(245, 246, 252);
}

/* 标题 */
h1 {
  margin: 24px 0;
  font-size: 28px;
  color: #414873;
}
</style>
