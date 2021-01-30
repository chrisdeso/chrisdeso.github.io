<template>
  <div id="app">
    <h1>chrisdeso</h1>
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
        <to-do-item :label="item.label" :done="item.done" :id="item.id"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>
import uniqueId from 'lodash.uniqueid';
import ToDoItem from './components/ToDoItem.vue';

export default {
  name: 'app',
  components: {
    ToDoItem,
  },
  data() {
    return {
      ToDoItems: [
        { id: uniqueId('todo-'), label: 'Learn Vue', done: false },
        { id: uniqueId('todo-'), label: 'Build personal website', done: false },
        { id: uniqueId('todo-'), label: 'Walk the dogs', done: true },
        { id: uniqueId('todo-'), label: 'Eat a twinky', done: true },
        { id: uniqueId('todo-'), label: 'Schedule time off', done: false },
        { id: uniqueId('todo-'), label: 'Update resume', done: true },
      ],
    };
  },
};
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
