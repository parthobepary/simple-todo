<template>
  <div>
    <todo v-for="(todo, index) in todos" :key="index" :todo="todo" />
  </div>
</template>

<script>
import {mapState} from 'vuex'
import Todo from "./Todo.vue";
export default {
  components: {
    Todo,
  },
  computed: {
    ...mapState({
      todos: 'todos'
    })
    //   todos(){
    //       return this.$store.state.todos;
    //   }
  }
};
</script>

<style lang="scss" scoped>
</style>