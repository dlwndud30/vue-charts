<template>
  <div id="app">
    <ul>
      <item-element v-for="(item, idx) in items" :key="idx">{{ item }}</item-element>
      <item-element>item6 <button>click me</button></item-element>
      <item-element>
        <div style="color:bisque; font-size:20px">item7</div>
      </item-element>
    </ul>
  </div>
</template>

<script>
import ItemElement from '@/ItemElement.vue';

export default {
  name: 'App',
  components: {
    ItemElement
  },
  data(){
    return{
      items:['아이템1', '아이템2', '아이템3', '아이템4', '아이템5'],
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
