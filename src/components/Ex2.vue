<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                userInput: "",
            }
            
        },
        methods:{
            addItem(){
                if (this.userInput !== ''){
                    this.items.push(this.userInput);
                    this.userInput = '';
                }
            },
            deleteItem(index){
                this.items.splice(index, 1);
            }
            
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul v-for="(item, index) in items" v-bind:key="index">
        <li>{{item}} <button @click="deleteItem(index)">Delete!</button></li>
    </ul>
    <input v-model="userInput"><button @click="addItem()">Add!</button>
   
</template>
