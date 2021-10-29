<template>
  <div class="menu pb-6 border-b lg:px-16">
      <img :src="image4" alt="" class="menuitem">
      <img :src="image5" alt="" class="menuitem">
      <img :src="image1" alt="" class="menuitem">
      <img :src="image2" alt="" class="menuitem">
      <img :src="image3" alt="" class="menuitem">
  </div>
</template>

<script>
import image1 from "@/assets/1.png"
import image2 from "@/assets/2.png"
import image3 from "@/assets/3.png"
import image4 from "@/assets/4.png"
import image5 from "@/assets/5.png"
export default {
    data(){
        return {
            image1: image1,
            image2: image2,
            image3: image3,
            image4: image4,
            image5: image5,
        }
    }
}
</script>

<style scoped>

.menu{
  display: flex;
  flex-wrap: nowrap;
  overflow-x: auto;
  overflow-y: hidden;
  scroll-behavior: smooth;
  
}

.menu::-webkit-scrollbar
{
  height: 0px;
	background-color: #F5F5F5;
}
.menuitem{
  max-width: 250px;
  flex: 0 0 auto;
  margin-right: 40px;
  cursor: pointer;
  /* max-height: 260px */
}
@media only screen and (min-width: 1024px){
  .menu{
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .menuitem{
    flex: 0 0 15%
  }
}
</style>