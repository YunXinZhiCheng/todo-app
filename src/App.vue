<template>
  <main>
    <!-- 容器 -->
    <div class="container">
      <!-- 标题 -->
      <h1>欢迎使用 Todo 待办事项！</h1>
      <!-- 输入框和按钮 -->
      <div class="input-add">
        <input type="text" name="todo" />
        <button>
          <!-- 按钮图标 -->
          <i class="plus"></i>
        </button>
      </div>
      <!-- 过滤选项 -->
      <div class="filters">
        <span class="filter active">全部</span>
        <span class="filter">已完成</span>
        <span class="filter">未完成</span>
      </div>
      <!-- todo 列表 -->
      <div class="todo-list">
        <!-- todo 项目，外层容器用于显示背景、圆角边框 -->
        <div class="todo-item">
          <!-- 用 label 包裹后，点击里边任何一个元素都能触发 checkbox 的事件 -->
          <label>
            <input type="checkbox" />
            Todo 1
            <!-- 自定义的复选按钮 -->
            <span class="check-button"></span>
          </label>
        </div>
        <div class="todo-item">
          <label>
            <input type="checkbox" />
            Todo 2
            <span class="check-button"></span>
          </label>
        </div>
        <div class="todo-item">
          <label>
            <input type="checkbox" />
            Todo 3
            <span class="check-button"></span>
          </label>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
