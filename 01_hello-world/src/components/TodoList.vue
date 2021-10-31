<template>
    <div>
       <div>
           <input type="text" v-model="inputValue">
           <button @click="addItem" >추가하기</button>
       </div>
       <ul>
           <ListItem
           v-for="(value, index) in listArray"
           :key="index"
           :style="style"
           :text="value === '' ? undefined : value"
           :index="index"
           @delete="catchDeleteItem"
           />
           <!-- @delete="(index) => catchDeleteItem(index)" -->
       </ul>
    </div>
</template>
<script>
import ListItem from "./ListItem";

export default {
    data(){
        return{
            inputValue: "",
            listArray: [],
            style: {
                color: "green",
            }
        }
    },
    components: {
        ListItem
    },
    methods: {
        addItem(){
            this.listArray.push(this.inputValue);
            this.inputValue = "";
        },
        catchDeleteItem(index){
            console.log(index)
            this.listArray.splice(index, 1)

        }
    },
}
</script>
<style lang="">
    
</style>