<template>
  <div>
    <ul>
        <li v-for="(item,idx) in items" :key="idx">{{ item }}</li>
    </ul>
    <button @click="onClick">renew</button>
  </div>
</template>

<script>
export default {
    props:{
        items: {
            type: Array,
            required: true,
        }
    },
    methods:{
        onClick(){
            this.$emit('renew');
        }
    }
}
</script>

<style>

</style>