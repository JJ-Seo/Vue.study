<template>
  <div id="app">
    <div class="container">
      <div class="com-md-6 offser-md-3">
        <h1 class="text-center mb-4">Todo App</h1>
        <input type="text" class="form-control mb-4" v-model="userInput" @keyup.enter="addNewTodo">

        <div class="list-group mb-4">
          <div v-for="todo in activeTodoList" :key="todo">
            <todo 
              :label="todo.label"
              @componentClick="toggleTodoState(todo)"
              
            />
          </div>
        </div>

        <div class="text-right">
          <button type="button" class="btn btn-sm" @click="changeCurrentState('active')">To do List</button>
          <button type="button" class="btn btn-sm" @click="changeCurrentState('done')">Done</button>
          <button type="button" class="btn btn-sm" @click="changeCurrentState('all')">All</button>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
  import Todo from './components/Todo.vue';

export default {
  name: 'App',

  data() {
    return{
      userInput:'',
      todoList:[],
      currentState: 'active'      
    };
  },

  computed: {
    activeTodoList(){
      return this.todoList.filter(todo => this.currentState ==='all' || todo.state === this.currentState);
    }
    
  },

  methods:{
    changeCurrentState(state){
      this.currentState = state;
    },
    addNewTodo(){
      this.todoList.push({
        label: this.userInput,
        state: 'active'
      });
      this.userInput = '';
    },
    toggleTodoState(todo){
      todo.state = todo.state === 'active' ? 'done' : 'active';
    }
  },
  components: {
    Todo
  }
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
.text-left{text-align: left;}
</style>
