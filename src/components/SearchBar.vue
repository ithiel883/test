<template>
<div>
    <input type="text" @keyup.enter="onSumbit()" class="search" v-model="value" placeholder="Search for photo">
</div>
<h1>hmm</h1>
</template>

<script>
export default {
    data() {
        return  {
            value: ''
        }
    },
    methods: {
        onSumbit() {
            this.$emit('sent', this.value)
            this.value = ''
        }
    }
}
</script>

<style scoped>
div {
    position: fixed;
    top: 0;
    left: 0;
    background-color: #ccc;
    width: 100vw;
    height: 180px;
   
}
input {
    padding: 20px;
    border: 0;
    border-radius: 3px;
    margin-top: 60px;
    width: 530px;
    box-shadow: 2px 3px 2px 2px #888888;

}
</style>