<template>
    <li>
        {{text}}
        <button @click="itemDelete">삭제</button>
    </li>
</template>
<script>
export default {
    // props: ["text"]
    props:{
        index:{
            type: Number,
        },
        text: {
            type: String,
            required: true,
            default: "안녕!"
        }
    },
    methods: {
        itemDelete(){
            this.$emit('delete', this.index);
        }
    },
}
</script>
<style>
    
</style>