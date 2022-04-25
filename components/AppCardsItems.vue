
<template>
    <section class="cards-items">
        <div class="container">
            <div class="d-flex justify-content-start align-items-center">
                <span class="text title black">To do cards:</span>
                <button  class="field-button" v-on:click="addTodo">
                    <span class="">New Todo</span>                  
                </button>
            </div>
            
            <div class="professional-cards-items row flex-wrap justify-content-start align-items-start">
                <div class="col-12 col-md-6 col-lg-4" v-for="(todo, i) in todos">
                    <Todo :index="i" :data="todos[i]" :deleteFunc="removeTodo"></Todo>
                </div>
                <!-- <CardItem v-for="(professionalItem) in professionalItems" :key="`professional-item-${professionalItem.id}`"  :value="professionalItem"/> -->               
            </div>
        </div>   
    </section>
</template>

<script>
import CardItem from '@/components/cards/CardItem';
import Todo from "@/components/cards/Todo.vue";

export default {
    name: 'AppCardsItems',
    components: {
        CardItem,
        Todo,
    },
    props: {
        todos: {
            type: Array,
            default: () => {
                return []
            }  
        },
    },
    data: function () {
        return {
            
        }
    },
    methods: {
        addTodo(){
            this.todos.push({
                id: Date.now(),
                title: 'New Todo ' + this.todos.length,
                mode: true,
                option: 'todo',
                list: []
            })
            // console.log('addTodo', this.todos)
        },
        removeTodo(index){
            this.todos.splice(index, 1);
        }
    },
}
</script>