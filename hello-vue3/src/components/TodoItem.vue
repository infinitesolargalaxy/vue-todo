<template>
  <div class="todo-wrapper">
    <div class="checkbox-wrapper">
        <input type="checkbox" id="checkbox" v-model="checked">
        <!-- <label for="checkbox">{{ checked }}</label> -->
    </div>
    <div class="name">{{ name }}</div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props: {
    name: String,
    // checked: Boolean,
  },
  data() {
      return {
          checked: false,
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.todo-wrapper {
    display: flex;
    flex-direction: row;
    border: 1px solid black;
    border-radius: 5px;

    margin: 5px;
    width: 300px;
}
.name {
    font-size: 12px;
    font: Karla;

    margin-top: auto;
    margin-bottom: auto;
    margin-left: 12px;
}
</style>
