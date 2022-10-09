<template>
  <div style="width:250px; margin:5px auto;">
    <div style="display:flex; justify-content:space-between">
      <span :class="{completed: todo.completed}" @click="toggleTodoStatus(todo)">{{ todo.title }}</span>
      <button @click="deleteTodo(todo)">Delete</button>
    </div>
  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
  props: ['todo'],
  methods:{
    ...mapActions({
      deleteTodo: 'deleteTodo',
      toggleTodoStatus: 'toggleTodoStatus'
    })
    // deleteTodo(){
    //     this.$store.dispatch('deteleTodo', this.todo)
    // },
    // toggleTodoStatus(){
    //     this.$store.dispatch('toggleTodoStatus', this.todo)
    // }
  }
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
}
</style>