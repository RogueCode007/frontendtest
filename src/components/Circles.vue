<template>
  <div class="absolute circlebox">
    <div id="outer-circle">
        <div id="inner-circle1"></div>
        <div id="inner-circle2"></div>
        <div id="inner-circle3"></div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.circlebox{
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    /* border: 1px solid red */
}
#outer-circle {
   border:  1px solid #FED5FE;
   border-radius: 50%;
   height: 350px;
   width: 350px;
   position: relative;
   /* 
    Child elements with absolute positioning will be 
    positioned relative to this div 
   */
 }
 #inner-circle1{
   position: absolute;
   border:  1px solid #FED5FE;
   border-radius: 50%;
   height: 250px;
   width: 250px;
   /*
    Put top edge and left edge in the center
   */
   top: 50%;
   left: 50%;
   margin: -125px 0px 0px -125px;
 }
 #inner-circle2 {
   position: absolute;
   border:  1px solid #FED5FE;
   border-radius: 50%;
   height: 150px;
   width: 150px;
   /*
    Put top edge and left edge in the center
   */
   top: 50%;
   left: 50%;
   margin: -75px 0px 0px -75px;
   /* 
    Offset the position correctly with
    minus half of the width and minus half of the height 
   */
 }
 @media only screen and (min-width: 1024px){
   #outer-circle {
   height: 650px;
   width: 650px;
 }
 #inner-circle1{
   height: 480px;
   width: 480px;
   margin: -240px 0px 0px -240px;
 }
 #inner-circle2{
   height: 300px;
   width: 300px;
   margin: -150px 0px 0px -150px;
 }
 #inner-circle3 {
   position: absolute;
   border:  1px solid #FED5FE;
   border-radius: 50%;
   height: 150px;
   width: 150px;
   /*
    Put top edge and left edge in the center
   */
   top: 50%;
   left: 50%;
   margin: -75px 0px 0px -75px;
   /* 
    Offset the position correctly with
    minus half of the width and minus half of the height 
   */
 }
 }
</style>