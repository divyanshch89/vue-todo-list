<template>
  <div>
    <div v-bind:key="item.id" v-for="item in todos">
     <TodoItem v-bind:todo="item" v-on:del-todo="$emit('del-todo',item.id)"/>
    </div>
  </div>
</template>


<script>
import TodoItem from './TodoItem.vue';

export default {
  name: "Todos",
  components:{
      TodoItem
  },
  props: ["todos"],
};
</script>

<style scoped>
</style>