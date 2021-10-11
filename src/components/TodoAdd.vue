<template>
  <!-- 输入框和按钮
       双向数据绑定
       表单回车事件 @keyup.enter
       按钮点击事件 @click
   -->
  <div class="input-add">
    <input
      type="text"
      name="todo"
      v-model="todoContent"
      @keyup.enter="emitAddTodo"
    />
    <button @click="emitAddTodo">
      <!-- 按钮图标 -->
      <i class="plus"></i>
    </button>
  </div>
</template>

<script>
// 导入setup函数
import { ref } from 'vue'
export default {
  name: 'TodoAdd',
  // setup函数
  setup(props, context) {
    const todoContent = ref('')
    // 事件处理函数
    const emitAddTodo = () => {
      const todo = {
        id: props.id,
        content: todoContent.value,
        complete: false,
      }
      context.emit('add-todo', todo)
      // 清空输入框内容
      todoContent.value = ''
    }

    // return返回对象
    return {
      todoContent,
      emitAddTodo,
    }
  },
}
</script>

<style>
/* 添加框 */
.input-add {
  position: relative;
  display: flex;
  align-items: center;
}
/* 添加框里面的表单 */
.input-add input {
  padding: 16px 52px 16px 18px;
  border-radius: 48px;
  border: none;
  outline: none;
  box-shadow: 0px 0px 24px rgba(0, 0, 0, 0.08);
  width: 100%;
  font-size: 16px;
  color: #626262;
}
/* 添加框里面的按钮 */
.input-add button {
  width: 46px;
  height: 46px;
  border-radius: 50%;
  background: linear-gradient(#9f98e8, #aff6cf);
  border: none;
  outline: none;

  color: white;
  position: absolute;
  right: 0px;

  cursor: pointer;
}
/* 按钮里面的加号 */
.input-add .plus {
  display: block;
  width: 100%;
  height: 100%;
  background: linear-gradient(#fff, #fff), linear-gradient(#fff, #fff);
  background-size: 50% 2px, 2px 50%;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
