<template> 
    <div class="add">
        <h3>Add Todo</h3>
        <form @submit="onSubmit">
            <input  class="Input" type="text"  placeholder="Add Todo..." v-model="title">
            <input class="addTodo" type="submit" value="Submit">
        </form>
    </div>
</template>

<script>
import {mapActions} from 'vuex';
export default {
    name: "addTodo",
    data(){

        return{
            title:''
        }
    },

    methods:{
        ...mapActions(['addTodo']),
        onSubmit(e){
            e.preventDefault();
            this.addTodo(this.title);
        }
    }
}
</script>

<style scoped>
form{
    display: flex;
}
.Input{
    flex: 10;
    padding: 10px;
    border:1px solid #41b883;
    outline: 0;
}
.addTodo{
    float: 2px;
    background: #41b883;
    color: #ffff;
    border: 1px solid #41b883;
    cursor: pointer;
}

</style>