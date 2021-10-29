<template>
  <div class="relative pinkbox lg:flex lg:items-end lg:pt-10 lg:pb-0 lg:px-16" style="background: #FFEBFF">
      <LeftBox />
      <!-- <RightBox /> -->
      <DemoBox />
  </div>
</template>

<script>
import LeftBox from "./LeftBox.vue"
// import RightBox from "./RightBox/RightBox.vue"
import DemoBox from "./RightBox/Demo.vue"
export default {
    components:{
        LeftBox, 
        // RightBox, 
        DemoBox
    }
}
</script>

<style>

</style>