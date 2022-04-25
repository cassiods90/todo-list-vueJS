
<template>
    <section class="filter">
        <div class="container">
            <h1 class="text title black">Find a todo:</h1>
            <div class="filter-content row justify-content-between align-items-center">
                <div class="col-12 col-md-6 col-lg-8">
                    <div class="filter-content-input">
                        <input type="text" placeholder="Type a to do name" @keyup="submit()" >                    
                    </div>
                </div>
                <div class="col-12  col-md-4 col-lg-4">
                    <div class="filter-content-select">
                        <select name="Select status" id="" v-model="selectedOption">
                            <option value="all">All</option>
                            <option value="todo">To do</option>
                            <option value="doing">Doing</option>
                            <option value="done">Done</option>
                        </select>
                    </div>
                </div>
                <!-- <ul>
                    <li v-for="item in computed_items">
                        <span>{{ todo.title }}</span>
                        <span>{{ todo.option }}</span>
                    </li>
                </ul> -->
                <!-- <div class="col-1">
                    <div class="filter-content-icon d-flex justify-content-center align-items-center">
                        <img  src="@/assets/images/search/loupe.png" alt="">
                    </div>
                </div> -->
            </div>
        </div>     
    </section>
</template>

<script>


export default {
    name: 'AppFilter',
    props: {
        todos: {
            type: Array,
            default: () => {
                return []
            }  
        },
    },
    data() {
        return {
            selectedOption: ''
        }
    },
    methods: {
        submit() {
            console.log('submit')
            console.log('key enter all todos', this.todos)
        }
    },
    computed: {
        
    },
}
</script>