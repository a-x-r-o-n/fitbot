<template>
  <aside class="w-full lg:w-16 bg-white dark:bg-[#1b2b3a] py-4 lg:py-6 flex lg:flex-col items-center justify-center gap-6 shadow-md">
    <div v-if="navBar === 0" @click="$emit('changeNav', 0)" class="navBar w-10 h-10 bg-yellow-400 rounded-lg"><strong>H</strong></div>
    <div v-else @click="$emit('changeNav', 0)" class="navBar  w-10 h-10 bg-gray-400 rounded-lg"><strong>H</strong></div>

    <div v-if="navBar === 1" @click="$emit('changeNav', 1)" class="navBar w-10 h-10 bg-yellow-400 rounded-lg"><strong>I</strong></div>
    <div v-else @click="$emit('changeNav', 1)" class="navBar w-10 h-10 bg-gray-400 rounded-lg"><strong>I</strong></div>
    
    <div v-if="navBar === 2" @click="$emit('changeNav', 2)" class="navBar w-10 h-10 bg-yellow-400 rounded-lg"></div>
    <div v-else @click="$emit('changeNav', 2)" class="navBar w-10 h-10 bg-gray-400 rounded-lg"></div>
  </aside>
</template>

<script>
export default{
  name: 'Sidebar',
  props: {"navBar": Number},
  data(){
    return{
      
    }
  }
}
</script>
<style scoped>
.navBar{
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
}
.navBar:hover{
    background-color: rgb(250,204,21,0.5);
}
</style>