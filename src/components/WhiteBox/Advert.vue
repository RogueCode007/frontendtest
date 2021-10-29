<template>
  <div class="box py-6 px-3 lg:flex lg:justify-between lg:px-16 lg:py-16">
      <div v-for="(a, index) in arr" :key="index" class="tile flex justify-center items-center">
          <p>ADVERTISEMENT</p>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            arr : [0, 1, 2]
        }
    }

}
</script>

<style scoped>
.tile{
background: #FBFBFB;
border: 1px solid #D6D6D6;
box-sizing: border-box;
border-radius: 4px;
padding: 100px;
margin-bottom: 20px;
}
.tile p{
    color: #C2C2C2
}
@media only screen and (min-width: 1024px){
    .tile{
        flex: 0 1 30%;
        padding: 120px 100px 
    }
}
</style>