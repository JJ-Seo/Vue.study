<template>
    <button class="list-group-item text-left w-100 p-3" @click="clickButton">
            {{ label }}
    </button>  
</template>

<script>
export default {
    props: ['label'],
    methods: {
        clickButton(){
            this.$emit('componentClick')
        }
    }
};
</script>

<style>

</style>