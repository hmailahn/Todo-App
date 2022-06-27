<script >

export default {
    name: 'todo-list',
    data () {
        return {
            newTodo: '', 
            todos: [
                {
                    'id': 1,
                    'title': 'Finish Vue Screencast',
                    'completed': false,
                },
                {
                    'id': 2,
                    'title': 'Take over world',
                    'completed': false,
                }
            ]

        }
    }
    methods: {
        addTodo(){
            alert('adding')
        }
    }
} 

</script>

<template>
  <div >
  <input type="text" class="todo-input" placeholder="What needs to be done" v-model="newTodo" @keyup.enter="addTodo">
  <div v-for="todo in todos" :key="todo.id" class="todo-item">
{{ todo.title }}
  </div>
  </div>
</template>



<style >
.todo-input {
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;

    &:focus {
        outline: 0;
    }
}
</style>
