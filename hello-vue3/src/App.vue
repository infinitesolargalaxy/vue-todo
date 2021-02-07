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
        <todo-footer>
        </todo-footer>
    </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue';
import TodoFooter from './components/TodoFooter.vue';

export default {
    name: 'App',
    components: {
        TodoItem,
        TodoFooter,
    },
    data() {
        return {
            todoList: [
              {
                name: "Finish TODO",
                checked: false,
              },
              {
                name: "Add Vuex to allow creation of new TODO",
                checked: false,
              },
              {
                name: "PEN ROULETTE",
                checked: true,
              },
            ],
        };
    },
}
</script>

<style>
/* Global styles */
div {
  font-family: 'Karla', sans-serif;
  font-size: 13px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
}

body {
  margin: 0;
}

.todo-list {
  margin: 20px;
}
</style>
