<template>
    <div>
        <div class="todo-list">
          <todo-item
            v-for="(item, index) in todoList" :key="index"
            :name="item.name"
            :checked="item.checked"
          >
          </todo-item>
        </div>
    </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
    name: 'App',
    components: {
        TodoItem
    },
    data() {
        return {
            todoList: [
              {
                name: "Finish TODO",
                checked: false,
              },
              {
                name: "PEN ROULETTE",
                checked: true,
              },
            ]
        };
    },
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
