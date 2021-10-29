<template>
  <div class="bg-white p-2 flex justify-between">
    <div @click="shownav = true" class="flex font-bold text-sm items-center p-2 border border-solid border rounded menu">
      Menu
      <svg  class="ml-2" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 18H3V16H12V18ZM21 13H3V11H21V13ZM21 8H12V6H21V8Z" fill="#FF6634"></path>
      </svg>
    </div>
    <div></div>
    <NavItems v-if="shownav" v-on:close="shownav = false" />
  </div>
</template>

<script>
import NavItems from "./NavItems.vue"
export default {
  components:{
    NavItems
  },
  data(){
    return{
      shownav : false
    }
  },
  methods:{
    showNav(){
      console.log('showNav')
    }
  }
}
</script>

<style lang="scss" scoped>
.menu{
  border: 1px solid #FF6634;
  color: #FF6634
}

</style>